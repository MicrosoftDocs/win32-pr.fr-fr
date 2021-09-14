---
description: La méthode SetRecompFormatFromSource définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup :: SetRecompFormatFromSource, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857716"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>IAMTimelineGroup :: SetRecompFormatFromSource, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetRecompFormatFromSource` méthode définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSource* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineSrc**](iamtimelinesrc.md) de l’objet source.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                             | Description                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                                                                    |
| <dl> <dt>**E \_ aucune \_ chronologie**</dt> </dl>          | Le groupe n’est pas dans une chronologie.<br/>                                                         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>           | Mémoire insuffisante.<br/>                                                                        |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide. Le groupe n’est pas un groupe vidéo ou le fichier source n’a pas de flux vidéo.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode recherche le fichier source associé à *pSource*, récupère le type de média du premier flux vidéo dans le fichier et définit le format de compression de groupe à l’aide de ce type. Pour plus d’informations sur les formats de compression, consultez [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



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

 

 




