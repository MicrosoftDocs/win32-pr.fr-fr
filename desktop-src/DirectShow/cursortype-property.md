---
description: La propriété CursorType définit ou récupère le type de curseur actuel.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: CursorType, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846357"
---
# <a name="cursortype-property"></a>CursorType, propriété

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CursorType` propriété définit ou récupère le type de curseur actuel.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le type de curseur.

## <a name="remarks"></a>Notes

Les valeurs possibles pour cette propriété sont :



| Valeur | Description |
|-------|-------------|
| 0     | Flèche       |
| 1     | Zoom avant     |
| 2     | Zoom arrière    |
| 3     | Toutefois        |
| -1    | Aucun        |



 

Cette propriété est en lecture/écriture avec une valeur par défaut de zéro. Lorsque l’image est zoomée, le paramètre `CursorType` à la **main** (0x3) met l’application en mode glisser-déplacer, ce qui permet à l’utilisateur de déplacer l’image à l’intérieur de la zone d’affichage vidéo.

 

 



