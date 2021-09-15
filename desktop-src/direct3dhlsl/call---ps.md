---
title: appeler-PS
description: Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie. | appeler-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524861"
---
# <a name="call---ps"></a>appeler-PS

Effectue un appel de fonction à l’instruction marquée avec l’étiquette fournie.

## <a name="syntax"></a>Syntaxe



| appeler l\# |
|----------|



 

Où :

-   l \# est une [étiquette-PS](label---ps.md) qui marque le début de la sous-routine à appeler.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| appel                  |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :

1.  Adresse push de la prochaine instruction à la pile d’adresses de retour.
2.  Poursuivez l’exécution à partir de l’instruction marquée par l’étiquette.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




