---
description: 'La méthode SplitAt2 fractionne l’objet à l’heure spécifiée. Cette méthode est équivalente à IAMTimelineSplittable :: SplitAt, mais prend une valeur REFTIME.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'IAMTimelineSplittable :: SplitAt2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542254"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>IAMTimelineSplittable :: SplitAt2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SplitAt2` méthode fractionne l’objet à l’heure spécifiée. Cette méthode est équivalente à [**IAMTimelineSplittable :: SplitAt**](iamtimelinesplittable-splitat.md), mais prend une valeur [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Time* 
</dt> <dd>

Heure à laquelle fractionner l’objet, en secondes, par rapport au début de la chronologie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Rien à fractionner.<br/>                       |
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L’objet n’existe pas pour l’instant.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




