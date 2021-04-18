---
description: Fournit des restrictions pour l’utilisation de valeurs 64 bits dans le cadre d’un chemin d’accès.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Prise en charge des instances de classe pour les valeurs 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542960"
---
# <a name="class-instance-support-for-64-bit-values"></a>Prise en charge des instances de classe pour les valeurs 64 bits

Vous pouvez utiliser une valeur de clé 64 bits dans le cadre d’un chemin d’accès, avec les restrictions suivantes :

-   Tant que vous ne dépassez pas la plage de 32 bits, vous pouvez assigner et récupérer des valeurs à partir de la clé, comme vous le feriez pour une propriété 32 bits.
-   Une fois que vous avez dépassé la valeur entière de 0x7FFFFFFF (pour les types signés), 0x80000000 (pour les types non signés) ou 32 bits, vous devez utiliser des guillemets.
-   Le seul chemin d’accès valide pour une valeur 64 bits se trouve dans les propriétés **\_ \_ RelPath** ou **\_ \_ path** de l’instance. Par conséquent, WMI ne prend pas en charge la notation hexadécimale pour la valeur équivalente.
-   Si WMI enregistre la clé d’instance sous la forme d’un nombre négatif, vous devez utiliser le numéro d’origine pour récupérer l’instance.

La sémantique de requête n’est pas affectée et se comporte comme prévu. Ce comportement affecte uniquement le chemin d’accès de l’objet, les opérations [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)et [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

L’exemple suivant montre que les instances de classe peuvent avoir des valeurs de clé de 64 bits.

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



