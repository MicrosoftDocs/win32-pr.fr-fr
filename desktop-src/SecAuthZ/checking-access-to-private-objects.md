---
description: Une application serveur protégée doit vérifier les droits d’accès des clients avant d’autoriser le client à accéder à un objet privé protégé.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Vérification de l’accès aux objets privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951258"
---
# <a name="checking-access-to-private-objects"></a>Vérification de l’accès aux objets privés

Une application serveur protégée doit vérifier les droits d’accès d’un client avant d’autoriser le client à accéder à un objet privé protégé. Pour ce faire, le serveur passe un [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly), un descripteur de sécurité et un ensemble de droits d’accès demandés à [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste DACL [*du descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifient les droits d’accès accordés ou refusés à différents destinataires. La fonction **AccessCheck** compare le tiers de confiance de chaque ACE aux tiers de confiance identifiés dans le jeton d’emprunt d’identité. Pour obtenir une description de l’algorithme utilisé pour accorder ou refuser l’accès, voir [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md).

La fonction [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) effectue une vérification d’accès similaire. En outre, il génère des enregistrements d’audit dans le journal des événements de sécurité en fonction de la liste SACL dans le descripteur de sécurité.

Les fonctions [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) et [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) sont similaires à [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) et [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , à ceci près qu’elles vous permettent de vérifier l’accès aux sous-objets d’un objet, comme les jeux de propriétés ou les propriétés. Les fonctions [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) et [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) sont également similaires à **AccessCheck** , à ceci près qu’elles fournissent les résultats de la vérification d’accès pour chaque sous-objet dans une hiérarchie des propriétés et jeux de propriétés de l’objet. Ces fonctions utilisent la structure de la [**\_ \_ liste de types**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) d’objets pour décrire la hiérarchie des objets pour lesquels l’accès est vérifié. Les fonctions qui génèrent un message d’audit utilisent le type d’énumération de [**\_ \_ type d’événement audit**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) pour indiquer si l’objet en cours de vérification est un objet de service d’annuaire. Pour plus d’informations sur la hiérarchie d’un objet et de ses sous-objets, consultez [ACE pour contrôler l’accès aux propriétés d’un objet](aces-to-control-access-to-an-object-s-properties.md).

Les droits d’accès demandés passés aux fonctions [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) et [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) ne doivent pas inclure de [droits d’accès génériques](generic-access-rights.md). Le serveur peut utiliser la fonction [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) pour convertir tous les droits d’accès génériques en autorisations standard et spécifiques correspondantes selon le mappage spécifié dans la structure de [**\_ mappage générique**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

Les fonctions [**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) et [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) comparent un [*masque d’accès*](/windows/desktop/SecGloss/a-gly) demandé avec un masque d’accès accordé.

Pour obtenir un exemple de code qui utilise la fonction [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , consultez [vérification de l’accès client avec les ACL en C++](verifying-client-access-with-acls-in-c--.md).

La fonction [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) crée et retourne un descripteur de sécurité dans un format qui autorise la propagation automatique des ACE pouvant être héritées. Ce descripteur de sécurité contient toutes les ACE, héritées et non héritées, dans le descripteur de sécurité actuel et se trouve dans [*un format auto-relatif*](/windows/desktop/SecGloss/s-gly) . La fonction **ConvertToAutoInheritPrivateObjectSecurity** détermine si les ACE sont héritées ou non héritées en comparant toutes les entrées du descripteur de sécurité actuelles avec toutes les entrées du descripteur de sécurité parent. Il se peut qu’il n’existe pas de correspondance un-à-un entre les deux groupes d’ACE. Par exemple, une entrée du contrôle d’accès qui autorise l’autorisation de lecture/écriture peut être équivalente à deux ACE : une entrée du contrôle d’accès qui autorise l’autorisation de lecture et une entrée de contrôle d’accès qui autorise l’autorisation d’écriture. Un descripteur de sécurité parent ne peut pas être fourni lorsque le descripteur de sécurité actuel est le parent.

 

 
