---
title: ICMProgressProcCallback, fonction de rappel
description: La fonction ICMProgressProcCallback est une fonction de rappel fournie par l’application qui signale la progression et permet à l’application d’annuler le traitement des couleurs.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- fonction de rappel ICMProgressProcCallback Windows système de couleurs
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d697bb09b4871f6debb1a41a7ecc3e795307ee544ec30bfaf4b5b44ba0328578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671385"
---
# <a name="icmprogressproccallback-callback-function"></a>ICMProgressProcCallback, fonction de rappel

La fonction **ICMProgressProcCallback** est une fonction de rappel fournie par l’application qui signale la progression et permet à l’application d’annuler le traitement des couleurs.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulMax* 
</dt> <dd>

Spécifie la valeur maximale du compteur de progression (utilisée pour estimer l’achèvement du traitement de la bitmap).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Spécifie la valeur actuelle du compteur de progression (lorsqu’elle est divisée par la valeur maximale, fournit une estimation approximative du pourcentage d’achèvement).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Spécifie les données qui sont passées par l’application à une fonction ICM2, qui la transmet ensuite à la fonction de rappel. Ces données peuvent être utilisées, par exemple, pour identifier la bitmap et traiter la progression signalée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** pour continuer le traitement de la bitmap. La valeur de retour est **false** pour annuler le traitement. Si le traitement est annulé, la fonction appelante retourne la valeur zéro pour indiquer un échec, même si sa mémoire tampon de sortie peut être partiellement remplie.

## <a name="remarks"></a>Remarques

Le nom de cette fonction de rappel est fourni par l’application. Plusieurs fonctions WCS, y compris [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) et [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), appellent cette fonction régulièrement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Fonctions](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
