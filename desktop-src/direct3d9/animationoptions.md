---
description: Vous permet de définir les options d’animation.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111014"
---
# <a name="animationoptions"></a>AnimationOptions

Vous permet de définir les options d’animation.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Où :

-   openclosed : utilisez 0 pour une animation fermée ou 1 pour une animation ouverte. Par défaut, une animation est fermée.
-   positionquality : définit la qualité de position pour toutes les clés de position spécifiées. Utilisez 0 pour les positions de spline ou 1 pour les positions linéaires.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



