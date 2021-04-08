---
description: Autorise le traitement d’une commande de transformation rencontrée dans un modèle d’aperçu.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt ::P méthode rocessTransformCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862173"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt ::P méthode rocessTransformCommand

Autorise le traitement d’une commande de transformation rencontrée dans un modèle d’aperçu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwContext* \[ dans\]
</dt> <dd>

Type : **DWORD**

Identificateur de contexte de l’opération. Remplacez la valeur par défaut de *dwContext* pour définir l’identificateur de contexte sur la valeur de votre choix.

</dd> <dt>

*pwszName* \[ dans\]
</dt> <dd>

Type : **LPCOLESTR**

Pointeur vers le nom de la commande de transformation sous la forme d’une chaîne Unicode.

</dd> <dt>

*pwszArg* \[ dans\]
</dt> <dd>

Type : **LPCOLESTR**

Pointeur vers l’argument comme une chaîne Unicode.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Type : **Variant \** _

Pointeur vers la variante de résultat. _pvarResult * ne doit pas être un pointeur **null** .

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

 

 




