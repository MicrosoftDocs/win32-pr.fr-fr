---
description: La liste suivante répertorie les fichiers. lib requis pour compiler différentes applications TAPI 3, à partir de 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Bibliothèques requises
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538654"
---
# <a name="libraries-required"></a>Bibliothèques requises

Liste des fichiers. lib requis pour compiler différentes applications TAPI 3, à compter du 1/22/01 :

-   Advapi32. lib
-   Amstrmid. lib (GUID ActiveMovie)
-   Kernel32.lib
-   Mdhcpid. lib (GUID de multidiffusion)
-   Ole32. lib (COM)
-   Oleaut32. lib (Automation COM)
-   Rendid. lib (GUID Rendezvous)
-   Rpcndr. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Sdpblbid. lib (GUID du protocole de descripteur de session (SDP))
-   Strmiids. lib
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   Ws2 \_ 32. lib

Si vous utilisez Microsoft Visual Studio, vous devrez peut-être mettre à jour votre version. En particulier, Link.exe doit comporter une date de 3/19/98 ou une version ultérieure.

Le compilateur définit doit inclure \_ Win32 \_ winnt défini sur au moins 0x500 et \_ \_ DCOM Win32.

 

 



