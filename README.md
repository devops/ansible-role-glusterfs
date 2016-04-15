# Ansible Role: glusterfs

Install GlusterFS Server or Client On Linux.

## Requirements

- CentOS7默认的base源里存在glust-fuse 3.6版本的软件包，如果要安装自己指定版本的Fuse Client, 请设置`glusterfs_baserepo_disabled: true`.
- CentOS7用于KVM主机时,请安装系统自带的或是大于3.6版本的GlusterFS.

## Role Variables

`defaults/main.yml`

* `glusterfs_repo_baseurl: http://download.gluster.org/pub/gluster/glusterfs/3.4/LATEST/EPEL.repo/epel-7/x86_64/`
* `glusterfs_baserepo_disabled: false`
* `glusterfs_server: false`
* `glusterfs_client: false`

## Dependencies

None

## Example Playbook

    - hosts: servers
      vars:
        glusterfs_repo_baseurl: http://download.gluster.org/pub/gluster/glusterfs/3.4/LATEST/EPEL.repo/epel-7/x86_64/
        glusterfs_server: true
      roles:
         - glusterfs

    - hosts: servers
      vars:
        glusterfs_repo_baseurl: http://download.gluster.org/pub/gluster/glusterfs/3.4/LATEST/EPEL.repo/epel-7/x86_64/
        glusterfs_client: true
      roles:
        - glusterfs

## Author Information

z
