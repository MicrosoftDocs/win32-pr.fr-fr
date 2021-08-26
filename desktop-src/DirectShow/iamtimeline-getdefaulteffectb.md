---
description: 'La méthode GetDefaultEffectB récupère l’effet par défaut. Cette méthode est équivalente à IAMTimeline :: GetDefaultEffect, mais elle reçoit une valeur BSTR plutôt qu’un GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'IAMTimeline :: GetDefaultEffectB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f0abfac297817b4e93b4eabe5bd2517c22ab363498bbbe35f2b5ae449524ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997769"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>IAMTimeline :: GetDefaultEffectB, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetDefaultEffectB` méthode récupère l’effet par défaut. Cette méthode est équivalente à [**IAMTimeline :: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), mais elle reçoit une valeur **BSTR** plutôt qu’un GUID.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguid* \[ out, retval\]
</dt> <dd>

Reçoit une valeur **BSTR** représentant le GUID de l’effet par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode alloue de la mémoire pour la chaîne. L’application doit appeler **SysFreeString** pour libérer la mémoire.

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

 

 




