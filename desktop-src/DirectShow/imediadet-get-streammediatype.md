---
description: La \_ méthode obtenir StreamMediaType récupère le type de média du flux actuel. Tous les flux vidéo sont convertis en types VIDEOINFOHEADER, et tous les flux audio sont convertis en types WAVEFORMATEX.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'IMediaDet :: get_StreamMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e62f7c7d5a6881647280e17d7ae21c442ae57c21a0c48470e255434007c5db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154181"
---
# <a name="imediadetget_streammediatype-method"></a>IMediaDet :: \_ StreamMediaType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_StreamMediaType` méthode récupère le type de média du flux actuel. Tous les flux vidéo sont convertis en types [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , et tous les flux audio sont convertis en types [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui est remplie avec le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

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

 

 
