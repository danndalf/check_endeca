NAME
    check_endeca - Nagios plugin to poll Endeca dgraph status

DESCRIPTION
    This script acts as a plugin module for the Nagios IT infrastructure
    monitoring system. It polls an Endeca server for dgraph status
    information and responds with a status string and appropriate exit
    status.

SYNOPSIS
  Command Line Interface
    Poll status on a server with no encryption or authentication:

            check_endeca -H your_host.com

  Running within Nagios
    In objects/commands.cfg:

            define command{
            command_name    check_endeca
            command_line    $USER1$/check_endeca -H $HOSTNAME$
            }

    In the configuration file for your host with apache running on it:

            define service{
            use                   local-service
            host_name             your.hostname.com
            service_description   Endeca DGraph
            check_command         check_endeca
            }

SEE ALSO
    If using an external configuration file, it should be structured
    according to the specification at
    <http://nagiosplugins.org/extra-opts/>.

    This module is built upon Nagios::Plugin by the Nagios Plugin
    Development Team. Further reading on Nagios, NPRE, and Nagios Plugins is
    available at <http://nagios.com/>.

AUTHOR
    This script is written and maintained by Danne Stayskal
    <danne@stayskal.com> and is available on his website, at
    <http://danne.stayskal.com/software/check_endeca/>.

LICENSE
    Copyright (C) 2013 by Danne Stayskal.

    This program is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License as published by the
    Free Software Foundation; either version 2 of the License, or (at your
    option) any later version.

    This program is distributed in the hope that it will be useful, but
    WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
    Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    59 Temple Place, Suite 330, Boston, MA 02111-1307 USA

    Nagios, the Nagios logo, and Nagios graphics are the servicemarks,
    trademarks, or registered trademarks owned by Nagios Enterprises. All
    other servicemarks and trademarks are the property of their respective
    owner.

