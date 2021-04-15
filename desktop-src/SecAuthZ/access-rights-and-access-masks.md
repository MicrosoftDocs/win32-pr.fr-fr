---
description: Un droit d’accès est un indicateur binaire qui correspond à un ensemble particulier d’opérations qu’un thread peut effectuer sur un objet sécurisable.
ms.assetid: da67c486-d2e7-4632-ac7a-c18aabc3f21d
title: Droits d’accès et masques d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f06cdf447f9d91c1553ea5fb6b3b7d1f324dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393656"
---
# <a name="access-rights-and-access-masks"></a>Droits d’accès et masques d’accès

Un *droit d’accès* est un indicateur binaire qui correspond à un ensemble particulier d’opérations qu’un thread peut effectuer sur un objet sécurisable. Par exemple, une clé de registre a le \_ \_ droit d’accès à la valeur de jeu de clés, qui correspond à la capacité d’un thread à définir une valeur sous la clé. Si un thread essaie d’exécuter une opération sur un objet, mais n’a pas le droit d’accès nécessaire à l’objet, le système n’effectue pas l’opération.

Un [*masque d’accès*](/windows/desktop/SecGloss/a-gly) est une valeur 32 bits dont les bits correspondent aux droits d’accès pris en charge par un objet. Tous les objets sécurisables Windows utilisent un [format de masque d’accès](access-mask-format.md) qui comprend des bits pour les types suivants de droits d’accès :

-   [Droits d’accès génériques](generic-access-rights.md)
-   [Droits d’accès standard](standard-access-rights.md)
-   [Droit d’accès SACL](sacl-access-right.md)
-   [Droits d’accès aux services d’annuaire](directory-services-access-rights.md)

Quand un thread tente d’ouvrir un handle vers un objet, le thread spécifie généralement un masque d’accès pour [demander un jeu de droits d’accès](requesting-access-rights-to-an-object.md). Par exemple, une application qui doit définir et interroger les valeurs d’une clé de Registre peut ouvrir la clé à l’aide d’un masque d’accès pour demander la valeur du jeu de clés et les droits d’accès à la \_ valeur de requête de \_ clé \_ \_ .

Le tableau suivant présente les fonctions qui manipulent les informations de sécurité pour chaque type d’objet sécurisable.



| Type d'objet                                                                                                                                           | Fonctions du descripteur de sécurité                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fichiers ou répertoires](/windows/desktop/FileIO/file-security-and-access-rights) sur un système de fichiers NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Canaux [nommés](/windows/desktop/ipc/named-pipe-security-and-access-rights)canaux[anonymes](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>                 | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| Mémoires tampons d’écran de la console                                                                                                                                | Non pris en charge.                                                                                                                                                                                     |
| [Traite](/windows/desktop/ProcThread/process-security-and-access-rights)les[Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                                      | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objets de mappage de fichiers](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Jetons d’accès](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objets Window-Management ([stations](/windows/desktop/winstation/window-station-security-and-access-rights) et [postes de travail](/windows/desktop/winstation/desktop-security-and-access-rights)Windows) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Clés de Registre](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Services Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Imprimantes locales ou distantes                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Partages réseau                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objets de synchronisation interprocessus](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (événements, mutex, sémaphores et minuteurs attendus)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objets de traitement](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |



 

 

