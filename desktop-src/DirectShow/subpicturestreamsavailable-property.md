---
description: La propriété SubpictureStreamsAvailable récupère le nombre de flux de sous-image disponibles dans le titre actuel.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propriété SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530743"
---
# <a name="subpicturestreamsavailable-property"></a>Propriété SubpictureStreamsAvailable

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SubpictureStreamsAvailable` propriété récupère le nombre de flux de sous-image disponibles dans le titre actuel.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre de flux disponibles sous la forme d’un entier.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Pour interroger chaque flux pour son attribut Language, appelez d’abord cette méthode pour obtenir la limite supérieure.

La numérotation des flux est de base zéro.

 

 



