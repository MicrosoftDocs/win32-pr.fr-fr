---
description: La propriété FullScreenMode définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriété FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108538"
---
# <a name="fullscreenmode-property"></a>Propriété FullScreenMode

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `FullScreenMode` propriété définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant s’il faut activer ou désactiver la lecture en plein écran.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture et sa valeur par défaut est false.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| true  | Activez la lecture en plein écran. Il s'agit de la valeur par défaut |
| false | Désactivez la lecture en plein écran.                          |



 

Le mode plein écran est disponible uniquement lorsque le contrôle MSWebDVD s’exécute en mode fenêtre.

 

 



