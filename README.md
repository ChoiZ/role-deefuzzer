# role-deefuzzer
ansible role for deefuzzer

## Example Playbook

    - hosts: stream-server
      vars_files:
        - vars/deefuzzer.yml
      roles:
        - role-deefuzzer

## Example vars/deefuzzer.yml

    ---
    deefuzzer_log: /path/to/deefuzzer.log
    deefuzzer_m3u: /path/to/deefuzzer.m3u
    
    deefuzzer_stationdefaults_control_mode: 1
    deefuzzer_stationdefaults_control_port: 16001
    deefuzzer_stationdefaults_jingle_dir: /path/to/jingles
    deefuzzer_stationdefaults_jingle_mode: 0
    deefuzzer_stationdefaults_jingle_shuffle: 1
    
    deefuzzer_stations:
      - name: 70s
        infos:
        - description: My 70's station
        - genre: 70s
        - name: My 70's Station - www.70s-station.fm
        media:
        - bitrate: 128
        - source: /path/to/mp3_or_m3u_file
        - format: mp3
        - ogg_quality: 4
        - samplerate: 44100
        - shuffle: 0
        - voices: 2
        feeds:
        - mode: 1
        - rss: 0
        - json: 1
        - playlist: 1
        - dir: /path/to/meta_folder
        - enclosure: 1
        - media_url: https://www.70s-station.fm/media
        server:
        - host: 127.0.0.1
        - mountpoint: 70s
        - port: 8000
        - public: 1
        - sourcepassword: source_password_of_icecast
        - type: icecast
        - appendtype: 1
      - name: 80s
        infos:
        - description: My 80's station
        - genre: 80s
        - name: My 80's Station - www.80s-station.fm
        media:
        - bitrate: 128
        - source: /path/to/mp3_or_m3u_file
        - format: mp3
        - ogg_quality: 4
        - samplerate: 44100
        - shuffle: 0
        - voices: 2
        feeds:
        - mode: 1
        - rss: 0
        - json: 1
        - playlist: 1
        - dir: /path/to/meta_folder
        - enclosure: 1
        - media_url: https://www.80s-station.fm/media
        server:
        - host: 127.0.0.1
        - mountpoint: 80s
        - port: 8000
        - public: 1
        - sourcepassword: source_password_of_icecast
        - type: icecast
        - appendtype: 1
    
## Licence

MIT

## Author Information

This role was created by François LASSERRE aka ChoiZ.
