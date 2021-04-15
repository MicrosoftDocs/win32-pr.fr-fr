---
title: entrée dcl_usage (SM1, SM2, SM3-vs ASM)
description: Déclarez l’association entre une utilisation d’élément de vertex et un index d’utilisation pour un registre d’entrée de nuanceur de sommets.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38113846fe62c37247bb2d3ca522a34dc9282441
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463354"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>\_entrée d’utilisation DCL (SM1, SM2, SM3-vs ASM)

Déclarez l’association entre une utilisation d’élément de vertex et un index d’utilisation pour un registre d’entrée de nuanceur de sommets.

## <a name="syntax"></a>Syntaxe



|                                |
|--------------------------------|
| \_index d’utilisation de l’utilisation de DCL \[ \_ \]\# |



 

Où :

-   l' \_ utilisation de la configuration DCL identifie la manière dont les données du Registre sont utilisées. Il s’agit de la même valeur que les membres de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sans le préfixe D3DDECLUSAGE.
-   l' \_ index d’utilisation est un index d’entiers facultatif compris entre 0 et 15. Il modifie les données d’utilisation. L’index correspond à l’index d’utilisation dans une déclaration de vertex. Voir la [déclaration de vertex (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). L’index est ajouté à la valeur d’utilisation (DCL \_ ) sans espace. S’il n’est pas fourni, il est supposé être égal à 0.
-   v \# est un [Registre d’entrée](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| utilisation de DCL \_             | x    | x    | x    | x     | x    | x     |



 

Toutes les \_ instructions d’utilisation de la DCL doivent apparaître avant la première instruction exécutable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 