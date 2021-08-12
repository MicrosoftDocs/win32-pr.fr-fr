---
description: Fournit la progression et d’autres notifications pendant un transfert.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback :: TransferCallback, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440317"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>IWiaTransferCallback :: TransferCallback, méthode

Fournit la progression et d’autres notifications pendant un transfert.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*pWiaTransferParams* \[ dans\]
</dt> <dd>

Type : **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

Spécifie un pointeur vers une structure [**WiaTransferParams**](-wia-wiatransferparams.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

lorsque cette méthode est implémentée par un filtre de traitement d’image, le minipilote WIA (Windows image acquisition) 2,0 l’appelle lors de l’acquisition d’images pour renvoyer des messages de progression à l’application.

**IWiaTransferCallback :: TransferCallback** d’un filtre doit déléguer à la méthode **IWiaTransferCallback :: TransferCallback** du rappel d’application. En règle générale, le flux de filtre filtre les données qui lui sont passées et écrit les données filtrées directement dans le flux de données fourni par l’application. Lorsque le filtre de traitement d’images stocke les données entre les appels à sa méthode [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , il doit également modifier les valeurs *lPercentComplete* et *ulBytesWrittenToCurrentStream* dans la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
