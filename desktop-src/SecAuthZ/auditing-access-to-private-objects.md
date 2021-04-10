---
description: Un serveur protégé peut utiliser les fonctions suivantes pour générer des rapports d’audit dans le journal des événements de sécurité.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Audit de l’accès aux objets privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953162"
---
# <a name="auditing-access-to-private-objects"></a>Audit de l’accès aux objets privés

Un serveur protégé peut utiliser les fonctions suivantes pour générer des rapports d’audit dans le journal des événements de sécurité.



| Fonction                                                                                                     | Description                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Identique à la fonction [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , sauf qu’elle peut générer des messages d’audit pour les tentatives d’accès ayant échoué ou réussi.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Identique à la fonction [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) , sauf qu’elle peut générer des messages d’audit pour les tentatives d’accès ayant échoué ou réussi.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Identique à la fonction [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , sauf qu’elle peut générer des messages d’audit pour les tentatives d’accès ayant échoué ou réussi.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Identique à la fonction [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) , sauf qu’elle permet au thread appelant d’effectuer la vérification d’accès avant d’emprunter l’identité du client. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Génère un message d’audit pour indiquer qu’un client a tenté de fermer un objet privé.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Génère un message d’audit pour indiquer qu’un client a tenté de supprimer un objet privé.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Génère un message d’audit pour indiquer qu’un client a tenté d’ouvrir ou de créer un objet privé.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Génère un message d’audit pour indiquer qu’un client a tenté d’utiliser un jeu de privilèges spécifié conjointement à une tentative d’accès à un objet privé.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Génère un message d’audit pour indiquer qu’un client a tenté d’utiliser un jeu de privilèges spécifié.                                                                                                                        |



 

 

 
