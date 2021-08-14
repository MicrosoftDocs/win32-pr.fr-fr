---
description: Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés. l’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'IItemPropertyBag :: Read, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226604"
---
# <a name="iitempropertybagread-method"></a>IItemPropertyBag :: Read, méthode

Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés. l’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cProperties* \[ dans\]
</dt> <dd>

Nombre de propriétés à lire. Cet argument spécifie le nombre d’éléments dans les tableaux à *pPropBag*, *pvarValue* et *phrError*.

</dd> <dt>

*pPropBag* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui spécifie les propriétés demandées.

</dd> <dt>

*pvarValue* \[ à\]
</dt> <dd>

Reçoit un pointeur qui retourne un tableau de structures **Variant** qui reçoit les valeurs de propriété.

</dd> <dt>

*phrError* \[ à\]
</dt> <dd>

Pointeur vers un tableau de valeurs **HRESULT** qui reçoit le résultat de chaque lecture de propriété. Il doit y avoir au moins éléments *cProperties* dans ce tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

l’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour prévisualiser les pièces jointes avec un gestionnaire de protocole tiers sur des ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPropertyBag**](iitempropertybag.md) et les api suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




