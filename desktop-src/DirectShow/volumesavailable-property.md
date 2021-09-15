---
description: La propriété VolumesAvailable récupère le nombre de volumes dans un ensemble multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propriété VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238890"
---
# <a name="volumesavailable-property"></a>Propriété VolumesAvailable

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `VolumesAvailable` propriété récupère le nombre de volumes dans un ensemble multivolume.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre de volumes dans le jeu sous la forme d’un entier.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Certains titres de DVD peuvent être publiés sous la forme d’un jeu ou d’une série à plusieurs disques. Utilisez cette méthode pour déterminer le numéro de volume du disque actuel.

 

 



