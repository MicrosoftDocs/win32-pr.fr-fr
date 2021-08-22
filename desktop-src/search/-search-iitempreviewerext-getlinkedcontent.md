---
description: Autorise l’extension à du contenu riche pour une propriété.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'IItemPreviewerExt :: GetLinkedContent, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9b99d46d33ba66a9669d47021661b0a359fb2ca98d418735238e2baf3dc9e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094920"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>IItemPreviewerExt :: GetLinkedContent, méthode

Autorise l’extension à du contenu riche pour une propriété.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwContext* \[ dans\]
</dt> <dd>

Type : **DWORD**

Identificateur de contexte de l’opération. Remplacez la valeur par défaut de *dwContext* pour définir l’identificateur de contexte sur la valeur de votre choix.

</dd> <dt>

*pwszProp* \[ dans\]
</dt> <dd>

Type : **LPCOLESTR**

Pointeur vers la propriété du contenu lié sous la forme d’une chaîne Unicode.

</dd> <dt>

*pinfo* \[ out, retval\]
</dt> <dd>

Type : **[ **LINKINFO**](-search-linkinfo.md)\***

Reçoit un pointeur vers la structure [**LINKINFO**](-search-linkinfo.md) dans laquelle la méthode retourne des informations sur la transaction. *pinfo* ne doit pas être un pointeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les api suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




