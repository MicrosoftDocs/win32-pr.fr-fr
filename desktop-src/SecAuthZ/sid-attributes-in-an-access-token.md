---
description: Chaque identificateur de sécurité (SID) d’utilisateur et de groupe dans un jeton d’accès possède un ensemble d’attributs qui contrôlent la façon dont le système utilise le SID dans une vérification d’accès. Le tableau suivant répertorie les attributs qui contrôlent la vérification de l’accès.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Attributs SID dans un jeton d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe504e190e6d6e884b8068eb23983b2bc506c7c8447a8db77fd3ddb9cdfb917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413419"
---
# <a name="sid-attributes-in-an-access-token"></a>Attributs SID dans un jeton d’accès

Chaque [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) d’utilisateur et de groupe dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) possède un ensemble d’attributs qui contrôlent la façon dont le système utilise le SID dans une vérification d’accès. Le tableau suivant répertorie les attributs qui contrôlent la vérification de l’accès.



| Attribut                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_ GROUPE \_ activé              | Un SID avec cet attribut est activé pour les vérifications d’accès. Lorsque le système effectue une vérification d’accès, il recherche les [*entrées de contrôle*](/windows/desktop/SecGloss/a-gly) d’accès (ACE) autorisées et refusées d’accès qui s’appliquent à l’un des SID activés dans le jeton d’accès. un SID sans cet attribut est ignoré au cours d’une vérification d’accès, à moins que l' \_ attribut SE groupe n' \_ \_ \_ est défini pour l’option refuser \_ uniquement.<br/> |
| SE \_ \_utilisation \_ de groupe pour \_ Deny \_ uniquement | Un SID avec cet attribut est un SID en refus seul. Lorsque le système effectue une vérification d’accès, il recherche les ACE avec accès refusé qui s’appliquent au SID, mais ignore les entrées de contrôle d’accès (ACE) autorisées pour le SID. si cet attribut est défini, l' \_ attribut SE activé du groupe \_ n’est pas défini et le SID ne peut pas être réactivé.<br/>                                                                                                                                                          |



 

pour définir ou désélectionner l' \_ attribut SE groupe \_ activé d’un SID de groupe, utilisez la fonction [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) . vous ne pouvez pas désactiver un SID de groupe avec \_ l' \_ attribut obligatoire groupe SE. Vous ne pouvez pas utiliser **AdjustTokenGroups** pour désactiver le SID de l’utilisateur d’un jeton d’accès.

pour déterminer si un SID est activé dans un jeton, c’est-à-dire s’il a l’attribut SE activé pour le \_ groupe \_ , appelez la fonction [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) .

pour définir l' \_ attribut SE \_ groupe \_ pour \_ refuser \_ uniquement d’un sid, incluez le sid dans la liste des sid de refus uniquement que vous spécifiez lorsque vous appelez la fonction [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . **CreateRestrictedToken** peut appliquer \_ \_ \_ à n’importe quel sid l’utilisation du groupe SE pour \_ \_ un attribut DENY uniquement, y compris les sid d’utilisateur et de groupe qui ont l' \_ attribut SE group \_ obligatoire. toutefois, vous ne pouvez pas supprimer l’attribut de refus uniquement d’un sid, et vous ne pouvez pas utiliser [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) pour définir l’attribut de groupe de SE \_ \_ activé sur un sid en refus seul.

Pour obtenir les attributs d’un SID, appelez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) avec la valeur tokenGroups. La fonction retourne un tableau de structures [**sid \_ et d' \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) qui identifient les SID de groupe et leurs attributs.

 

