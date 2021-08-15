---
description: Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche. cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Interface IItemPropertyBag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2657fea53c4e7021e17df4b74cc210bd8547180566ff579524f85b7663a0c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226560"
---
# <a name="iitempropertybag-interface"></a>Interface IItemPropertyBag

Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche. cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

## <a name="members"></a>Membres

L’interface **IItemPropertyBag** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPropertyBag** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IItemPropertyBag** possède ces méthodes.



| Méthode                                                      | Description                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Obtient le nombre de propriétés dans le conteneur de propriétés.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés.<br/> |
| [**Lire**](iitempropertybag-read.md)                       | Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés.<br/>                   |
| [**Écriture**](iitempropertybag-write.md)                     | Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés.<br/>                  |



 

## <a name="remarks"></a>Remarques

l’interface **IItemPropertyBag** est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour prévisualiser les pièces jointes avec un gestionnaire de protocole tiers sur des ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **IItemPropertyBag** et les api suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LINKTYPE**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
