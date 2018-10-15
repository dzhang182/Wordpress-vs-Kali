# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **up to five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: <img src="https://github.com/dzhang182/Wordpress-vs-Kali/blob/master/wp%201.gif" width="800">
  - [ ] Steps to recreate: Create a new post. Insert url embed shortcode with any youtube video link. At the end of the youtube video link, insert the escape code sequence \x3c (<) followed by your xss code, ended with \x3e (>). Viewing the post will create alert.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset/40160/trunk/src/wp-includes/embed.php?old=38361&old_path=trunk%2Fsrc%2Fwp-includes%2Fembed.php)
2. (Required) Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough: <img src="https://github.com/dzhang182/Wordpress-vs-Kali/blob/master/wp%202.gif" width="800">
  - [ ] Steps to recreate: Create a new post. Splice HTML tag with shortcode tag to to create alert on mouse click.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8)
3. (Required) Authenticated Cross-Site Scripting (XSS) with alert
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough: <img src="https://github.com/dzhang182/Wordpress-vs-Kali/blob/master/wp%203.gif" width="800">
  - [ ] Steps to recreate: Create a new post. In the text box, add the alert tag. Viewing post will create alert.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset/36185)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Daniel Zhang]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
