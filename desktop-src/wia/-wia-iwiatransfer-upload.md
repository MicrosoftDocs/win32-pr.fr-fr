---
description: Lance un chargement de données d’un élément unique à partir de l’appelant.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer :: upload, méthode (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201490"
---
# <a name="iwiatransferupload-method"></a>IWiaTransfer :: upload, méthode

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

Type : **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Spécifie un pointeur vers les données [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

_pIWiaTransferCallback * \[ dans\]
</dt> <dd>

Tapez : **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
