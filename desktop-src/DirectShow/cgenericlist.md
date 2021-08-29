---
description: Le modèle de classe CGenericList qui implémente une liste spécifique au type. Pour plus d’informations, consultez CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: CGenericList, classe (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79bbc003770d7fec94af93a54386bccbfbd00c4cd2a8b3f9a8ff81e14aa7a6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999419"
---
# <a name="cgenericlist-class"></a>CGenericList, classe

![hiérarchie de la classe cgenericlist](images/list01.png)

`CGenericList`Modèle de classe qui implémente une liste spécifique au type. Pour plus d’informations, consultez [**CBaseList**](cbaselist.md).

Pour utiliser ce modèle, déclarez une variable de type `CGenericList` avec un argument de modèle qui définit le type d’objet dans la liste. Par exemple, l’instruction suivante déclare une liste d’objets [**CBaseFilter**](cbasefilter.md) :


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Pour plus de commodité, Wxlist. h définit les types de liste suivants :

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| M&#233;thodes publiques                                          | Description                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | Méthode de constructeur.                                                      |
| [**~ CGenericList**](cgenericlist--cgenericlist.md)     | Méthode de destructeur.                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | Récupère la position du premier élément de la liste.                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | Récupère la position du dernier élément de la liste.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Récupère le nombre d’éléments dans la liste.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Récupère l’élément à la position spécifiée et avance la position. |
| [**Télécharger**](cgenericlist-get.md)                         | Récupère l’élément à la position spécifiée.                            |
| [**GetHead**](cgenericlist-gethead.md)                 | Récupère l’élément au début de la liste.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Supprime le premier élément de la liste.                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | Supprime le dernier élément de la liste.                                       |
| [**Installez**](cgenericlist-remove.md)                   | Supprime l'élément à la position spécifiée.                              |
| [**AddBefore**](cgenericlist-addbefore.md)             | Insère un élément ou une liste avant la position spécifiée.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Insère un élément ou une liste après la position spécifiée.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Ajoute un élément ou une liste au début de la liste.                           |
| [**AddTail**](cgenericlist-addtail.md)                 | Ajoute un élément ou une liste à la fin de la liste.                          |
| [**Rechercher**](cgenericlist-find.md)                       | Récupère la première position qui contient l’élément spécifié.              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




