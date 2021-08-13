---
description: La méthode EnableEffects active ou désactive tous les effets de la chronologie. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: 'IAMTimeline :: EnableEffects, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a6cce5d06b65bb6a7b3b6063e6cf6b9190e268ba7ee5f5abadf4343be2cf64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401110"
---
# <a name="iamtimelineenableeffects-method"></a>IAMTimeline :: EnableEffects, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `EnableEffects` méthode active ou désactive tous les effets de la chronologie. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut activer ou désactiver les effets. Si la **valeur est true**, les effets sont activés. Si la **valeur est false**, les effets sont désactivés.

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

 

 




