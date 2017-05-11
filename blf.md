sipXsss
=======

(sipXsss)[https://github.com/ezuce/sipXsss] - an application to monitor Sip UA states and provide
notification of state changes.

Current state
=============

Application analyzes SIP packets forwarded by SIP proxy and tries to assemble SIP dialogs out of it,
and then deduce the state of SIP UA (identified by SIP URI). States could be Ringing, Busy and Available.

There are some issues related with Polycom devices support (requested by customers), mostly related
with Polycom ability to display what's going on with other call end. This support is incomplete,
and in fact, couldn't be complete, as this requires the application to act as a full-fledged softswitch
system (think of FreeSWITCH and Asterisk).

How it should be
================

The idea is to make SSS work reliably by tracking the state of SIP UAs only (thus removing Polycom support),
and focusing on standard SIP messages NOTIFY, PUBLISH and SUBSCRIBE.

It would be useful to have a registry of SIP UAs states for other applications to integrate, ReachMe namely.

FreeSWITCH
==========

There should be an option to route calls through FreeSWITCH instance(s), either signalling only, or with audio.

Anchoring calls to FreeSWITCH will allow:

1. Transcode audio/video
2. Provide NAT support
3. Develop and offer PBX functionality
4. Have complete information about calls (for Polycom devices)

This is somehow related with how ReachMe works by automating FreeSWITCH and tracking calls states by processing
FreeSWITCH events.

Required Modifications
======================

At some point in time Anchoring SIP signalling in FS will be the default...
Park Orbit monitoring must work.
Monitoring conference bridge in use would be nice also.

Configuration for FreeSWITCH to anchor SIP signalling. SIPX-
Admin GUI setting to anchor SIP signalling. SIPX-
Configuration for FreeSWITCH to anchor SIP signalling and media. SIPX-
Admin GUI setting to anchor SIP signalling and media. SIPX-
Option for SSS to get call state from FreeSWITCH. SIPX-
Admin GUI setting for SSS to get call state from FreeSWITCH. SIPX-
