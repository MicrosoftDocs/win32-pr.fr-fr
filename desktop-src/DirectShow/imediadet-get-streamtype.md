---
description: La \_ méthode obtenir StreamType récupère l’identificateur global unique (Guid) pour le type de média du flux actuel.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'IMediaDet :: get_StreamType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853870"
---
# <a name="imediadetget_streamtype-method"></a>IMediaDet :: \_ StreamType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_StreamType` méthode récupère l’identificateur global unique (Guid) pour le type de média du flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit le GUID de type principal pour le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode récupère le membre **MajorType** de la structure [**du \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . La structure du **\_ \_ type de média am** décrit le format du flux, et le membre **MajorType** est un GUID qui indique la catégorie générale, telle que l’audio ou la vidéo. Pour un flux vidéo, le GUID est la \_ vidéo de MediaType. Pour le son, il s’agit de l’audio de MEDIATYPE \_ . Pour récupérer l’ensemble de la structure du **\_ \_ type de média am** , appelez la méthode [**IMediaDet :: obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md) .

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG. Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




