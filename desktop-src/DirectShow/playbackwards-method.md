---
description: La méthode PlayBackwards démarre la lecture vers l’arrière à partir de l’emplacement actuel à la vitesse spécifiée.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Méthode PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998985"
---
# <a name="playbackwards-method"></a>Méthode PlayBackwards

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayBackwards` méthode démarre la lecture vers l’arrière à partir de l’emplacement actuel à la vitesse spécifiée.

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Spécifie la vitesse à laquelle jouer en tant que nombre. Ce nombre est un multiplicateur : 1.0 est une vitesse de lecture normale ; 2,0 est à double vitesse, 0,5 à mi-vitesse, et ainsi de suite. Quand **nSpeed** n’est pas égal à 1,0, l’audio est muet et la sous-image est désactivée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayForwards**](playforwards-method.md)
</dt> </dl>

 

 



