# container that can be used to build kernel packages.
# archlinux image created with:
# https://github.com/docker/docker/blob/master/contrib/mkimage-arch.sh
FROM archlinux
MAINTAINER George Angelopoulos

# enable multilib repo
RUN sed -i '/^#\[multilib\]/ {s/^#//;n;s/^#//}' /etc/pacman.conf

RUN pacman --noconfirm -Syy
RUN pacman --noconfirm --needed -S sudo base-devel

# passwordless root through sudo for wheel group
RUN sed -i '/^#.*NOPASSWD/s/^# //' /etc/sudoers

RUN useradd -G wheel -m builder

USER builder

RUN gpg --keyserver https://pgp.mit.edu --recv-keys 0xABAF11C65A2970B130ABE3C479BE3E4300411886 0x647F28654894E3BD457199BE38DBBDC86092693E
