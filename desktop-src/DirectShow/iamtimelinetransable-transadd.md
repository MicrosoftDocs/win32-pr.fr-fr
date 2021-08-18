---
description: La méthode TransAdd ajoute une transition à l’objet. Un objet peut avoir plusieurs transitions, mais il ne doit pas se chevaucher dans le temps. Les transitions doivent se situer dans les limites de temps de l’objet.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable :: TransAdd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 930c3ff43e11cfb71ffce6c7257d0124fe87aeaaf4ae065433f11b860020eeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952748"
---
# <a name="iamtimelinetransabletransadd-method"></a>IAMTimelineTransable :: TransAdd, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `TransAdd` méthode ajoute une transition à l’objet. Un objet peut avoir plusieurs transitions, mais il ne doit pas se chevaucher dans le temps. Les transitions doivent se situer dans les limites de temps de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTrans* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la transition à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                   | Description                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Impossible d’insérer la transition.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *pTrans* n’est pas un pointeur vers une transition.<br/> |



 

## <a name="remarks"></a>Remarques

Si la transition chevauche une transition existante, la méthode retourne E \_ INVALIDARG.

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

[**Interface IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




