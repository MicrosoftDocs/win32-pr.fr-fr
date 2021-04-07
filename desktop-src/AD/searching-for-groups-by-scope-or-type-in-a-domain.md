---
title: Recherche de groupes par portée ou par type dans un domaine
description: Dans les domaines Windows 2000, il existe une seule classe appelée groupe pour toutes les étendues de groupe (domaine local, global, universel) et types (sécurité, distribution).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Recherche de groupes par étendue ou type dans un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724428"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Recherche de groupes par portée ou par type dans un domaine

Dans les domaines Windows 2000, il existe une seule classe appelée [**groupe**](/windows/desktop/ADSchema/c-group) pour toutes les étendues de groupe (domaine local, global, universel) et types (sécurité, distribution). L’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) de l’objet Group spécifie le type de groupe et l’étendue.

Pour utiliser le type ou l’étendue pour rechercher des groupes sur les domaines Windows 2000, utilisez un filtre qui contient une règle de correspondance pour l’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).

Pour plus d’informations et pour obtenir un exemple de code qui montre comment rechercher des groupes dans un domaine, consultez l' [exemple de code pour rechercher des groupes dans un domaine](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Exemples de chaînes de requête LDAP

Les exemples de chaînes de requête suivants montrent comment construire une chaîne de requête LDAP utilisée pour rechercher ou filtrer des types de groupes spécifiques.

La chaîne de requête suivante recherche des groupes de sécurité. Cet exemple utilise « -2147483648 » comme équivalent décimal de l’indicateur **de \_ sécurité de type groupe ADS \_ \_ \_ activé** .


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



La chaîne de requête suivante recherche les groupes de distribution universels ; autrement dit, les groupes qui contiennent l’indicateur de **\_ \_ \_ \_ groupe universel du type de groupe ADS** et ne contiennent pas l’indicateur de sécurité de **\_ type groupe ADS \_ \_ \_ activé** . Cet exemple utilise « 8 » comme équivalent décimal du type de groupe **ad \_ \_ \_ \_ groupe universel** et « -2147483648 » comme équivalent décimal du type de **\_ groupe ADS \_ \_ \_ activée** pour la sécurité.


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 