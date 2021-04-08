---
description: Chaque identificateur de sécurité (SID) d’utilisateur et de groupe dans un jeton d’accès possède un ensemble d’attributs qui contrôlent la façon dont le système utilise le SID dans une vérification d’accès. Le tableau suivant répertorie les attributs qui contrôlent la vérification de l’accès.
ms.assetid: c902f876-f05e-4b0c-ab65-a0c6cebca933
title: Attributs SID dans un jeton d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a93e180c8c6ffe03a26591d5b9f722c2266356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752741"
---
# <a name="sid-attributes-in-an-access-token"></a>Attributs SID dans un jeton d’accès

Chaque [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) d’utilisateur et de groupe dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) possède un ensemble d’attributs qui contrôlent la façon dont le système utilise le SID dans une vérification d’accès. Le tableau suivant répertorie les attributs qui contrôlent la vérification de l’accès.



| Attribut                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Groupe de SE \_ \_ activé              | Un SID avec cet attribut est activé pour les vérifications d’accès. Lorsque le système effectue une vérification d’accès, il recherche les [*entrées de contrôle*](/windows/desktop/SecGloss/a-gly) d’accès (ACE) autorisées et refusées d’accès qui s’appliquent à l’un des SID activés dans le jeton d’accès. Un SID sans cet attribut est ignoré lors d’une vérification d’accès, sauf si le \_ groupe \_ de se utilisé \_ pour l' \_ attribut de refus \_ seul est défini.<br/> |
| \_ \_ utilisation d’un groupe de se \_ pour \_ Deny \_ uniquement | Un SID avec cet attribut est un SID en refus seul. Lorsque le système effectue une vérification d’accès, il recherche les ACE avec accès refusé qui s’appliquent au SID, mais ignore les entrées de contrôle d’accès (ACE) autorisées pour le SID. Si cet attribut est défini, l' \_ attribut activé du groupe se \_ n’est pas défini et le SID ne peut pas être réactivé.<br/>                                                                                                                                                          |



 

Pour activer ou désactiver l' \_ attribut groupe \_ de se activé d’un SID de groupe, utilisez la fonction [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) . Vous ne pouvez pas désactiver un SID de groupe avec \_ l' \_ attribut obligatoire groupe se. Vous ne pouvez pas utiliser **AdjustTokenGroups** pour désactiver le SID de l’utilisateur d’un jeton d’accès.

Pour déterminer si un SID est activé dans un jeton, c’est-à-dire s’il a l' \_ attribut activé pour le groupe se \_ , appelez la fonction [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) .

Pour définir l' \_ attribut utiliser le groupe de se \_ \_ pour \_ refuser \_ uniquement d’un SID, incluez le SID dans la liste des SID de refus uniquement que vous spécifiez lorsque vous appelez la fonction [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . **CreateRestrictedToken** peut appliquer le \_ groupe \_ de se utiliser pour l' \_ \_ \_ attribut refuser uniquement à n’importe quel sid, y compris les SID d’utilisateur et de groupe qui ont l' \_ \_ attribut obligatoire groupe se. Toutefois, vous ne pouvez pas supprimer l’attribut de refus uniquement d’un SID, et vous ne pouvez pas utiliser [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups) pour définir l’attribut de groupe de se \_ \_ activé sur un SID en refus seul.

Pour obtenir les attributs d’un SID, appelez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) avec la valeur tokenGroups. La fonction retourne un tableau de structures [**sid \_ et d' \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) qui identifient les SID de groupe et leurs attributs.

 

