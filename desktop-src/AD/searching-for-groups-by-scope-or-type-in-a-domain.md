---
title: Recherche de groupes par portée ou par type dans un domaine
description: dans Windows domaines 2000, il existe une seule classe appelée groupe pour toutes les étendues de groupe (domaine Local, Global, universel) et types (sécurité, distribution).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Recherche de groupes par étendue ou type dans un domaine AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d424ce21912aa1e7fa7104099fc8359a5a1c80beeae1fc143aa0bd4aea71d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024947"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Recherche de groupes par portée ou par type dans un domaine

dans Windows domaines 2000, il existe une seule classe appelée [**groupe**](/windows/desktop/ADSchema/c-group) pour toutes les étendues de groupe (domaine Local, Global, universel) et types (sécurité, distribution). L’attribut [**GroupType**](/windows/desktop/ADSchema/a-grouptype) de l’objet Group spécifie le type de groupe et l’étendue.

pour utiliser le type ou l’étendue pour rechercher des groupes sur Windows domaines 2000, utilisez un filtre qui contient une règle de correspondance pour l’attribut [**groupType**](/windows/desktop/ADSchema/a-grouptype) . Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).

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



 

 