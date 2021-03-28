---
title: rsq-PS
description: Calcule la racine carrée réciproque (positive uniquement) du scalaire source. | rsq-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974147"
---
# <a name="rsq---ps"></a>rsq-PS

Calcule la racine carrée réciproque (positive uniquement) du scalaire source.

## <a name="syntax"></a>Syntaxe



| rsq DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rsq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

La valeur absolue est prise avant le traitement.

La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 4,0), car les implémentations courantes séparent la mantisse et l’exposant.

La sortie doit être exactement 1,0 si l’entrée est exactement 1,0. Une source de 0,0 donne l’infini.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




