---
description: Composants BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Composants BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367481"
---
# <a name="blob-components"></a>Composants BLOB

Un objet BLOB (Binary Large Object) comprend les composants hiérarchiques suivants :

-   Propriétaires
-   Catégories
-   Balises
-   Valeurs

## <a name="textual-representation"></a>Représentation textuelle

Pour plus de commodité, les objets BLOB s’affichent dans le format propriétaire : catégorie : balise : valeur dans lequel ils apparaissent lorsqu’ils sont enregistrés dans un fichier. La structure interne de l’objet BLOB est opaque, car elle représente les pointeurs et les tables. Par exemple, voici une entrée d’un objet BLOB qui peut être utilisée pour configurer un NPP :

``` syntax
NPP:Configure:BufferSize=32768
```

Le propriétaire est NPP. La catégorie est configurer, la balise est BufferSize et la valeur est 32768.

 

 



