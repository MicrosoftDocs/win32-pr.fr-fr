---
description: Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche. Cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
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
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112387"
---
# <a name="iitempropertybag-interface"></a>Interface IItemPropertyBag

Définit des méthodes pour obtenir des informations sur les propriétés d’un élément de recherche. Cette interface est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

## <a name="members"></a>Membres

L’interface **IItemPropertyBag** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPropertyBag** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IItemPropertyBag** possède ces méthodes.



| Méthode                                                      | Description                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Obtient le nombre de propriétés dans le conteneur de propriétés.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Obtient les informations requises pour lire ou enregistrer les propriétés dans le conteneur de propriétés.<br/> |
| [**En lecture**](iitempropertybag-read.md)                       | Provoque la lecture d’une ou plusieurs propriétés à partir du conteneur des propriétés.<br/>                   |
| [**Ecrire**](iitempropertybag-write.md)                     | Entraîne l’enregistrement d’une ou plusieurs propriétés dans le conteneur de propriétés.<br/>                  |



 

## <a name="remarks"></a>Notes

L’interface **IItemPropertyBag** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **IItemPropertyBag** et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) et [**ISearchItem**](-search-isearchitem.md) , les structures [**LINKINFO**](-search-linkinfo.md) et [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
