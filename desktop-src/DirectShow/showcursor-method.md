---
description: La méthode ShowCursor rend le curseur visible lorsque l’objet MSWebDVD est en mode plein écran.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Méthode ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050519"
---
# <a name="showcursor-method"></a>Méthode ShowCursor

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

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

## <a name="remarks"></a>Remarques

Lorsque l’affichage du DVD passe en mode plein écran, le curseur disparaît dans les 3 à 5 secondes. Utilisez cette méthode pour que le curseur soit de nouveau visible si les boutons de contrôle de votre application sont visibles en mode plein écran.

 

 



