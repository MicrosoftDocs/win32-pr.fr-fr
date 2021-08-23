---
description: le modèle de sécurité Windows vous permet de contrôler l’accès aux objets event, mutex, semaphore et timer waitable. Les files d’attente du minuteur, les variables interbloquées et les objets de section critique ne sont pas sécurisables. Pour plus d’informations, consultez Access-Control modèle.
ms.assetid: 92478298-617c-4672-a1cc-9a8e9af40327
title: Sécurité de l’objet de synchronisation et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85ca76002a92e305983ab97d46dfde2f36f9ae49a779e091a072d3090ceb976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739289"
---
# <a name="synchronization-object-security-and-access-rights"></a>Sécurité de l’objet de synchronisation et droits d’accès

le modèle de sécurité Windows vous permet de contrôler l’accès aux objets event, mutex, semaphore et timer waitable. Les files d’attente du minuteur, les variables interbloquées et les objets de section critique ne sont pas sécurisables. Pour plus d’informations, consultez [modèle de contrôle d’accès](../secauthz/access-control-model.md).

Vous pouvez spécifier un [descripteur de sécurité](../secauthz/security-descriptors.md) pour un objet de synchronisation interprocessus lorsque vous appelez la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Si vous spécifiez **null**, l’objet obtient un descripteur de sécurité par défaut. Les [listes de contrôle d’accès (ACL)](../secauthz/access-control-lists.md) dans le descripteur de sécurité par défaut pour un objet de synchronisation proviennent du jeton principal ou d’emprunt d’identité du créateur.

Pour récupérer ou définir le descripteur de sécurité d’un événement, d’un mutex, d’un sémaphore ou d’un objet de minuteur qui peut être attendu, appelez les fonctions [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Les handles retournés par [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)et [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ont un accès complet au nouvel objet. Lorsque vous appelez les fonctions [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)et [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet.

Les droits d’accès valides pour les objets de synchronisation interprocessus incluent les [droits d’accès standard](../secauthz/standard-access-rights.md) et certains droits d’accès spécifiques aux objets. Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.

| Valeur                           | Signification                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Supprimer** (0x00010000L)        | Requis pour supprimer l’objet.                                                                                                                                                                                                                                                           |
| **Lecture \_ CONTRÔLE** (0x00020000L) | Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL. Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la **\_ \_ sécurité du système Access** . Pour plus d’informations, consultez [droit d’accès SACL](../secauthz/sacl-access-right.md). |
| **Synchroniser** (0x00100000L)   | Droit d'utiliser l'objet pour la synchronisation. Cela permet à un thread d’attendre jusqu’à ce que l’objet soit dans l’état signalé.                                                                                                                                                                |
| **Écriture \_ DAC** (0x00040000L)    | Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                                   |
| **Écriture \_ PROPRIÉTAIRE** (0x00080000L)  | Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                                  |



 

Le tableau suivant répertorie les droits d’accès spécifiques à l’objet pour les objets d’événement. Ces droits sont pris en charge en plus des droits d’accès standard.



| Valeur                             | Signification                                                                                                                                                                                                                                                                                          |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Événement \_ TOUT \_ accès** (0x1F0003) | Tous les droits d’accès possibles pour un objet d’événement. Utilisez ce droit uniquement si votre application nécessite un accès au-delà de ce qui est accordé par les droits d’accès standard et l' **\_ \_ État de modification d’événement**. L’utilisation de ce droit d’accès augmente la possibilité que votre application soit exécutée par un administrateur. |
| **Événement \_ \_État de modification** (0x0002) | Modifiez l’accès à l’État, qui est requis pour les fonctions [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-setevent), [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) et [**PulseEvent n'**](/windows/desktop/api/WinBase/nf-winbase-pulseevent) .                                                                                                                                    |



 

Le tableau suivant répertorie les droits d’accès spécifiques aux objets pour les objets mutex. Ces droits sont pris en charge en plus des droits d’accès standard.



| Valeur                             | Signification                                                                                                                                                                                                                                                            |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MUTEX \_ TOUT \_ accès** (0x1F0001) | Tous les droits d’accès possibles pour un objet Mutex. Utilisez ce droit uniquement si votre application nécessite un accès au-delà de ce qui est accordé par les droits d’accès standard. L’utilisation de ce droit d’accès augmente la possibilité que votre application soit exécutée par un administrateur. |
| **MUTEX \_ \_État de modification** (0x0001) | Réservé pour un usage futur.                                                                                                                                                                                                                                           |



 

Le tableau suivant répertorie les droits d’accès spécifiques à l’objet pour les objets Semaphore. Ces droits sont pris en charge en plus des droits d’accès standard.



| Valeur                                 | Signification                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sémaphore \_ TOUT \_ accès** (0x1F0003) | Tous les droits d’accès possibles pour un objet Semaphore. Utilisez ce droit uniquement si votre application nécessite un accès au-delà de ce qui est accordé par les droits d’accès standard et l' **\_ \_ État de modification de sémaphore**. L’utilisation de ce droit d’accès augmente la possibilité que votre application soit exécutée par un administrateur. |
| **Sémaphore \_ \_État de modification** (0x0002) | Modifiez l’accès à l’État, qui est requis pour la fonction [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) .                                                                                                                                                                                                   |



 

Le tableau suivant répertorie les droits d’accès spécifiques aux objets pour les objets de minuteur qui sont attendus. Ces droits sont pris en charge en plus des droits d’accès standard.



| Valeur                             | Signification                                                                                                                                                                                                                                                                                                  |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Minuteur \_ TOUT \_ accès** (0x1F0003) | Tous les droits d’accès possibles pour un objet de minuteur qui peut être attendu. Utilisez ce droit uniquement si votre application nécessite un accès au-delà de ce qui est accordé par les droits d’accès standard et l' **\_ \_ État de modification du minuteur**. L’utilisation de ce droit d’accès augmente la possibilité que votre application soit exécutée par un administrateur. |
| **Minuteur \_ \_État de modification** (0x0002) | Modifiez l’accès à l’État, qui est requis pour les fonctions [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) et [**CancelWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-cancelwaitabletimer) .                                                                                                                                            |
| **Minuteur \_ \_État** de la requête (0x0001)  | Réservé pour un usage futur.                                                                                                                                                                                                                                                                                 |



 

Pour lire ou écrire dans la liste SACL d’un objet de synchronisation interprocessus, vous devez demander le droit d’accès à la **\_ \_ sécurité du système d’accès** . Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](../secauthz/access-control-lists.md) et [droit d’accès SACL](../secauthz/sacl-access-right.md).

 

 
