---
description: La propriété SubpictureStreamsAvailable récupère le nombre de flux de sous-image disponibles dans le titre actuel.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propriété SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2349cb696c1f6d363fefb6a6e90a662fa7c3233b3b0aefcb57d381a604f41832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633439"
---
# <a name="subpicturestreamsavailable-property"></a>Propriété SubpictureStreamsAvailable

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SubpictureStreamsAvailable` propriété récupère le nombre de flux de sous-image disponibles dans le titre actuel.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre de flux disponibles sous la forme d’un entier.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Pour interroger chaque flux pour son attribut Language, appelez d’abord cette méthode pour obtenir la limite supérieure.

La numérotation des flux est de base zéro.

 

 



