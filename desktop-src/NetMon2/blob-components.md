---
description: Composants BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Composants BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204012"
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

 

 



