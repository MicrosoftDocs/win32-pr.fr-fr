---
title: appel-vs
description: Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie. | appel-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2321224b10ca1f7822b19e48ebbb58c1e01c261720f64a8b39331fbceab75fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986889"
---
# <a name="call---vs"></a>appel-vs

Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie.

## <a name="syntax"></a>Syntaxe



| appeler l\# |
|----------|



 

où l \# est une [étiquette, et](label---vs.md) qui marque le début de la sous-routine à appeler.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| appel                   |      | x    | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :

1.  Adresse push de la prochaine instruction à la pile d’adresses de retour.
2.  Poursuivez l’exécution à partir de l’instruction marquée par l’étiquette.

Dans le nuanceur de sommets 2 \_ 0, les appels d’imbrication ne sont pas autorisés.

Dans le nuanceur de vertex 2 \_ x, la profondeur d’imbrication est limitée par l’élément StaticFlowControlDepth de la structure [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) . Pour plus d’informations, consultez [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

Dans le nuanceur de sommets 3 \_ 0, quatre niveaux d’imbrication des appels sont autorisés.

Seuls les appels de transfert sont autorisés. Cela signifie que l’emplacement de l’étiquette dans le nuanceur de sommets doit se trouver après l’instruction call qui la référence.

Si une instruction d’appel est appelée à l’intérieur d’une [boucle](loop---vs.md)... bloc [ENDLOOP](endloop---vs.md) , la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) est accessible à l’intérieur de la sous-routine.

Si une sous-routine référence le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) situé en dehors de la sous-routine, chaque instance de l’appel à cette sous-routine doit être entourée d’une [boucle](loop---vs.md)... bloc [ENDLOOP](endloop---vs.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
