---
description: Prototype de fonction utilisé par D3DXComputeIMTFromSignal pour décrire un signal défini par l’utilisateur dans l’espace u, v d’un maillage d’entrée. La fonction évalue un signal procédural de la dimension uSignalDimension à la coordonnée u, v fournie.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e4f6ffaa4c844e755d489aae52dd13b8390da1145734d50f5865bbe0e3cfc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728506"
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

## <a name="remarks"></a>Remarques

veillez à spécifier la convention d’appel des [**Types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel. Sinon, les dépassements de capacité de la pile peuvent se produire.



| Condition requise               | Valeur            |
|----------------|-------------|
| En-tête         | d3dx9mesh. h |
| Bibliothèque d'importation | d3dx9. lib   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de rappel](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
