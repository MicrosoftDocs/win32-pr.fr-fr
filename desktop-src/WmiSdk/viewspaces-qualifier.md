---
description: Le qualificateur ViewSpaces définit les noms et l’emplacement des espaces de noms où se trouvent les instances source. Vous pouvez spécifier n’importe quelle combinaison d’espaces de noms sur des ordinateurs locaux ou distants.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificateur ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210538"
---
# <a name="viewspaces-qualifier"></a>Qualificateur ViewSpaces

Le **qualificateur ViewSpaces** définit les noms et l’emplacement des espaces de noms où se trouvent les instances source. Vous pouvez spécifier n’importe quelle combinaison d’espaces de noms sur des ordinateurs locaux ou distants.

L’exemple suivant répertorie deux espaces de noms sur l’ordinateur local.


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



Le [fournisseur de vues](view-provider.md) met en correspondance les requêtes sources du [qualificateur ViewSources](viewsources-qualifier.md) avec les espaces de noms répertoriés dans le qualificateur **ViewSpaces** dans l’ordre dans lequel les requêtes et les espaces de noms sont répertoriés. Normalement, il existe une relation un-à-un entre le nombre d’espaces de noms figurant dans le qualificateur **ViewSpaces** et les requêtes listées dans le qualificateur **ViewSources** . Dans certains cas, vous souhaiterez peut-être que les requêtes listées dans le qualificateur ViewSources s’exécutent sur deux espaces de noms ou plus. Vous pouvez utiliser un double deux-points «  :: » pour séparer plusieurs espaces de noms qui seront évalués par l’une des requêtes dans le tableau **ViewSources** .

Dans l’exemple suivant, la première requête du tableau [**ViewSources**](viewsources-qualifier.md) est exécutée sur l’espace de noms dans la première paire de guillemets, la deuxième requête sur les trois espaces de noms dans la deuxième paire de guillemets, et la troisième pour les deux espaces de noms dans la troisième paire de guillemets.


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs spécifiques au fournisseur de vues**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




