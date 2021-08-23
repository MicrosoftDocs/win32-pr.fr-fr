---
title: SNB (Objidl. h)
description: Un bloc de nom de chaîne (SNB) est un pointeur vers un tableau de pointeurs vers des chaînes, qui se termine par un pointeur NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49a7868912b9d7d1e3d9f3b1f82805e6e285d815eacbc559c887febd23e9e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682779"
---
# <a name="snb"></a>SNB

Un bloc de nom de chaîne (**SNB**) est un pointeur vers un tableau de pointeurs vers des chaînes, qui se termine par un pointeur **null** . Les blocs de nom de chaîne sont utilisés par l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et par les appels de fonction qui ouvrent des objets de stockage. Les chaînes pointent vers les objets de stockage contenus ou les flux qui doivent être exclus dans les appels ouverts.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**SNB**
</dt> <dd>

\[\_marshaling de câble (wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Remarques

Le **SNB** doit être créé en allouant un bloc de mémoire contigu dans lequel les pointeurs vers les chaînes sont suivis d’un pointeur **null** , qui est ensuite suivi des chaînes réelles.

Le marshaling d’un **SNB** est basé sur l’hypothèse que le **SNB** qui a été passé a été créé de cette façon. Bien qu’il puisse être stocké d’une autre manière, les **SNB** créés de cette manière ont l’avantage d’exiger une seule opération d’allocation et de libérer de la mémoire pour toutes les chaînes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





