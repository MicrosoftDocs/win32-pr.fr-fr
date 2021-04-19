---
description: L’événement UpdateOverlay est envoyé lorsque la surface de recouvrement a été déplacée ou redimensionnée ou que sa clé de couleur a changé.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533243"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

L’événement **UpdateOverlay** est envoyé lorsque la surface de recouvrement a été déplacée ou redimensionnée ou que sa clé de couleur a changé.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Notes

Les applications ne doivent jamais se préoccuper de la surface de superposition redimensionnée ou déplacée. Tout est géré en interne. Toutefois, cet événement est également envoyé lorsque la clé de couleur change. Cela signifie que si une application héberge MSWebDVD comme un contrôle sans fenêtre et affiche des boutons flottants en plus de la surface vidéo en mode plein écran, elle doit répondre à cet événement en obtenant la nouvelle valeur de la propriété **ColorKey** afin de pouvoir dessiner correctement les boutons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

 




