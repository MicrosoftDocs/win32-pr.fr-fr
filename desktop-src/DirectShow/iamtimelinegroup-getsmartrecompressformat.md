---
description: La méthode GetSmartRecompressFormat récupère le format de compression actuel pour la recompression intelligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'IAMTimelineGroup :: GetSmartRecompressFormat, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8d568bdf0446533df9391c1c0b30382b9a56ecdf0ed788d64c48c38ddf0684a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400727"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a>IAMTimelineGroup :: GetSmartRecompressFormat, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetSmartRecompressFormat` méthode récupère le format de compression actuel pour la recompression intelligente.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppFormat* 
</dt> <dd>

Reçoit un pointeur vers une structure [**SCompFmt0**](scompfmt0.md) , casté en un pointeur vers une valeur long. Si la méthode échoue, la valeur est définie sur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si l’application n’a pas défini de format de compression intelligente (en appelant [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), le format retourné par cette méthode n’est pas valide. Appelez la méthode [**IAMTimelineGroup :: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) pour déterminer si un format de compression a été défini.

Si la méthode est réussie, l’appelant doit libérer le type de média retourné et supprimer la structure [**SCompFmt0**](scompfmt0.md) :


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



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

 

 




