---
description: Vous permet de définir les options d’animation.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346eaa1b94637fa357f09cd701ac9d99d5ddf2076ee12654076e54bce82527fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069429"
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

 

 



