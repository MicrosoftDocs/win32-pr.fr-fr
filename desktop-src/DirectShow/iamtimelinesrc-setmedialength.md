---
description: La méthode SetMediaLength spécifie la durée du fichier source.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc :: SetMediaLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543933"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>IAMTimelineSrc :: SetMediaLength, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetMediaLength` méthode spécifie la durée du fichier source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Durée* 
</dt> <dd>

Longueur du média, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Vous pouvez éviter les erreurs de rendu potentielles en définissant la longueur du support avant de définir l’heure d’arrêt du support. Lorsque vous définissez l’heure d’arrêt du support, l’algorithme DES le vérifie par rapport à la longueur du support.

Cette méthode ne valide pas le paramètre de *longueur* , mais la valeur doit être égale à la durée réelle du fichier source. Obtenez la durée du fichier source en appelant [**IMediaDet :: obtenir \_ StreamLength**](imediadet-get-streamlength.md).

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




