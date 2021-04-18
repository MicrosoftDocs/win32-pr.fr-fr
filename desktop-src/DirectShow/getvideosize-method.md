---
description: La méthode GetVideoSize récupère les dimensions natives de la vidéo.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Méthode GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106540797"
---
# <a name="getvideosize-method"></a>Méthode GetVideoSize

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetVideoSize` méthode récupère les dimensions natives de la vidéo.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valeur renvoyée

Retourne un objet [DVDRect](dvdrect-object.md) contenant quatre propriétés en lecture/écriture : (en haut à gauche) x ; (en haut à gauche) y, largeur et hauteur. Les propriétés **x** et **y** sont définies sur zéro et les deux autres propriétés reflètent la largeur et la hauteur du rectangle vidéo tel qu’il a été créé sur le disque.

 

 



