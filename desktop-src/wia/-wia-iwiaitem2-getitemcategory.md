---
description: Obtient les informations de catégorie d’un élément.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2 :: GetItemCategory, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516885"
---
# <a name="iwiaitem2getitemcategory-method"></a>IWiaItem2 :: GetItemCategory, méthode

Obtient les informations de catégorie d’un élément.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItemCategoryGUID* \[ à\]
</dt> <dd>

Type : **GUID \** _

Reçoit un pointeur vers le GUID qui identifie la catégorie de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Chaque objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence hiérarchique d’objets associés à un périphérique matériel WIA (Windows Image Acquisition) 2,0 a une catégorie spécifique. Cette méthode permet aux applications d’identifier la catégorie d’un élément dans une arborescence hiérarchique d’objets Item dans un appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




