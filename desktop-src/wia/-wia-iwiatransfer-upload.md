---
description: Lance un chargement de données d’un élément unique à partir de l’appelant.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer :: Télécharger, méthode (Wia. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312781"
---
# <a name="iwiatransferupload-method"></a>IWiaTransfer :: Télécharger, méthode

Lance un chargement de données d’un élément unique à partir de l’appelant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*pSource* \[ dans\]
</dt> <dd>

Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Spécifie un pointeur vers les données [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

*pIWiaTransferCallback* \[ dans\]
</dt> <dd>

Type : **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Spécifie un pointeur vers l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
