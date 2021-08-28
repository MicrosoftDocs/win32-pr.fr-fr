---
description: Supprime l’objet IWiaItem2 actuel de l’arborescence d’objets de l’appareil.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: IWiaItem2 ::D méthode eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592999"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2 ::D méthode eleteItem

Supprime l’objet [**IWiaItem2**](-wia-iwiaitem2.md) actuel de l’arborescence d’objets de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

le système d’exécution de l’acquisition d’images Windows (WIA) 2,0 représente chaque périphérique matériel wia 2,0 connecté à l’ordinateur de l’utilisateur sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) . Un périphérique WIA 2,0 donné peut ou non autoriser les applications à supprimer des objets **IWiaItem2** de son arborescence. Les éléments qui ont des enfants ne peuvent pas être supprimés. L’interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) doit être utilisée pour interroger l’appareil à la fonctionnalité de suppression d’éléments.

Si l’appareil prend en charge la suppression d’élément dans son arborescence [**IWiaItem2**](-wia-iwiaitem2.md) , appelez la méthode **IWiaItem2 ::D eleteitem** pour supprimer l’objet **IWiaItem2** . Notez que cette méthode supprime uniquement un objet une fois que toutes les références à l’objet ont été libérées. Si la suppression d’un élément a échoué, E \_ DELETEITEM est retourné. La valeur numérique de cette erreur n’est pas encore définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




