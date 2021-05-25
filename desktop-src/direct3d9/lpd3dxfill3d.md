---
description: 'LPD3DXFILL3D : type de fonction utilisé par les fonctions de remplissage de texture.'
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed5845f04486a6ac9cf1c984178fb0ed98447a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342764"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

Type de fonction utilisé par les fonctions de remplissage de texture.

## <a name="syntax"></a>Syntaxe


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Paramètres

Moue-pointeur vers un vecteur, que la fonction utilise pour retourner son résultat. X, Y, Z et W sont mappés respectivement à R, G, B et A.

pTexCoord-pointeur vers un vecteur contenant les coordonnées du Texel en cours d’évaluation. Les composants de coordonnée de texture des textures et volumes sont compris entre 0 et 1. Les composants de coordonnée de texture pour les textures de cube sont compris entre-1 et 1.

pTexelSize-pointeur vers un vecteur contenant les dimensions du Texel actuel.

pData-pointeur vers les données utilisateur.

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel. Sinon, les dépassements de capacité de la pile peuvent se produire.



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3dx9tex. h |
| Bibliothèque d'importation           | d3dx9. lib  |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de rappel](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
