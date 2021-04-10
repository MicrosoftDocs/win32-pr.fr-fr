---
description: La méthode ShowCursor rend le curseur visible lorsque l’objet MSWebDVD est en mode plein écran.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Méthode ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846414"
---
# <a name="showcursor-method"></a>Méthode ShowCursor

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ShowCursor` méthode rend le curseur visible lorsque l’objet **mswebdvd** est en mode plein écran.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Spécifie s’il faut afficher le curseur en tant que valeur booléenne.



| Valeur | Description            |
|-------|------------------------|
| true  | Afficher le curseur        |
| false | Ne pas afficher le curseur |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Lorsque l’affichage du DVD passe en mode plein écran, le curseur disparaît dans les 3 à 5 secondes. Utilisez cette méthode pour que le curseur soit de nouveau visible si les boutons de contrôle de votre application sont visibles en mode plein écran.

 

 



