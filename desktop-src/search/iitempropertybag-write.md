---
description: Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés. l’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'IItemPropertyBag :: Write, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: e8860653244cef53739c7d104405a176c1ec63d2de1d3434b1d25e3206c431aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863108"
---
# <a name="iitempropertybagwrite-method"></a>IItemPropertyBag :: Write, méthode

Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés. l’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cProperties* \[ dans\]
</dt> <dd>

Nombre de propriétés à enregistrer. Cet argument spécifie le nombre d’éléments dans les tableaux à *pPropBag* et *pvarValue*.

</dd> <dt>

*pPropBag* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui spécifie les propriétés à enregistrer.

</dd> <dt>

*pvarValue* \[ dans\]
</dt> <dd>

Pointeur vers un **Variant** dont le type dépend du type de données des informations de propriété qu’il contient.

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

 

 




