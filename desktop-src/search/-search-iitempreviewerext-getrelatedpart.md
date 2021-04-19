---
description: Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'IItemPreviewerExt :: GetRelatedPart, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513984"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>IItemPreviewerExt :: GetRelatedPart, méthode

Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwContext* \[ dans\]
</dt> <dd>

Type : **DWORD**

Identificateur de contexte de l’opération. Remplacez la valeur par défaut de **dwContext** pour définir l’identificateur de contexte sur la valeur de votre choix.

</dd> <dt>

*pwszProp* \[ dans\]
</dt> <dd>

Type : **LPCOLESTR**

Pointeur vers la propriété du contenu lié sous la forme d’une chaîne Unicode.

</dd> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Type : **DWORD**

Valeur d’entier long non signé qui contient l’index de base zéro de la partie du corps associée.

</dd> <dt>

*pinfo* \[ out, retval\]
</dt> <dd>

Tapez : **[**LINKINFO**](-search-linkinfo.md) \** _

Reçoit un pointeur vers la structure [_ *LINKINFO* *](-search-linkinfo.md) dans laquelle la méthode retourne des informations sur la transaction. *pinfo* ne doit pas être un pointeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




