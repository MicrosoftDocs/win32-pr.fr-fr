---
description: Définition des propriétés personnalisées.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Définition des propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348049"
---
# <a name="defining-custom-properties"></a>Définition des propriétés personnalisées

**Définition des propriétés personnalisées**.

si le minipilote wia (Windows Image Acquisition) est nécessaire pour définir des propriétés personnalisées, la \_ \_ propriété DEVPROP privée wia doit être utilisée pour les propriétés de l’élément racine personnalisé, et la \_ \_ propriété ITEMPROP privée wia "doit être utilisée pour les autres propriétés de l’élément. Ces constantes sont définies dans *wiadef. h*.

L’exemple de code suivant montre des définitions pour trois propriétés d’élément racine. L’ID de propriété de la première propriété d’élément racine personnalisée \_ , \_ prop source personnalisée \_ 1, est défini en termes \_ de \_ DEVPROP privés WIA. Les ID de propriété pour les propriétés d’élément racine supplémentaires sont définis en termes de \_ DEVPROP privée WIA \_ + 1, WIA \_ Private \_ DEVPROP + 2, et ainsi de suite. Le modèle peut être poursuivi si des propriétés d’élément racine personnalisées supplémentaires sont nécessaires.


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



L’exemple suivant montre des définitions pour trois propriétés d’élément enfant personnalisées et ID de propriété. L’ID de propriété de la première propriété d’élément enfant personnalisé \_ , \_ prop enfant personnalisée \_ 1, est défini en termes \_ de \_ ITEMPROP privés WIA. Les ID de propriété pour les propriétés d’élément enfant supplémentaires sont définis en termes de \_ ITEMPROP privé WIA \_ + 1, et ainsi de suite. Comme précédemment, le modèle peut être poursuivi si davantage de propriétés d’élément enfant personnalisées sont nécessaires.


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



Les propriétés WIA personnalisées doivent avoir des noms de propriétés personnalisés associés aux ID de propriétés personnalisées. L’exemple de code suivant montre des définitions pour trois noms de propriété d’élément racine personnalisés. (Ces noms de propriétés sont utilisés avec les ID de propriétés personnalisées qui ont été créés dans un exemple précédent, où le nom de la propriété personnalisée contenu dans CUSTOM \_ \_La prop racine \_ 1 \_ Str est associée à l’ID de propriété de l’élément racine personnalisé prop de la \_ racine personnalisée \_ \_ 1.)


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> Les noms de propriété WIA ne sont *pas* localisés dans plusieurs langues. Cela est dû au fait que les propriétés WIA peuvent être lues par les applications à l’aide de l’ID de propriété ou du nom de propriété. Si le nom est utilisé, il doit s’agir d’une constante, tout comme l’ID de propriété.

 

 

 



