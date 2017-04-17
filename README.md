# Project 9 - Honeypot

Time spent: **7** hours spent in total

> Objective: Setup a honeypot and provide a working demonstration of its features.

### Required: Overview & Setup

- [x] A basic writeup (250-500 words) on the `README.md` desribing the overall approach, resources/tools used, findings
  - There's a multitude of resources for setting up your own honeypot. Even on Github alone there are [masterlists](https://github.com/paralax/awesome-honeypots) of honeypots-- ranging from the quirkily named WordPress honeypots like [HonnyPotter](https://github.com/MartinIngesen/HonnyPotter), to database honeypots that detect attackers and logging attack incidents. However, despite all the resources available, the act of deploying a honeypot for the first time can be overwhelming and perplexing. Ultimately I decided it would be best to take the well-documented approach for my first attempt— using Vagrant to set up a Modern Honeypot Network honeypot. Using the VM provider VirtualBox, I cloned the [MHN source](https://github.com/threatstream/mhn) (git clone https://github.com/threatstream/mhn.git) and launched the source using Vagrant. This created two virtual machines— the honeypot, which was the target, and the server, which ran the admin console for monitoring data collected by the honeypot. After installing git to the server, I used a patched fork instead of the primary MHN repo (issue with primary explained [here](https://github.com/threatstream/mhn/issues/383)) and launched the pre-requisite install scripts (hpfeeds, mnemosyne, honeymap). Finally, I ran the server install script (./install_mhnserver.sh). Once completed, I went to MHN console via a browser, and copied the deploy command for Ubuntu - Dionea. [Dionaea](https://github.com/rep/dionaea) is a low interaction honeypot that traps malware, but in this instance it was just used to detect port scanning. Once executed, the honeypot was ready to be put to work.
- [x] A specific, reproducible honeypot setup, ideally automated:
	- **A Vagrantfile or Dockerfile which provisions the honeypot as a VM or container**
	
### Required: Demonstration

- [x] A basic writeup of the attack (what offensive tools were used, what specifically was detected by the honeypot)
  
- [x] An example of the data captured by the honeypot (example: IDS logs including IP, request paths, alerts triggered)
- [x] A walkthrough of the attack being conducted
      <img src='http://i.imgur.com/wF6NoaD.gif' title='Gif Walkthrough' width='' alt='Gif Walkthrough' />
    
GIF created with [LiceCap](http://www.cockos.com/licecap/).

## License

    Copyright [2017] [Nora Gilmartin]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
