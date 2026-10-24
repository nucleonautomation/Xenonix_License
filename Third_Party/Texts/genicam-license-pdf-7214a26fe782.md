# GenICam_License.pdf

[Browse libraries](../README.md) · [Repository home](../../README.md)

Original-file SHA-256: `7214a26fe782821cab04c86636db2bd02ac59c5f9cd41e3d2eef32a2b98d79ee`

Readable text transcription of the upstream document; original source locations are listed below.

## License and notices

```text
   
 
   
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
GenICam License 
 
Version 1.0 - October 9th, 2023 
 
 
 
 
 
 
 
 
 
 
Published by EUROPEAN MACHINE VISION ASSOCIATION (EMVA) 
 
© 2023 EMVA 
 
All rights reserved. 
 
No part of this publication may be reproduced in any form, in an electronic retrieval 
system or otherwise, without prior written permission of EMVA. 


EMVA GenICam License 
v1.0  Page 2 of 9          October 9th, 2023 
 
 
Table of Contents 
 
History 3 
1 Introduction 4 
2 Overview 4 
3 Rules for Standard Compliancy 5 
4 Rules for Using the Runtime Version of the Reference Implementation  7 
5 Rules for Using the Development Version of the Reference Implementation  8 
6 Rules for Redistributing SFNC or GenTL SFNC 9 
 
  

EMVA GenICam License 
v1.0  Page 3 of 9          October 9th, 2023 
 
History 
 
 
Version Date Changed by Change 
1.0 09.10.2023 Christoph Zierl, MVTec Official release based on 
Version 1.0 of the EMVA 
GenICam Working Group Rules 
 
  

EMVA GenICam License 
v1.0  Page 4 of 9          October 9th, 2023 
1 Introduction 
This document describes the GenICam license within the GenICam standard working group. Note 
that chapters 2-6 are an exact copy of the related chapters in the EMVA GenICam Working 
Group Rules document  which is p art of the “EMVA legal envelope” for the GenICam standard , 
see https://www.emva.org/standards-technology/genicam/: 
• EMVA Standards Development and Approval Procedures 
• EMVA IPR1 Policy 
• EMVA IPR Committee Rules 
• EMVA GenICam Working Group Application Form  
• EMVA GenICam Working Group Rules 
2 Overview 
The goal of GenICam is to provide a generic programming interface for cameras which is 
independent of the camera’s interface technology like GigE Vision, USB3 Vision, CoaXPress, 
Camera Link HS, CSI2 or  else. GenICam requires that cameras have a low level, register based 
programming interface, and that interface standards define a protocol for accessing these 
registers. All modern interface standards follow this scheme. 
GenICam Modules 
The GenICam standard consists of several modules according to the main tasks to be solved: 
 
• GenApi: standardizes the format of a XML based device description file which describes 
how to map high level feature access (e.g. Camera.Gain = 42) by the user to low level 
register accesses (e.g. Camera.WriteReg(0xff1234, 0x2A, 2)). 
 
• SFNC (Standard Features Naming Convention): standardizes names, types, and behavior 
for the most common device features resu lting in a plug&play -like interoperability 
between products from different vendors. Part of the SFNC is also the PFNC (Pixel Format 
Naming Convention) which standardizes the memory layout of video data. 
 
• CLProtocol: standardizes the interface of an adapter  DLL to permit interfacing Camera 
Link cameras with GenICam. 
 
• FWUpdate: standardizes the firmware update process for devices using GenApi. 
 
• GenTL: standardizes a generic programming interface for transport layers, which defines 
the enumeration, control and data acquisition of cameras. This interface allows 
combining drivers and image processing libraries from different vendors. 
 
 
1 IPR: Intellectual Property Rights 

EMVA GenICam License 
v1.0  Page 5 of 9          October 9th, 2023 
• GenTL SFNC : standardizes names, types, and behavior for common features of the 
transport layer interface. 
 
• GenCP (Generic Control Protocol): standardizes a generic packet -based protocol for 
controlling cameras. It is used to simplify the definition and implementation of new 
transport layer standards.  
 
• GenDC  (Generic Data Container): standardizes a portable generic data container (GenDC) 
format. This allows devices to send any form of data in a Transport Layer Protocol (TLP) 
independent format and permits to share a common data container format for all the TLP 
standards. 
 
Reference Implementation 
The GenICam working group also provides a reference implementation for the GenApi module. 
The reference implementation is a collection of software modules which can be distributed in 
two ways: as runtime version or as development version, see Chapters 4 and 5 for more details 
about using and redistributing the reference implementation. 
The runtime as well as the development version may contain 3rd party modules which come with 
their own license. These licenses override the GenICam license. 
Note that GenICam is a B2B industry standard which is mostly used by vendors “under the hood” 
to provide interoperability between their products. As a consequence of this, the reference 
implementation does not contain any driver and thus cannot be used stand -alone to control a 
camera. 
 
3 Rules for Standard Compliancy 
The standard documents are available for free to anybody. Users may download the 
latest version of the standard documents from the GenICam website at 
www.genica m.org .  
Regarding compliancy, the GenICam standard has been divided into four parts:  
• GenICam (mainly the modules GenApi and SFNC)  
• GenICam TL (mainly the modules GenTL and GenTL SFNC)  
• GenICam CP (mainly the module GenCP)  
• GenICam DC (mainly the module GenDC)  
While the compliancy rules for GenICam (i.e, the modules GenApi and SFNC) are always 
valid, the compliancy rules for GenICam TL, GenICam CP and GenICam DC are only valid 
if applicable.  
 

EMVA GenICam License 
v1.0  Page 6 of 9          October 9th, 2023 
GenICam Compliancy 
The term GenICam compliant  is true for:  
• Cameras (or other devices) providing a GenICam compliant XML based device 
description file and obeying the standard’s additional rules. In particular, it must 
follow the GenICam Standard Features Naming Convention (S FNC), whenever 
applicable or possible.  
• Software libraries being able to access GenICam compliant devices.  
GenICam TL Compliancy 
The term GenICam TL compliant is true for: 
 
• Products that provide a transport layer interface compatible with the definitions of  the 
GenTL and the GenTL SFNC modules ("GenICam GenTL Producers"). 
 
• Products that can access devices via a GenICam GenTL Producer based on the definitions 
of the GenTL and the GenTL SFNC modules ("GenICam GenTL Consumers") 
GenICam CP Compliancy 
The term GenICam CP compliant is true for: 
 
• Cameras (or other devices) that support the generic packet -based protocol and provide 
the bootstrap register map as defined in the GenICam GenCP standard. 
  
• Products that can access devices via the generic packet -based prot ocol and bootstrap 
register map as defined in the GenICam GenCP standard. 
GenICam DC Compliancy 
The term GenICam DC compliant is true for: 
 
• Products that create, transmit, receive, deliver or store GenDC containers as defined in 
the GenICam GenDC standard  which meet  the requirements given in the "List of 
Requirements and Objectives" and respect the related text in the GenDC specification. 
 
Certification and Logo 
In general, the GenICam compliancy is declared by self-certification. The GenICam working group 
can provide additional checklists or certification software that have to be used during the self -
certification procedure. Vendors may use the GenICam logo(s) and use the name GenICamTM for 
advertising GenICam compliant products. In future, additional compliancy procedures may 
become mandatory for new devices such as validation test suites and/or obligations to 
participate at plug-fests. 
 
 

EMVA GenICam License 
v1.0  Page 7 of 9          October 9th, 2023 
4 Rules for Using the Runtime Version of the Reference 
Implementation 
 
The runtime version of the reference implementation is available for free to anybody in binary 
format. 
Everyone may download the latest version from the GenICam website.  
 
The runtime ver sion is distributed under a modified BSD License (the term source code below 
refers to the header files delivered with the runtime version):  
Copyright (c) 2005-<year>, <owner of the software module> 
All rights reserved. 
Redistribution and use in source and binary forms, without2 modification, are permitted 
provided that the following conditions are met: 
▪ Redistributions of source code must retain the above copyright notice, this list of 
conditions and the following disclaimer.  
▪ Redistributions in binary form must reproduce the abo ve copyright notice, this list of 
conditions and the following disclaimer in the documentation and/or other materials 
provided with the distribution.  
▪ Neither the name of the GenICam standard group nor the names of its contributors may 
be used to endorse or promote products derived from this software without specific prior 
written permission. 
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" 
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE 
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE 
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL 
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR 
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER 
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR 
TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF 
THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. 
In contrast to the BSD License the user must not modify the software except the installation 
procedure, see Chapter 5 for more details. This is to make sure only properly tested and released 
GenICam versions are used in the machine vision community and the support effort is restricted. 
 
 
 
2 The original BSD License reads here “with or without modification”. 

EMVA GenICam License 
v1.0  Page 8 of 9          October 9th, 2023 
5 Rules for Using the Development Version of the Reference 
Implementation 
 
In order to get access to the development version of the GenICam reference implementation a 
company must become GenICam Working Group member. Application requires the completion 
and submission of the EMVA GenICam Working Group Application Form which can be  found on 
www.genicam.org. 
 
GenICam Working Group members get, inter alia, the following benefits:  
 
• Access to code repository, which allows GenICam Working Group members to download 
the source code of the development version of the GenICam reference implementation 
and use it for debugging. 
• Access to GenICam Working Group meetings and the GenICam mailing list. 
• Technical support from the GenICam community through the GenICam mailing list. 
• The company name is listed on the GenICam website as a GenICam Working Group 
member. 
 
By registering, the company accepts in particular, without limitation, the following obligations: 
 
• It must not give the source code of the development version of the GenICam reference 
implementation to any 3rd party. 
• All bug fixes and all changes regarding unsupported platforms and compilers (for which 
no official binaries exist yet) shall be submitted to the respective GenICam module 
maintainers for reviewing and testing. Once the code change is in the code repository, 
private builds can be made using the repository code, provided that the official way to 
create a private namespace and private binary names is used. Additionally, the self-
generated release must clearly indicate the snapshot version used and state that it is not 
an official release. 
• Custom builds of the unmodified source of the GenICam reference implementation may 
be re-distributed in binary format only by GenICam Working Group member companies, 
provided that they follow the official mechanism for utilizing private binary names, 
namespaces, and indicate the repository snapshot version of the source code. 
• It must submit improvements to the GenICam Working Group which will validate them 
and add them to the next GenICam release in reasonable time. 
• For details about the handling of intellectual property please see the EMVA GenICam 
Working Group Application Form. 
• Working group members are charged a reasonable admin fee in order to meet the 
EMVA’s cost for hosting the GenICam standard. 
 

EMVA GenICam License 
v1.0  Page 9 of 9          October 9th, 2023 
 
6 Rules for Redistributing SFNC or GenTL SFNC  
 
Redistributing (parts of) SFNC or GenTL SFNC without modification, addition or interpretation, is 
allowed as long as it is clearly stated that this is a copy of the GenICam (GenTL) SFNC standard 
document version <x.y> that can be found at www.genicam.org.
```

## Where this notice appears

- [genicam 1.6.0](../Libraries/genicam/1.6.0/README.md) — `genicam-1.6.0/linux-arm64/genicam-1.6.0.data/purelib/genicam/licenses/GenICam_License.pdf`
- [genicam 1.6.0](../Libraries/genicam/1.6.0/README.md) — `genicam-1.6.0/linux-amd64/genicam-1.6.0.data/purelib/genicam/licenses/GenICam_License.pdf`
- [genicam 1.6.0](../Libraries/genicam/1.6.0/README.md) — `genicam-1.6.0/windows/genicam-1.6.0.data/purelib/genicam/licenses/GenICam_License.pdf`
