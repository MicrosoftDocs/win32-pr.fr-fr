---
title: Noms d’objets et identités
description: Dans Active Directory Domain Services, un objet a plusieurs identités, y compris les éléments suivants.
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- noms d’objets et identités Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dc3e79cd40eebb47fe85b14f50130750cdb4a1cea884d8ebf50a89555d2ba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025578"
---
# <a name="object-names-and-identities"></a>Noms d’objets et identités

Dans Active Directory Domain Services, un objet a plusieurs identités, y compris les éléments suivants.

## <a name="relative-distinguished-name"></a>Nom unique relatif

Le nom unique relatif est le nom défini par l’attribut de nom d’un objet. L’attribut **rDnAttID** d’un objet **classSchema** identifie l’attribut de nom pour les instances de la classe. La plupart des classes d’objet utilisent l’attribut **CN** (Common-Name) comme attribut de nom. Le nom unique relatif d’un objet doit être unique dans le conteneur où se trouve l’objet. Il peut y avoir de nombreuses instances d’objet avec le même nom unique relatif, mais deux ne peuvent pas être dans le même conteneur. Pour plus d’informations sur l’attribut **rDnAttID** et les objets **classSchema** , consultez [caractéristiques des classes d’objets](characteristics-of-object-classes.md).

## <a name="distinguished-name"></a>Nom unique

Le [*nom unique*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) est le nom actuel de l’objet et est contenu dans l’attribut **distinguishedName** de l’objet. Le nom unique est une chaîne qui comprend l’emplacement de l’objet et est formé en concaténant le nom unique relatif de l’objet et chacun de ses ancêtres jusqu’à la racine. Par exemple, le nom unique du conteneur Users dans le domaine Fabrikam.com serait « CN = Users, DC = fabrikam, DC = com ». Les noms uniques sont uniques au sein d’une forêt. Le nom unique d’un objet change lorsque l’objet est déplacé ou renommé.

## <a name="object-guid"></a>GUID de l’objet

Le GUID de l’objet est un identificateur global unique affecté par Active Directory Domain Services lors de la création de l’instance d’objet. Le GUID de l’objet est contenu dans l’attribut **objectGUID** de l’objet. Un GUID est un nombre 128 bits garanti pour être unique dans l’espace et dans le temps. Les GUID d’objet ne changent jamais ; par conséquent, si un objet est renommé ou déplacé n’importe où dans la forêt d’entreprise, le GUID de l’objet reste le même. Les applications qui enregistrent des références aux objets dans Active Directory Domain Services doivent utiliser le GUID de l’objet pour s’assurer que la référence d’objet survivra à un changement de nom de l’objet. Le nom unique d’un objet peut changer, mais ce n’est pas le cas du GUID de l’objet.

## <a name="other-identities"></a>Autres identités

Les instances d’objet peuvent avoir de nombreux autres attributs, et les attributs peuvent être utilisés pour l’identification par les applications. Par exemple, les objets principal de sécurité (instances des classes d’objets **utilisateur**, **ordinateur** et **groupe** ) ont des attributs **userPrincipalName**, **sAMAccountName** et **objectSID** . ces attributs sont des « noms » très importants pour Windows 2000, mais ils ne font pas partie de l’identité de l’objet du point de vue du répertoire.

 

 