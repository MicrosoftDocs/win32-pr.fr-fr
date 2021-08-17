---
description: Ces constantes s’appliquent aux variables d’effet.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: Constantes D3D10_EFFECT_VARIABLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7541253fffd6671e01a8da38c06fd15924d45b461d5acc0e468fd17660746f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736068"
---
# <a name="d3d10_effect_variable-constants"></a>\_Constantes de variable d’effet D3D10 \_

Ces constantes s’appliquent aux variables d’effet.



| \#définition                                       | Description  | Valeur                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Annotation de \_ variable d’effet D3D10 \_            | 1 << 0 | Indique qu’il s’agit d’une annotation ou d’une variable globale.                                                                                                                                                                                                        |
| \_Variable d’effet D3D10 \_ \_ regroupée                | 1 << 1 | Indique que cette variable ou cette mémoire tampon constante réside dans un pool d’effets. Si cet indicateur n’est pas défini, la variable réside dans un effet autonome ou un effet enfant (les effets autonomes renvoient la valeur false à partir de [**ID3D10Effect :: IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool). |
| \_Point de \_ \_ liaison explicite \_ \_ de la variable d’effet D3D10 | 1 << 2 | Indique que la variable a été explicitement liée à l’aide du mot clé Register.                                                                                                                                                                                 |



 

Ces indicateurs sont définis en tant que macros dans d3d10effect. h.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets, constantes (Direct3D 10)](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



