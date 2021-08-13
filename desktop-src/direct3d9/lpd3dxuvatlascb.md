---
description: Fonction de rappel pour UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4473134d7ecf98c50d0c3a69085e7f46344d1d57ff2650c1adbc54c43dba266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458712"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Fonction de rappel pour UVAtlas.

## <a name="syntax"></a>Syntaxe


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Paramètres

\[\]fPercentDone : nombre à virgule flottante compris entre 0 et 1,0 qui représente le pourcentage de calculs effectués (entre 0 et 100 pour cent).

\[dans \] lpUserContext-pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel ; généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

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

 

 
