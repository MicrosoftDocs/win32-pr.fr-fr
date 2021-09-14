---
description: La méthode zoom fait un zoom avant ou arrière sur un ensemble donné de coordonnées d’écran.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom, méthode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111058"
---
# <a name="zoom-method"></a>Zoom, méthode

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Zoom` méthode effectue un zoom avant ou arrière sur un ensemble donné de coordonnées d’écran.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Spécifie la coordonnée x au centre de la zone de zoom rectangulaire sous la forme d’un entier.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Spécifie la coordonnée y au centre du rectangle à faire faire un zoom sous la forme d’un entier.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Spécifie le facteur d’agrandissement appliqué à la valeur de zoom actuelle sous la forme d’un entier. La valeur maximale totale dépend de ce que la superposition matérielle peut prendre en charge ; Il s’agit généralement d’un facteur de 32 à 64 fois la taille d’origine.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le nouveau facteur de zoom reste en vigueur jusqu’à ce qu’il soit rétabli à sa taille d’origine ou qu’il soit de nouveau modifié. En d’autres termes, deux appels à cette méthode spécifiant un *iZoomRatio* de deux entraînent un ratio de zoom quatre fois supérieur à la taille vidéo d’origine. Si l’utilisateur tente d’effectuer un zoom au-delà de ce que le matériel peut prendre en charge, cette méthode fonctionnera, mais ne fera rien.

La méthode [**SetClipVideoRect**](setclipvideorect-method.md) est une autre façon d’effectuer un zoom avant. la seule différence entre les deux méthodes est la façon dont le rectangle de zoom est spécifié.

 

 



