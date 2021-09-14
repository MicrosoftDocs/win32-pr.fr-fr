---
description: Un tiers de confiance est le compte d’utilisateur, le compte de groupe ou la session à laquelle une entrée de contrôle d’accès (ACE) s’applique. Chaque ACE d’une liste de contrôle d’accès (ACL) a un identificateur de sécurité (SID) qui identifie un tiers de confiance.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Confiance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222428"
---
# <a name="trustees"></a>Confiance

Un tiers de confiance est le compte d’utilisateur, le compte de groupe ou la [*session*](/windows/desktop/SecGloss/l-gly) à laquelle une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) s’applique. Chaque ACE d’une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) a un [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui identifie un tiers de confiance.

les comptes d’utilisateur incluent les comptes que les utilisateurs ou les programmes humains, tels que les Services Windows utilisent pour se connecter à l’ordinateur local.

Les comptes de groupe ne peuvent pas être utilisés pour ouvrir une session sur un ordinateur, mais ils sont utiles dans les ACE pour autoriser ou refuser un ensemble de droits d’accès à un ou plusieurs comptes d’utilisateur.

Un [*SID d’ouverture*](/windows/desktop/SecGloss/l-gly) de session qui identifie la session d’ouverture de session active est utile pour autoriser ou refuser des droits d’accès uniquement jusqu’à ce que l’utilisateur se déconnecte.

Les fonctions de contrôle d’accès utilisent la structure de [**tiers de confiance**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) pour identifier un tiers de confiance. La structure du **tiers de confiance** vous permet d’utiliser une chaîne de nom ou un SID pour identifier un tiers de confiance. Si vous utilisez un nom, les fonctions qui créent une entrée du contrôle d’accès à partir de la structure du **tiers de confiance** effectuent la tâche d’allocation des tampons sid et de recherche du SID qui correspond au nom du compte. Il existe deux fonctions d’assistance, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) et [**BuildTrusteeWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea), qui initialisent une structure de **tiers de confiance** avec un SID ou un nom spécifié. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) et [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) vous permettent d’initialiser une structure de **tiers de confiance** avec des informations ACE spécifiques à l’objet. Trois autres fonctions d’assistance, [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma), [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)et [**GetTrusteeType**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea), récupèrent les valeurs des différents membres d’une structure de **tiers de confiance** .

Le membre **ptstrName** de la structure de [**tiers de confiance**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) peut être un pointeur vers un [**objet et un \_ \_ nom**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) ou [**des objets et une structure \_ \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) . Ces structures spécifient des informations sur une entrée du contrôle d’accès spécifique à l' [objet](object-specific-aces.md) , en plus d’un nom de tiers de confiance ou d’un SID. Cela permet aux fonctions telles que [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) et [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) de stocker des informations ACE spécifiques à l’objet dans le membre du tiers de **confiance** de la structure d' [**\_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) .

 

 
