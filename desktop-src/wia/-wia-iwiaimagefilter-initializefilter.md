---
description: Initialise le filtre. appelée par Windows acquisition d’images (WIA) 2,0 avant chaque téléchargement d’image.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter :: InitializeFilter, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 43b818c3adc9926c4ba27f11f5d489ffc0b97e4443d0427e7a12067e9062072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440444"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter :: InitializeFilter, méthode

Initialise le filtre. appelée par Windows acquisition d’images (WIA) 2,0 avant chaque téléchargement d’image.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWiaItem2* \[ dans\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Spécifie un pointeur vers l’élément [**IWiaItem2**](-wia-iwiaitem2.md) qui représente l’image d’aperçu.

</dd> <dt>

*pWiaTransferCallback* \[ dans\]
</dt> <dd>

Type : **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Spécifie un pointeur vers l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée lorsqu’une application appelle le [**Téléchargement**](-wia-iwiatransfer-download.md) et lorsqu’une application appelle la fonction du composant WIA 2,0 Preview `GetNewPreview` . **IWiaImageFilter :: InitializeFilter** stocke les références à *pWiaItem2* et *pWiaTransferCallback* à transmettre à ces fonctions. Ces deux pointeurs d’interface doivent être stockés en tant que variables membres et [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) doit être appelé pour chacun. Les pointeurs d’interface sont également nécessaires dans l’implémentation du filtre de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) et [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) lors de l’acquisition d’images.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
