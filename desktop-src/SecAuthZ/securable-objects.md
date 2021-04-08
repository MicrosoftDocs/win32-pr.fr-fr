---
description: Un objet sécurisable est un objet qui peut avoir un descripteur de sécurité.
ms.assetid: 32f2ec06-822f-4d1e-bf51-5ae1d7355e60
title: Objets sécurisables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867a40e781d9d7f97302ed6e592a7fc26d61b939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752749"
---
# <a name="securable-objects"></a>Objets sécurisables

Un objet sécurisable est un objet qui peut avoir un [descripteur de sécurité](security-descriptors.md). Tous les objets Windows nommés sont sécurisables. Certains objets sans nom, tels que les objets de [*processus*](/windows/desktop/SecGloss/p-gly) et de thread, peuvent également avoir des descripteurs de sécurité. Pour la plupart des objets sécurisables, vous pouvez spécifier le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) d’un objet dans l’appel de fonction qui crée l’objet. Par exemple, vous pouvez spécifier un descripteur de sécurité dans les fonctions [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

En outre, les fonctions de sécurité Windows vous permettent d’obtenir et de définir les informations de sécurité pour les objets sécurisables créés sur des systèmes d’exploitation autres que Windows. Les fonctions de sécurité de Windows prennent également en charge l’utilisation de descripteurs de sécurité avec des objets privés définis par l’application. Pour plus d’informations sur les objets sécurisables privés, consultez [Access Control client/serveur](client-server-access-control.md).

Chaque type d’objet sécurisable définit son propre ensemble de [droits d’accès](access-rights-and-access-masks.md) spécifiques et son propre [mappage de droits d’accès génériques](generic-access-rights.md). Pour plus d’informations sur les droits d’accès génériques et spécifiques pour chaque type d’objet sécurisable, consultez la vue d’ensemble de ce type d’objet.

Le tableau suivant présente les fonctions à utiliser pour manipuler les informations de sécurité de certains objets sécurisables communs.



| Type d'objet                                                                                                                                           | Fonctions du descripteur de sécurité                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fichiers ou répertoires](/windows/desktop/FileIO/file-security-and-access-rights) sur un système de fichiers NTFS                                                                     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Canaux nommés](/windows/desktop/ipc/named-pipe-security-and-access-rights)<br/> [Canaux anonymes](/windows/desktop/ipc/anonymous-pipe-security-and-access-rights)<br/>     | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Processus](/windows/desktop/ProcThread/process-security-and-access-rights)<br/> [Threads](/windows/desktop/ProcThread/thread-security-and-access-rights)<br/>                          | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Objets de mappage de fichiers](/windows/desktop/Memory/file-mapping-security-and-access-rights)                                                                                  | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Jetons d’accès](access-rights-for-access-token-objects.md)                                                                                           | [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity), [ **GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)                                                                             |
| Objets Window-Management ([stations](/windows/desktop/winstation/window-station-security-and-access-rights) et [postes de travail](/windows/desktop/winstation/desktop-security-and-access-rights)Windows) | [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [ **SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)                                                                                                             |
| [Clés de Registre](/windows/desktop/SysInfo/registry-key-security-and-access-rights)                                                                                         | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Services Windows](/windows/desktop/Services/service-security-and-access-rights)                                                                                           | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Imprimantes locales ou distantes                                                                                                                              | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Partages réseau                                                                                                                                        | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objets de synchronisation interprocessus](/windows/desktop/Sync/synchronization-object-security-and-access-rights) (événements, mutex, sémaphores et minuteurs attendus)     | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| [Objets de traitement](/windows/desktop/ProcThread/job-object-security-and-access-rights)                                                                                             | [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo), [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) |
| Objets de service d’annuaire                                                                                                                             | Ces objets sont gérés par des objets Active Directory. Pour plus d’informations, consultez [Active Directory interfaces de service](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).                             |



 

 

