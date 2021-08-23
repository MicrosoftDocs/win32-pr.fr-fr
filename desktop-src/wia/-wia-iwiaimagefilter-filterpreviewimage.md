---
description: Filtre l’image d’aperçu.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter :: FilterPreviewImage, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 96b1d8ce92a847dcd4ffcebca6b45df2b652ad74c1216fc60b8aac72bb6a12ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659719"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>IWiaImageFilter :: FilterPreviewImage, méthode

Filtre l’image d’aperçu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Non utilisé. Définit la valeur 0.

</dd> <dt>

*pWiaChildItem2* \[ dans\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Élément traité.

</dd> <dt>

*InputImageExtents* \[ dans\]
</dt> <dd>

Type : **Rect**

Coordonnées (sur la zone d’acquisition physique) de l’image que le composant d’aperçu met en cache en interne.

</dd> <dt>

*pInputStream* \[ dans\]
</dt> <dd>

Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Pointeur vers l’interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) pour les données d’image mises en cache qui sont filtrées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

N’appelez pas cette méthode directement à partir de votre application.

*pWiaChildItem2* doit être un élément enfant du *pWiaItem2* qui a été passé dans [**IWiaImageFilter :: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* est nécessaire, car le filtre de traitement d’image est chargé de couper la zone d’image que *pWiaChildItem2* représente à partir des données d’image transmises par le biais de *pInputStream*.

Une application doit s’assurer que *pWiaChildItem2* a le même format d’image (WIA \_ \_ ), la résolution (WIA \_ IPS \_ XRES et WIA \_ \_ YRES) et la profondeur de bit (WIA de la \_ Loi WIA), \_ car *pWiaItem2* avait été passé dans [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
