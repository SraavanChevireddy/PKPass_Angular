npm install ngx-filesaver --save


<a href="/path/to/your/pkpassfile.pkpass" download="yourfile.pkpass">
  <button>Open PKPass File</button>
</a>



import { Component } from '@angular/core';
import { FileSaverService } from 'ngx-filesaver';

@Component({
  selector: 'app-your-component',
  template: `
    <button (click)="downloadFile()">Open PKPass File</button>
  `,
})
export class YourComponent {
  constructor(private fileSaverService: FileSaverService) {}

  downloadFile() {
    // Replace 'yourfile.pkpass' with the desired filename
    const filename = 'yourfile.pkpass';

    // Replace '/path/to/your/pkpassfile.pkpass' with the actual path to your PKPass file
    const filePath = '/path/to/your/pkpassfile.pkpass';

    this.fileSaverService.saveAs(filePath, filename);
  }
}
