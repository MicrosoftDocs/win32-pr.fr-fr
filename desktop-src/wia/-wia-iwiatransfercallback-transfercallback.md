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
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527612"
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

Tapez : **[**WiaTransferParams**](-wia-wiatransferparams.md) \** _

Spécifie un pointeur vers une structure [_ *WiaTransferParams* *](-wia-wiatransferparams.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Lorsque cette méthode est implémentée par un filtre de traitement d’image, le minipilote WIA (Windows Image Acquisition) 2,0 l’appelle lors de l’acquisition d’images pour renvoyer des messages de progression à l’application.

**IWiaTransferCallback :: TransferCallback** d’un filtre doit déléguer à la méthode **IWiaTransferCallback :: TransferCallback** du rappel d’application. En règle générale, le flux de filtre filtre les données qui lui sont passées et écrit les données filtrées directement dans le flux de données fourni par l’application. Lorsque le filtre de traitement d’images stocke les données entre les appels à sa méthode [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , il doit également modifier les valeurs *lPercentComplete* et *ulBytesWrittenToCurrentStream* dans la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
