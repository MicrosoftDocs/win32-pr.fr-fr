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
ms.openlocfilehash: 13aad8d0214c65c01237c8e74548c3915af9287c935b53e33c6d229b2da5b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654214"
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

## <a name="remarks"></a>Remarques

dans un fichier exécutable, appelez cette méthode avant d’utiliser les fonctionnalités de débogage DirectShow. Avant la fermeture de l’exécutable, appelez la fonction [**DbgTerminate**](dbgterminate.md) pour nettoyer la bibliothèque de débogage.

Dans une DLL qui établit un lien vers la bibliothèque de classes de base (Strmbase. lib), il n’est pas nécessaire d’appeler cette fonction. La fonction est appelée automatiquement lorsque la DLL est chargée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




