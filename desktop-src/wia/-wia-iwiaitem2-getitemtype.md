---
description: Obtient les informations de type d’un élément.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2 :: GetItemType, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751781"
---
# <a name="iwiaitem2getitemtype-method"></a>IWiaItem2 :: GetItemType, méthode

Obtient les informations de type d’un élément.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pItemType* \[ à\]
</dt> <dd>

Type : **long \** _

Reçoit un pointeur vers un _ *long** qui contient une combinaison d’indicateurs de type. Consultez [**indicateurs de type d’élément WIA**](-wia-wia-item-type-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Chaque objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence hiérarchique d’objets associés à un périphérique matériel WIA (Windows Image Acquisition) 2,0 a un type de données spécifique. Les objets Item représentent des dossiers et des fichiers. Les dossiers contiennent des objets de fichier. Les objets fichier contiennent des données acquises par l’appareil, telles que des images et des sons. Cette méthode permet aux applications d’identifier le type d’un élément dans une arborescence hiérarchique d’objets Item dans un appareil.

Un élément peut avoir plusieurs types. Par exemple, un élément qui représente un fichier audio aura les attributs de type [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




