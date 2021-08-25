---
description: La méthode PlayForwards démarre la lecture en avant à partir de l’emplacement actuel à la vitesse spécifiée.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Méthode PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e607779147ba057b9cfd747ebfe827a25e294e2b04cdfa7e61a0691ecf293c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830629"
---
# <a name="playforwards-method"></a>Méthode PlayForwards

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayForwards` méthode commence la lecture en avant à partir de l’emplacement actuel à la vitesse spécifiée.

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*
</dt> <dd>

Spécifie la vitesse à laquelle jouer en tant que valeur entière. Cette valeur est un multiplicateur — 1.0 est une vitesse de lecture normale ; 2,0 est à double vitesse, 0,5 à mi-vitesse, et ainsi de suite. Quand **nSpeed** n’est pas égal à 1,0, l’audio est muet et la sous-image est désactivée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayBackwards**](playbackwards-method.md)
</dt> </dl>

 

 



