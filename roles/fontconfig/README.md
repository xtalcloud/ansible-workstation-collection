Role Name
=========

Requirements
------------

Role Variables
--------------

The most important variable is `font_archive_full_url`, defined as:

  font_archive_full_url: "{{ font_archive_root_url }}/{{ font_family|urlencode }}/{{ font_archive_checksum }}.tar"

By default, there above assumptions are made regarding how to find the relevant archive file containing the folder with the font families associated TTF files.

  font_archive_root_url: https://your.com/base/path
  font_family: DejaVu Sans Mono
  font: 67bf06b25105e140d16feed3c4aad7afff5f8be5e97477c30990e038e876a7c0

Would fetch the file at the following URL:

  https://your.com/base/path/DejaVu%20Sans%20Mono/67bf06b25105e140d16feed3c4aad7afff5f8be5e97477c30990e038e876a7c0.tar

It is assumed, by default, that the archive contains a single directory named according to the following nameing scheme:

  font_family_dirname: "{{ font_family|lower|replace(' ','-')  }}"

Thus the archive containing the TTF files when: 

  font_family: DejaVu Sans Mono

Would consist of a directory with the following name, containing TTF font files:

  font_family_dirname: dejavu-sans-mono

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
