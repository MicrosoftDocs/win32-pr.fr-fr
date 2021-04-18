---
description: Prototype de fonction utilisé par D3DXComputeIMTFromSignal pour décrire un signal défini par l’utilisateur dans l’espace u, v d’un maillage d’entrée. La fonction évalue un signal procédural de la dimension uSignalDimension à la coordonnée u, v fournie.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106540792"
---
# <a name="lpd3dximtsignalcallback"></a>LPD3DXIMTSIGNALCALLBACK

Prototype de fonction utilisé par [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) pour décrire un signal défini par l’utilisateur dans l’espace u, v d’un maillage d’entrée. La fonction évalue un signal procédural de la dimension uSignalDimension à la coordonnée u, v fournie.

## <a name="syntax"></a>Syntaxe


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a>Paramètres

\[dans \] UV-A, pointeur vers un vecteur qui contient la coordonnée de texture de vertex.

\[dans \] uPrimitiveId, index du triangle d’entrée sur la maille pour laquelle le signal doit être calculé.

\[en \] uSignalDimension-nombre de valeurs float à stocker dans le tableau de données de signal (pfSignalOut).

\[dans \] pUserData, le pointeur pUserData est passé à [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).

\[out \] pfSignalOut : tableau de valeurs float qui contient les données de signal.

## <a name="return-value"></a>Valeur renvoyée

Cette fonction doit être implémentée pour retourner S \_ OK.

## <a name="remarks"></a>Notes

Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel. Sinon, les dépassements de capacité de la pile peuvent se produire.



|                |             |
|----------------|-------------|
| En-tête         | d3dx9mesh. h |
| Bibliothèque d'importation | d3dx9. lib   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de rappel](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
