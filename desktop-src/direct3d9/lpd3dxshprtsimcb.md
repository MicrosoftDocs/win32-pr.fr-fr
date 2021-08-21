---
description: Fonction de rappel pour la simulation et la compression précalculées par luminance Transfer (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799332"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Fonction de rappel pour la simulation et la compression précalculées par luminance Transfer (PRT).

## <a name="syntax"></a>Syntaxe


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Paramètres

fPercentDone : nombre à virgule flottante compris entre 0 et 1,0 qui représente le pourcentage de calculs effectués (entre 0 et 100 pour cent).

lpUserContext-pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

## <a name="return-value"></a>Valeur renvoyée

Cette fonction doit être implémentée pour retourner \_ OK pour continuer à exécuter le simulateur. Toute autre valeur arrêtera le simulateur.

## <a name="remarks"></a>Remarques

veillez à spécifier la convention d’appel des [**Types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel. Sinon, les dépassements de capacité de la pile peuvent se produire.



| Condition requise                         | Valeur            |
|--------------------------|-------------|
| En-tête                   | d3dx9mesh. h |
| Bibliothèque d'importation           | d3dx9. lib   |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de rappel](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
