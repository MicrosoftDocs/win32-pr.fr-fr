---
title: Composants du descripteur de sécurité
description: Après avoir utilisé la méthode IADs. obtenir pour récupérer un pointeur d’interface IADsSecurityDescriptor, vous pouvez utiliser les propriétés IADsSecurityDescriptor pour lire ou écrire les composants du descripteur de sécurité d’un objet d’annuaire.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Composants du descripteur de sécurité AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aa5ec61507e56c03bcc3809a2a5eebcb2cbcd36e18f63119aca53448c8a0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024917"
---
# <a name="security-descriptor-components"></a>Composants du descripteur de sécurité

Après avoir utilisé la méthode [**IADs. obtenir**](/windows/desktop/api/iads/nf-iads-iads-get) pour récupérer un pointeur d’interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) , vous pouvez utiliser les propriétés **IADsSecurityDescriptor** pour lire ou écrire les composants du descripteur de sécurité d’un objet d’annuaire. Par exemple, pour obtenir ou définir la liste DACL de l’objet, utilisez la propriété [**DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) .

Un descripteur de sécurité peut stocker les données suivantes :

-   Identificateur de sécurité (SID) qui identifie le propriétaire de l’objet : le propriétaire d’un objet a le droit implicite de modifier les données DACL et Owner dans le descripteur de sécurité de l’objet.
-   Liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) qui identifie les utilisateurs et les groupes qui peuvent effectuer diverses opérations sur l’objet : une liste DACL contient une liste d’entrées de contrôle d’accès (ACE). Chaque ACE autorise ou refuse un ensemble spécifié de droits d’accès à un compte d’utilisateur, un compte de groupe ou un autre tiers de confiance spécifié. Pour plus d’informations, consultez [récupération de la liste DACL d’un objet](retrieving-an-objectampaposs-dacl.md).
-   Une liste de contrôle d’accès système (SACL) qui contrôle la façon dont le système audite les tentatives d’accès à l’objet : chaque ACE d’une liste SACL spécifie les types de tentatives d’accès qui génèrent une entrée de journal d’audit pour un compte d’utilisateur, un compte de groupe ou un autre tiers de confiance spécifié. Pour plus d’informations, consultez [récupération de la liste SACL d’un objet](retrieving-an-objectampaposs-sacl.md).
-   ensemble de indicateurs de contrôle de contrôle de **\_ descripteur \_ de sécurité** qui qualifient la signification d’un descripteur de sécurité ou de ses composants : par exemple, le **SE indicateur \_ dacl \_ protégé** protège la dacl du descripteur de sécurité de l’héritage des entrées de contrôle d’accès de son objet parent.
-   Identificateur de sécurité (SID) qui identifie le groupe principal de l’objet : Active Directory Domain Services n’utilisez pas ce composant.

Pour plus d’informations et pour obtenir un exemple de code qui peut être utilisé pour lire et afficher les données dans un descripteur de sécurité d’objet et DACL, consultez [lecture du descripteur de sécurité d’un objet](reading-an-objectampaposs-security-descriptor.md).

 

 