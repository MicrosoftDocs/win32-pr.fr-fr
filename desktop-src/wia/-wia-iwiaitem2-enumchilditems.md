---
description: crée un objet énumérateur et passe un pointeur vers son interface IEnumWiaItem2 pour les dossiers contenant des éléments dans l’arborescence IWiaItem2 d’un appareil WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2 :: EnumChildItems, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 921a6b6e85f906ef62683038b2bb28dd484d58fd20600b2ff85ae594fafb3cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440417"
---
# <a name="iwiaitem2enumchilditems-method"></a>IWiaItem2 :: EnumChildItems, méthode

crée un objet énumérateur et passe un pointeur vers son interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) pour les dossiers contenant des éléments dans l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) d’un appareil WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCategoryGUID* \[ dans\]
</dt> <dd>

Type : **const GUID \***

Spécifie un pointeur vers une catégorie pour laquelle les nœuds enfants sont énumérés. Si la **valeur est null**, tous les nœuds enfants sont énumérés.

</dd> <dt>

*ppIEnumWiaItem2* \[ à\]
</dt> <dd>

Type : **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) créée par cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Le système d’exécution WIA 2,0 représente chaque périphérique matériel WIA 2,0 sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) . La méthode **IWiaItem2 :: EnumChildItems** permet aux applications d’énumérer les éléments enfants dans l’élément actuel. Toutefois, il ne peut être appliqué qu’aux éléments qui sont des dossiers.

Si le dossier n’est pas vide, il contient une sous-arborescence d’objets [**IWiaItem2**](-wia-iwiaitem2.md) . La méthode **IWiaItem2 :: EnumChildItems** énumère tous les éléments contenus dans le dossier. Elle stocke un pointeur vers un énumérateur dans le paramètre *ppIEnumWiaItem2* . Les applications utilisent le pointeur d’énumérateur pour effectuer l’énumération des éléments enfants d’un objet.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIEnumWiaItem2* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
