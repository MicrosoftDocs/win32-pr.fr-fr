---
description: La propriété AnglesAvailable récupère le nombre d’angles actuellement disponibles.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propriété AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515539"
---
# <a name="anglesavailable-property"></a>Propriété AnglesAvailable

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `AnglesAvailable` propriété récupère le nombre d’angles actuellement disponibles.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière comprise entre 1 et 9 représentant le nombre d’angles actuellement disponibles. Si


```
iAngles
```



= 1, il n’y a aucun bloc d’angle à l’emplacement actuel.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Un *bloc angulaire* est un segment vidéo qui a été capturé à partir de plusieurs angles d’appareil photo. Un bloc angle peut comporter jusqu’à neuf angles, numérotés de 1 à 9. Lorsque le navigateur DVD entre pour la première fois dans un bloc angle, il envoie à votre application une \_ notification d’événement d’angles de DVD EC \_ \_ disponible avec le nombre d’angles dans *lParam1*. Un disque peut être créé pour afficher automatiquement un menu pour les angles disponibles lorsqu’il entre dans un bloc angle, mais, en général, une application doit déterminer le nombre d’angles disponibles et offrir à l’utilisateur un moyen d’en sélectionner un.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CurrentAngle**](currentangle-property.md)
</dt> </dl>

 

 



