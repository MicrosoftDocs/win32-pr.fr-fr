---
description: Obtient l’élément de recherche pour les données spécifiées. Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'ISearchProtocolUI :: GetSearchItemForUrl, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295310"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>ISearchProtocolUI :: GetSearchItemForUrl, méthode

Obtient l’élément de recherche pour les données spécifiées. Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcwszURL* \[ dans\]
</dt> <dd>

Type : **LPCOLESTR**

Pointeur vers une chaîne Unicode terminée par des données NULL contenant l’élément de recherche pour l’URL accédée.

</dd> <dt>

*pPropertyBag* \[ dans\]
</dt> <dd>

Type : **IItemPropertyBag \***

Pointeur vers un objet [**IItemPropertyBag**](iitempropertybag.md) qui contient des informations sur l’élément de recherche, y compris les propriétés de l’élément.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Type : **[ **ISearchItem**](-search-isearchitem.md)\*\***

Reçoit l’adresse d’un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) créé par cette méthode. Cet objet contient des informations sur l’élément de recherche, telles que le nom de fichier de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

la méthode **ISearchProtocolUI :: GetSearchItemForUrl** est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**ISearchProtocolUI**](-search-isearchprotocolui.md) et les api suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




