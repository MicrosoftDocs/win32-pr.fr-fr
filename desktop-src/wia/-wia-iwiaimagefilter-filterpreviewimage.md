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
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523137"
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

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

N’appelez pas cette méthode directement à partir de votre application.

*pWiaChildItem2* doit être un élément enfant du *pWiaItem2* qui a été passé dans [**IWiaImageFilter :: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* est nécessaire, car le filtre de traitement d’image est chargé de couper la zone d’image que *pWiaChildItem2* représente à partir des données d’image transmises par le biais de *pInputStream*.

Une application doit s’assurer que *pWiaChildItem2* a le même format d’image (WIA \_ \_ ), la résolution (WIA \_ IPS \_ XRES et WIA \_ \_ YRES) et la profondeur de bit (WIA de la \_ Loi WIA), \_ car *pWiaItem2* avait été passé dans [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
