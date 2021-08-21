---
description: La méthode GetCutPoint récupère le point de coupe.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'IAMTimelineTrans :: GetCutPoint, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0582446a3f88b3692b50ca97d033a85d1dfca475051e3538c39d41003e788ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154793"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>IAMTimelineTrans :: GetCutPoint, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetCutPoint` méthode récupère le point de coupe. Si vous affichez une transition comme une coupe, le point de coupe est l’heure à laquelle la transition passe d’une source à la suivante. Par défaut, cette valeur est le milieu de la transition. Par exemple, dans une transition qui s’étend sur une seconde, le point de coupe par défaut est de 0,5 secondes dans la transition.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTLTime* 
</dt> <dd>

Reçoit le point de coupe par rapport à l’heure de début de la transition, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                               | Description                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Le point de coupe n’a pas été défini. La valeur retournée est la valeur par défaut.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Le point de coupe a été défini sur une valeur autre que la valeur par défaut.<br/>            |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/>                                          |



 

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutsOnly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




