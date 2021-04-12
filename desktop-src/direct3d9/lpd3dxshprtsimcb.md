---
description: Fonction de rappel pour la simulation et la compression précalculées par luminance Transfer (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482088"
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

## <a name="remarks"></a>Notes

Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel. Sinon, les dépassements de capacité de la pile peuvent se produire.



|                          |             |
|--------------------------|-------------|
| En-tête                   | d3dx9mesh. h |
| Bibliothèque d'importation           | d3dx9. lib   |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de rappel](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
