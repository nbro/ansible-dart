dart
=========

Dart is a cohesive, scalable platform for building apps that run on the web (where you can use Polymer) or on servers (such as with Google Cloud Platform). Use the Dart language, libraries, and tools to write anything from simple scripts to full-featured apps.
This ansible script is based off of the official instructions for ubuntu (https://www.dartlang.org/tools/download.html)

Role Variables
--------------

```
dart_signing_key_url: https://dl-ssl.google.com/linux/linux_signing_key.pub
dart_source_list_url: https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list
dart_source_list_path: /etc/apt/sources.list.d/dart_stable.list
dart_package: dart
dartium_archive_name: dartium-linux-x64-release
dartium_url: https://storage.googleapis.com/dart-archive/channels/stable/release/latest/dartium/{{dartium_archive_name}}.zip
dartium_path: /opt/google/dartium

```

Example Playbook
----------------

    - hosts: all
      roles:
        - { role: jgrowl.dart, when: ansible_os_family == "Debian", become: yes }

License
-------

MIT

Author Information
------------------

jonrowlands83@gmail.com
