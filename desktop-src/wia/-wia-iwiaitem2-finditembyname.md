---
description: Recherche dans l’arborescence d’un élément des sous-éléments en utilisant le nom comme clé de recherche.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2 :: FindItemByName, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522185"
---
# <a name="iwiaitem2finditembyname-method"></a>IWiaItem2 :: FindItemByName, méthode

Recherche dans l’arborescence d’un élément des sous-éléments en utilisant le nom comme clé de recherche.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*bstrFullItemName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie le nom de l’élément à rechercher.

</dd> <dt>

*ppIWiaItem2* \[ à\]
</dt> <dd>

Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément trouvé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode recherche l’arborescence des sous-éléments de l’élément actuel en utilisant le nom comme clé de recherche. Si **IWiaItem2 :: FindItemByName** trouve l’élément spécifié par *bstrFullItemName*, il stocke l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément dans le paramètre *ppIWiaItem2* .

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
