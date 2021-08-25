---
description: La méthode SetMediaTypeForVB spécifie le type de média du groupe pour les clients Automation.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'IAMTimelineGroup :: SetMediaTypeForVB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ea47e4edcdfc58e38e61a9f92eb5afac0092ab0cb445f6ff73471e1b65b1480b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905039"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>IAMTimelineGroup :: SetMediaTypeForVB, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetMediaTypeForVB` méthode spécifie le type de média du groupe pour les clients Automation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Val* \[ dans\]
</dt> <dd>

Valeur qui spécifie le type de média. Définissez la valeur sur 0 pour Video ou 1 pour audio.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est destinée aux clients Automation. Pour les applications C++, utilisez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) .

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




