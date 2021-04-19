---
description: Explique l’utilisation des jetons d’emprunt d’identité dans le contrôle d’accès.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Jetons d’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524408"
---
# <a name="impersonation-tokens"></a>Jetons d’emprunt d’identité

Un thread d’emprunt d’identité a deux [*jetons d’accès*](/windows/desktop/SecGloss/a-gly):

-   [*Jeton d’accès principal*](/windows/desktop/SecGloss/p-gly) qui décrit le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du serveur. Pour obtenir un descripteur de ce jeton, appelez la fonction [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .
-   Un jeton d’accès d’emprunt d’identité qui décrit le contexte de sécurité du client dont l’identité est empruntée. Pour obtenir un descripteur de ce jeton, appelez la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .

Un serveur peut utiliser le [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly) dans les fonctions suivantes :

-   Dans les fonctions [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)et [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) pour déterminer si un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) permet au client un ensemble de droits d’accès.
-   Dans la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer ou désactiver les privilèges du client.
-   Dans la fonction [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) pour déterminer si un jeu de privilèges est activé dans le jeton du client.
-   Dans les fonctions qui génèrent des entrées dans le journal des événements de sécurité, telles que [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) ou [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Ces fonctions utilisent un jeton d’emprunt d’identité pour obtenir des informations sur le client pour l’entrée de journal.

 

 
