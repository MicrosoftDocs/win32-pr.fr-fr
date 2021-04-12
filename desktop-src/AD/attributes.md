---
title: Attributs (AD DS)
description: Chaque objet dans Active Directory Domain Services contient un ensemble d’attributs qui définissent les caractéristiques de l’objet.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- attributs AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031054"
---
# <a name="attributes-ad-ds"></a>Attributs (AD DS)

Chaque objet dans Active Directory Domain Services contient un ensemble d’attributs qui définissent les caractéristiques de l’objet. Chaque attribut est décrit par un objet [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) dans le conteneur de schéma qui définit l’attribut. La définition de l’attribut comprend une variété de données, par exemple, les types d’objets auxquels s’applique l’attribut et le type de syntaxe de l’attribut. Pour plus d’informations sur les définitions de schéma d’attribut, consultez [caractéristiques des attributs](characteristics-of-attributes.md).

La liste suivante répertorie les types d’attributs qui sont stockés dans Active Directory Domain Services.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Attributs stockés et répliqués dans un domaine
</dt> <dd>

Certains attributs sont stockés dans le répertoire (par exemple, [**CN**](/windows/desktop/ADSchema/a-cn), [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)et [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) et répliqués sur tous les contrôleurs de domaine dans un domaine. Un sous-ensemble de ces attributs est également répliqué dans le catalogue global. Si vous énumérez les attributs d’un objet à partir du catalogue global, seuls les attributs répliqués dans le catalogue global sont retournés. Certains attributs sont également indexés, car l’inclusion d’une propriété indexée dans une requête améliore les performances des requêtes.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Attributs non répliqués, stockés localement
</dt> <dd>

Les attributs non répliqués, tels que [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon)et [**Last-Logoff**](/windows/desktop/ADSchema/a-lastlogoff) , sont stockés sur chaque contrôleur de domaine, mais ne sont pas répliqués. Les attributs non répliqués sont des attributs qui se rapportent à un contrôleur de domaine particulier. Par exemple, l’attribut **Last-Logon** correspond à la date et à l’heure de la dernière validation de l’ouverture de session réseau de l’utilisateur par ce contrôleur de domaine particulier qui a retourné la propriété. Ces attributs peuvent être récupérés de la même façon que les attributs à l’ensemble du domaine décrits précédemment. Toutefois, pour ces attributs, chaque contrôleur de domaine stocke uniquement les valeurs qui se rapportent à ce contrôleur de domaine particulier. Par exemple, pour obtenir la dernière fois qu’un utilisateur a ouvert une session sur le domaine, récupérez l’attribut **Last-Logon** pour l’utilisateur de chaque contrôleur de domaine dans le domaine et recherchez la date et l’heure les plus récentes.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Attributs non stockés et construits
</dt> <dd>

Un objet utilisateur a également des attributs construits qui ne sont pas stockés dans l’annuaire, mais qui sont calculés par le contrôleur de domaine, par exemple [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) et [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 