---
description: Initialise le filtre. Appelé par l’acquisition d’images Windows (WIA) 2,0 avant le téléchargement de chaque image.
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
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519714"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter :: InitializeFilter, méthode

Initialise le filtre. Appelé par l’acquisition d’images Windows (WIA) 2,0 avant le téléchargement de chaque image.

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

Tapez : **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Spécifie un pointeur vers l’élément [_ *IWiaItem2* *](-wia-iwiaitem2.md) qui représente l’image d’aperçu.

</dd> <dt>

*pWiaTransferCallback* \[ dans\]
</dt> <dd>

Tapez : **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est appelée lorsqu’une application appelle le [**Téléchargement**](-wia-iwiatransfer-download.md) et lorsqu’une application appelle la fonction du composant WIA 2,0 Preview `GetNewPreview` . **IWiaImageFilter :: InitializeFilter** stocke les références à *pWiaItem2* et *pWiaTransferCallback* à transmettre à ces fonctions. Ces deux pointeurs d’interface doivent être stockés en tant que variables membres et [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) doit être appelé pour chacun. Les pointeurs d’interface sont également nécessaires dans l’implémentation du filtre de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) et [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) lors de l’acquisition d’images.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
