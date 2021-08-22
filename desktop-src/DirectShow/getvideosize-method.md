---
description: La méthode GetVideoSize récupère les dimensions natives de la vidéo.
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: Méthode GetVideoSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21746242211357e9e58e825d8e217799953dd569e91765acabe11fc2252d17c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536589"
---
# <a name="getvideosize-method"></a>Méthode GetVideoSize

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetVideoSize` méthode récupère les dimensions natives de la vidéo.

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a>Valeur renvoyée

Retourne un objet [DVDRect](dvdrect-object.md) contenant quatre propriétés en lecture/écriture : (en haut à gauche) x ; (en haut à gauche) y, largeur et hauteur. Les propriétés **x** et **y** sont définies sur zéro et les deux autres propriétés reflètent la largeur et la hauteur du rectangle vidéo tel qu’il a été créé sur le disque.

 

 



