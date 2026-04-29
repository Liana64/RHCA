# Linux Paths

A list of useful Linux paths.

**Users and authentication**
```sh
/etc/passwd                             # Passwords
/etc/shadow                             # Hash map for passwords
/etc/group                              # Groups
/etc/skel/                              # Home folder skeleton
/etc/profile                            # System-wide bash profile
/etc/bashrc                             # System-wide bashrc
/etc/login.defs                         # Password policy defaults
/etc/sudoers                            # Sudoers
/etc/sudoers.d/                         # Sudoers drop-in files
/etc/openldap/cacerts/                  # LDAP server certificates
/etc/sssd/sssd.conf                     # SSSD service config
/etc/nslcd.conf                         # NSLCD config
/etc/krb5.keytab                        # Kerberos keytab
/etc/krb5.conf                          # Kerberos config
/etc/krb5.conf.d/                       # Kerberos drop-in files
/etc/ipa/ca.crt                         # IPA server certificate
/etc/ssh/sshd_config                    # SSH config
/etc/ssh/sshd_config.d/                 # SSH drop-in files
/etc/sysconfig/authconfig               # PAM settings
/etc/pam.d/                             # PAM drop-in files
/etc/openldap/ldap.conf                 # LDAP config
/etc/authselect/                        # Authselect files
```

**Generators**
```sh
/dev/zero                               # Endless zeroes
/dev/random                             # Stream getrandom syscall #1
/dev/urandom                            # Stream getrandom syscall #2
```

**It's always DNS**
```sh
/etc/hosts                              # DNS mapping
/etc/hostname                           # Hostname map
/etc/resolv.conf                        # DNS config
/etc/nsswitch.conf                      # Name Service Switch config, defines
\                                       # where the system looks up various
\                                       # information, such as hosts (hostname)
\                                       # `hosts: files dns myhostname`, passwd
\                                       # `passwd: files sss ldap`, shadow
\                                       # `shadow: files sss ldap`, sudoers
\                                       # and others. Don't edit this file,
\                                       # instead use `authselect`
```

**Filesystems and storage devices**
```sh
/etc/fstab                              # Filesystem mount table
/etc/crypttab                           # Mount table for encrypted volumes
/etc/lvm/backup                         # LVM backups
/etc/lvm/archive                        # LVM backup archives
/etc/lvm/lvm.conf                       # LVM config
/etc/stratis/                           # Stratis pools
/sys/block/                             # Configure block devices,
\                                       # e.g., I/O scheduling settings
/var/lib/iscsi                          # Stores iSCSI device information for
\                                       # the iSCSI initiator, which is
\                                       # identified by an Internet Qualified
\                                       # Name (IQN)
/etc/iscsi/iscsid.conf                  # iSCSI config
/etc/iscsi/initiatorname.iscsi          # iSCSI initiator
/etc/target/backup                      # iSCSI config backups
/etc/multipath.conf                     # Device mapper multipath config
```

**Security and misc logging**
```sh
/etc/rsyslog.conf                       # Rsyslog config
/var/log/cron                           # Cron logs
/var/log/secure                         # PAM logs
/var/log/messages                       # General logs
/var/log/audit/audit.log                # Auditd/SELinux logs
```

**Networking**
```sh
/etc/sysconfig/network-scripts          # Network config scripts (RHEL 8)
\                                       # Equivalent to /etc/network/interfaces
/etc/NetworkManager/                    # Not used in RHEL 8
/etc/firewalld/firewalld.conf           # Firewall config
/etc/nftables.conf                      # nftables config
```

**Kernel and hardware**
```sh
/var/crash                              # Kernel crash dumps
/proc/cmdline                           # Current kernel boot parameters
/etc/modprobe.d/                        # Custom kernel modules specified here
\                                       # e.g., options cdrom debug=1
/etc/sysctl.conf                        # Kernel tuning config
/etc/sysctl.d/                          # Kernel tuning drop-in files
/sys/module/amdgpu/parameters           # View kernel module params, e.g. amdgpu
/sys/devices/system/node                # NUMA topology
/sys/devices/system/edac/mc             # Memory controller
/proc/sys/vm/swappiness                 # Swappiness
/proc/sys/net/ipv4/ip_forward           # IP forwarding status
/var/lib/rasdaemon                      # Rasdaemon database is typically here
/etc/dracut.conf                        # Initramfs config
/etc/kdump.conf                         # kdump config
/etc/tuned/tuned-main.conf              # Tuned config
```

**Systemd**
```sh
/etc/systemd/journald.conf              # Journald config
/etc/systemd/system                     # Overrides and active unit links
/usr/lib/systemd/system                 # Systemd services and units live here
/usr/lib/systemd/systemd                # Systemd binary, used with exec
/run/systemd/system                     # Runtime generated units
```

**Misc**
```sh
/etc/os-release                         # Distribution info
/etc/securetty                          # List of secure TTYs
/etc/services                           # List of all services and ports
/var/spool                              # Simultaneous Peripheral Operations
\                                       # On-Line (SPOOL), queued work for some
\                                       # services like cups and cron    
```

**Packages**
```sh
/var/lib/rpm                            # RPM database
/etc/dnf/dnf.conf                       # DNF config
/etc/yum.repos.d/                       # Yum drop-in files
```

**Documentation**
```sh
/usr/share/doc                          # Various documentation and examples
/usr/share/systemtap/examples/          # SystemTap examples
```
