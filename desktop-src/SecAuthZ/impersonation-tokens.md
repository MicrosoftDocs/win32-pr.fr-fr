---
description: Explique l’utilisation des jetons d’emprunt d’identité dans le contrôle d’accès.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Jetons d’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67acf48a1f274703850fc8bfc2167014708124c46743f416591510b6c9ab559b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908139"
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

 

 
