---
description: La méthode obtenir une fréquence \_ d’images récupère la fréquence d’images du flux actuel. Le flux doit être un flux vidéo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'IMediaDet :: get_FrameRate, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a22be2caf5a66447c9c772861918f1a5dcfe7bc2c81bfdba4f1fefb59f89565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154425"
---
# <a name="imediadetget_framerate-method"></a>IMediaDet :: obtient la \_ méthode de fréquence

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_FrameRate` méthode récupère la fréquence d’images du flux actuel. Le flux doit être un flux vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit la fréquence d’images, en images par seconde.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                             | Description                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                 | L’en-tête de format vidéo ne spécifie pas de fréquence d’images.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argument non valide.<br/>                                  |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>                         |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                                |



 

## <a name="remarks"></a>Remarques

Cette méthode ne peut pas récupérer la fréquence d’images à partir d’un fichier ASF.

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG. Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




