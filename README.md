this.http.get(fileUrl, { responseType: 'arraybuffer' })
      .subscribe((data: ArrayBuffer) => {
        const blob = new Blob([data], { type: 'application/vnd.apple.pkpass' });
        this.fileSaverService.saveAs(blob, filename);
      });
