---
description: La fonction DbgInitialise initialise la bibliothèque de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: DbgInitialise, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544013"
---
# <a name="dbginitialise-function"></a>DbgInitialise fonction)

La fonction **DbgInitialise** initialise la bibliothèque de débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hInst* 
</dt> <dd>

Handle de l’instance de module.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Dans un fichier exécutable, appelez cette méthode avant d’utiliser les fonctionnalités de débogage DirectShow. Avant la fermeture de l’exécutable, appelez la fonction [**DbgTerminate**](dbgterminate.md) pour nettoyer la bibliothèque de débogage.

Dans une DLL qui établit un lien vers la bibliothèque de classes de base (Strmbase. lib), il n’est pas nécessaire d’appeler cette fonction. La fonction est appelée automatiquement lorsque la DLL est chargée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




