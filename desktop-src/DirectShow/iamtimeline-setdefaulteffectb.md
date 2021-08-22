---
description: 'La méthode SetDefaultEffectB définit l’effet par défaut. Cette méthode est équivalente à IAMTimeline :: SetDefaultEffect, mais prend une valeur BSTR plutôt qu’un pointeur vers un GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'IAMTimeline :: SetDefaultEffectB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356874574fd0d960350ab991a97bfd9c6e2641d026da836ecf240bb4391c4a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073123"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a>IAMTimeline :: SetDefaultEffectB, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetDefaultEffectB` méthode définit l’effet par défaut. Cette méthode est équivalente à [**IAMTimeline :: SetDefaultEffect**](iamtimeline-setdefaulteffect.md), mais prend une valeur BSTR plutôt qu’un pointeur vers un GUID.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGuid* 
</dt> <dd>

Valeur BSTR représentant le GUID de l’effet par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




