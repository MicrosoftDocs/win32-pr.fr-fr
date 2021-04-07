---
title: Recherche d’objets par nom
description: La plupart des objets dans Active Directory Domain Services utilisent la propriété CN comme attribut de nom.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, recherche, par nom
- objet AD, recherche par nom
- Recherche d’objets par nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671278"
---
# <a name="finding-objects-by-name"></a>Recherche d’objets par nom

La plupart des objets dans Active Directory Domain Services utilisent la propriété **CN** comme attribut de nom. Toutefois, certains objets utilisent un attribut de nom autre que **CN**. Par exemple, un contrôleur de domaine utilise la propriété **domainDNS** pour l’attribut Naming et une unité d’organisation utilise la propriété **OrganizationalUnit** pour l’attribut Naming. Pour éviter d’avoir à utiliser un attribut de nom différent pour les différents types d’objets, la propriété **Name** , qui contient le nom unique relatif de l’objet, doit être utilisée pour rechercher des objets par nom.

## <a name="examples"></a>Exemples

Les exemples de code suivants illustrent des chaînes de requête différentes qui peuvent être utilisées pour rechercher des objets par nom.

La chaîne de requête suivante recherche tous les objets dont le nom commence par « Jeff ».


```C++
(name=Jeff*)
```



La chaîne de requête suivante recherche tous les objets ordinateurs dont le nom commence par « leaseed » ou « Corp ».


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



La chaîne de requête suivante recherche tous les utilisateurs et dont le nom commence par « Karen » ou « Jeff ».


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




