---
description: Fournit des méthodes qui définissent l’interaction entre une interface utilisateur et les objets d’espace de noms de recherche créés par l’indexeur.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Interface ISearchItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295311"
---
# <a name="isearchitem-interface"></a>Interface ISearchItem

Fournit des méthodes qui définissent l’interaction entre une interface utilisateur et les objets d’espace de noms de recherche créés par l’indexeur.

## <a name="members"></a>Membres

L’interface **ISearchItem** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchItem** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISearchItem** possède ces méthodes.



| Méthode                                                         | Description                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Obtient l’objet **ISearchItem** si l’URL représente une source de données Shell réelle (également appelée extension d’espace de noms Shell).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Obtient l’objet de l’interface utilisateur (IU) de **ISearchItem**.<br/>                                                                        |



 

## <a name="remarks"></a>Notes

[**ISearchItem :: GetParentFolder**](-search-isearchitem-getparentfolder.md) est pris en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisé.

pour prévisualiser les pièces jointes avec un gestionnaire de protocole tiers sur des ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **ISearchItem** et les api suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)et [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
