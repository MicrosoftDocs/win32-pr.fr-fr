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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526457"
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

Tapez : **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de l’appelant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si un dossier est téléchargé, tous les éléments enfants de ce dossier sont également transférés. Chaque élément est transféré dans un flux distinct.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




