---
description: Lance un téléchargement de données vers l’appelant.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: IWiaTransfer ::D méthode lécharger (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 2863915b850588d4db018693d9081ed2907d644a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231041"
---
# <a name="iwiatransferdownload-method"></a>IWiaTransfer ::D méthode lécharger

Lance un téléchargement de données vers l’appelant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Download(
  [in] LONG                 lFlags,
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

*pIWiaTransferCallback* \[ dans\]
</dt> <dd>

Type : **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Spécifie un pointeur vers l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si un dossier est téléchargé, tous les éléments enfants de ce dossier sont également transférés. Chaque élément est transféré dans un flux distinct.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




