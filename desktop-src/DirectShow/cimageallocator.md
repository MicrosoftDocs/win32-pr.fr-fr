---
description: La classe CImageAllocator implémente un allocateur qui gère les bitmaps indépendantes du périphérique (DIB) GDI. Cette classe dérive de la classe CBaseAllocator. Il crée des exemples de supports qui sont implémentés à l’aide de la classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: CImageAllocator, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 383b9c2ca992db66e7bf397e42dcb8aaaa4bdb66251ddfd67f4b5175d87058aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402580"
---
# <a name="cimageallocator-class"></a>CImageAllocator, classe

![hiérarchie de la classe cimageallocator](images/wutil04.png)

La `CImageAllocator` classe implémente un allocateur qui gère les bitmaps indépendantes du périphérique (DIB) GDI. Cette classe dérive de la classe [**CBaseAllocator**](cbaseallocator.md) . Il crée des exemples de supports qui sont implémentés à l’aide de la classe [**CImageSample**](cimagesample.md) .

Un allocateur est partagé par deux broches connectées, mais appartient toujours à l’un des filtres de la connexion. Un filtre qui utilise `CImageAllocator` doit assurer le suivi de la façon dont l’allocateur a été fourni par lui-même ou par l’autre filtre. Si l’allocateur a été fourni seul, le filtre propriétaire peut s’appuyer sur le fait que tous les échantillons de média de l’allocateur sont des objets **CImageSample** . Il peut donc utiliser l’objet **CImageSample** pour obtenir des informations sur le DIB, qui est stocké dans une structure [**DIBDATA**](dibdata.md) .

Le filtre propriétaire doit appeler **NotifyMediaType** chaque fois que le type de média change.



| Variables membres protégées                                     | Description                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Pointeur désignant le filtre propriétaire.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Pointeur vers le type de média actuel.                                       |
| Méthodes protégées                                              | Description                                                              |
| [**Utilis**](cimageallocator-alloc.md)                         | Alloue de la mémoire pour les mémoires tampons.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Vérifie les propriétés d’allocateur par rapport au type de média actuel.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Crée un DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Crée un exemple de support. Virtuels.                                         |
| [**Gratuit**](cimageallocator-free.md)                           | Libère toute la mémoire tampon.                                       |
| M&#233;thodes publiques                                                 | Description                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Méthode de constructeur.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informe l’objet du type de média actuel.                            |
| Méthodes IMemAllocator                                          | Description                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




