---
description: La propriété FullScreenMode définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriété FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015617"
---
# <a name="fullscreenmode-property"></a>Propriété FullScreenMode

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `FullScreenMode` propriété définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant s’il faut activer ou désactiver la lecture en plein écran.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est false.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| true  | Activez la lecture en plein écran. Il s'agit de la valeur par défaut |
| false | Désactivez la lecture en plein écran.                          |



 

Le mode plein écran est disponible uniquement lorsque le contrôle MSWebDVD s’exécute en mode fenêtre.

 

 



