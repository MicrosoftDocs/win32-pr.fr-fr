---
description: Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés. L’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
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
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112391"
---
# <a name="iitempropertybagwrite-method"></a>IItemPropertyBag :: Write, méthode

Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés. L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

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

## <a name="remarks"></a>Notes

L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPropertyBag**](iitempropertybag.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




