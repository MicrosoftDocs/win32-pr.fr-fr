---
title: RET-PS
description: Prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution. Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971546"
---
# <a name="ret---ps"></a>RET-PS

Prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution. Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.

## <a name="syntax"></a>Syntaxe



| Av |
|-----|



 

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Av                   |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction prend l’adresse d’une instruction de la pile d’adresses de retour et poursuit son exécution. Dans le cas de la fonction main, cette instruction arrête l’exécution du nuanceur.

L’instruction RET consomme un emplacement d’instruction de nuanceur de sommets.

Si un nuanceur ne contient pas de sous-routines, l’utilisation de RET à la fin du programme principal est facultative.

Plusieurs instructions return ne sont pas autorisées dans le programme principal ou dans une sous-routine, la première instruction return est traitée comme la fin du programme ou de la sous-routine principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




