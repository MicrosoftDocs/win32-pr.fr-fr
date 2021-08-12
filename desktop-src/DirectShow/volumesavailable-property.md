---
description: La propriété VolumesAvailable récupère le nombre de volumes dans un ensemble multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propriété VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650936"
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

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Certains titres de DVD peuvent être publiés sous la forme d’un jeu ou d’une série à plusieurs disques. Utilisez cette méthode pour déterminer le numéro de volume du disque actuel.

 

 



