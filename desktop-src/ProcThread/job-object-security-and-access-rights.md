---
description: le modèle de sécurité Microsoft Windows vous permet de contrôler l’accès aux objets de travail. Pour plus d’informations sur la sécurité, consultez Access-Control modèle.
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: Sécurité de l’objet de travail et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62111a630b5fd8ee4639505bedec192155f3775f4c284ff1455b8eea63d21d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978499"
---
# <a name="job-object-security-and-access-rights"></a>Sécurité de l’objet de travail et droits d’accès

le modèle de sécurité Microsoft Windows vous permet de contrôler l’accès aux objets de travail. Pour plus d’informations sur la sécurité, consultez [modèle de contrôle d’accès](../secauthz/access-control-model.md).

Vous pouvez spécifier un [descripteur de sécurité](../secauthz/security-descriptors.md) pour un objet de traitement lorsque vous appelez la fonction [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Si vous spécifiez NULL, l’objet de traitement obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans le descripteur de sécurité par défaut pour un objet de traitement proviennent du jeton principal ou d’emprunt d’identité du créateur.

Pour obtenir ou définir le descripteur de sécurité d’un objet de traitement, appelez la fonction [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa), [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa), [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)ou [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) .

Les droits d’accès valides pour les objets de travail incluent les droits d' [accès standard](../secauthz/standard-access-rights.md) et certains droits d’accès spécifiques aux travaux. Le tableau suivant répertorie les droits d’accès standard utilisés par tous les objets.

| Valeur                           | Signification                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Supprimer** (0x00010000L)        | Requis pour supprimer l’objet.                                                                                                                                                                                                                                                           |
| **Lecture \_ CONTRÔLE** (0x00020000L) | Requis pour lire les informations dans le descripteur de sécurité de l’objet, à l’exclusion des informations contenues dans la liste SACL. Pour lire ou écrire dans la liste SACL, vous devez demander le droit d’accès à la **\_ \_ sécurité du système Access** . Pour plus d’informations, consultez [droit d’accès SACL](../secauthz/sacl-access-right.md). |
| **Synchroniser** (0x00100000L)   | Droit d'utiliser l'objet pour la synchronisation. Cela permet à un thread d’attendre jusqu’à ce que l’objet soit dans l’état signalé.                                                                                                                                                                |
| **Écriture \_ DAC** (0x00040000L)    | Requis pour modifier la liste DACL dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                                   |
| **Écriture \_ PROPRIÉTAIRE** (0x00080000L)  | Requis pour modifier le propriétaire dans le descripteur de sécurité de l’objet.                                                                                                                                                                                                                  |



 

Le tableau suivant répertorie les droits d’accès spécifiques aux travaux.



| Valeur                                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Travail \_ \_Tous les \_ accès à l’objet** (0x1F001F)             | Combine tous les droits d’accès aux objets de travail valides.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Travail \_ \_ \_ Processus d’attribution d’objet** (0x0001)           | Requis pour appeler la fonction [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) pour assigner des processus à l’objet de traitement.                                                                                                                                                                                                                                                                                                                                                                |
| **Travail \_ \_Requête d’objet** (0x0004)                     | Requis pour récupérer certaines informations sur un objet de traitement, telles que les attributs et les informations de comptabilité (consultez [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) et [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)).                                                                                                                                                                                                                                                                    |
| **Travail \_ \_ \_ Attributs du jeu d’objets** (0x0002)           | Obligatoire pour appeler la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) afin de définir les attributs de l’objet de traitement.                                                                                                                                                                                                                                                                                                                                                                |
| **Travail \_ \_Attributs de \_ sécurité \_ du jeu d’objets** (0x0010) | Cet indicateur n’est pas pris en charge. Vous devez définir des limites de sécurité individuellement pour chaque processus associé à un objet de traitement. **Windows Server 2003 et Windows XP :** Requis pour appeler la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) avec la classe d’informations **JobObjectSecurityLimitInformation** pour définir des limitations de sécurité pour les processus associés à l’objet de traitement. la prise en charge de cet indicateur a été supprimée dans Windows Vista et Windows Server 2008. <br/> |
| **Travail \_ \_Fin** de l’objet (0x0008)                 | Requis pour appeler la fonction [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) pour mettre fin à tous les processus de l’objet de traitement.                                                                                                                                                                                                                                                                                                                                                                     |



 

Le handle retourné par [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) possède un accès à l’objet de travail pour **\_ \_ tous les \_** accès à l’objet de traitement. Lorsque vous appelez la fonction [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet. Si un objet de traitement se trouve dans une hiérarchie de [travaux imbriqués](nested-jobs.md), un appelant ayant accès à l’objet de travail a implicitement accès à toutes ses tâches enfants dans la hiérarchie.

Vous pouvez demander le droit accès à la **\_ \_ sécurité du système d’accès** à un objet de traitement si vous souhaitez lire ou écrire la liste SACL de l’objet. Pour plus d’informations, consultez [listes de contrôle d’accès (ACL)](../secauthz/access-control-lists.md) et [droit d’accès SACL](../secauthz/sacl-access-right.md).

Vous devez définir des limitations de sécurité individuellement pour chaque processus associé à un objet de traitement, plutôt que de les définir pour l’objet de traitement lui-même. Pour plus d’informations, consultez [sécurité des processus et droits d’accès](process-security-and-access-rights.md).

**Windows Server 2003 et Windows XP :** Vous pouvez utiliser la fonction [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) pour définir des limites de sécurité pour l’objet de traitement. cette fonctionnalité a été supprimée dans Windows Vista et Windows Server 2008.

 

 
