---
description: La méthode SetPreviewMode définit le mode Aperçu pour le groupe.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'IAMTimelineGroup :: SetPreviewMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541452"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a>IAMTimelineGroup :: SetPreviewMode, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La méthode SetPreviewMode définit le mode Aperçu pour le groupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fPreview* 
</dt> <dd>

Mode aperçu. Si la **valeur est true**, le groupe est en mode aperçu. Si la **valeur est false**, le groupe est en mode création.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

En mode aperçu, les images sont supprimées pendant les effets lents ou les transitions pour maintenir la vidéo synchronisée avec l’audio. La vidéo peut paraître hachée en conséquence. En mode création, chaque frame est rendu. Le mode création est approprié pour l’écriture de fichiers ; pour l’aperçu à l’écran, la vidéo peut ne pas être synchronisée avec l’audio.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




