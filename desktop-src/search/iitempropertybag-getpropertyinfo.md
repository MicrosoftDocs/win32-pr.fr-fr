---
description: Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés. L’interface IItemPropertyBag est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'IItemPropertyBag :: GetPropertyInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516619"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>IItemPropertyBag :: GetPropertyInfo, méthode

Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés. L’interface [**IItemPropertyBag**](iitempropertybag.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nouvel IProperty* \[ dans\]
</dt> <dd>

Index de base zéro de la première propriété pour laquelle des informations sont demandées.

</dd> <dt>

*cProperties* \[ dans\]
</dt> <dd>

Nombre de propriétés pour lesquelles obtenir des informations. Cet argument spécifie le nombre d’éléments de tableau dans *pPropBag*.

</dd> <dt>

*pPropBag* \[ à\]
</dt> <dd>

Pointeur vers un tableau de structures [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) qui reçoit les informations pour les propriétés.

</dd> <dt>

*pcProperties* \[ à\]
</dt> <dd>

Reçoit un pointeur vers une variable **ULong** qui reçoit le nombre de propriétés pour lesquelles des informations ont été récupérées.

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

 

 




