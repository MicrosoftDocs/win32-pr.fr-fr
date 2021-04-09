---
description: L’interface IWiaItem2 fournit aux applications les mêmes fonctionnalités que l’interface IWiaItem (la capacité à interroger des appareils pour découvrir leurs fonctionnalités, à accéder aux interfaces de transfert de données et aux propriétés d’élément, et à contrôler l’appareil).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: Interface IWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862678"
---
# <a name="iwiaitem2-interface"></a>Interface IWiaItem2

L’interface **IWiaItem2** fournit aux applications les mêmes fonctionnalités que l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (la capacité à interroger des appareils pour découvrir leurs fonctionnalités, à accéder aux interfaces de transfert de données et aux propriétés d’élément, et à contrôler l’appareil). Il fournit également à l’application la possibilité de créer et d’utiliser dynamiquement des filtres de traitement d’images qui peuvent être des extensions des pilotes de périphériques WIA (Windows Image Acquisition) 2,0 fournis dans Windows Vista.

## <a name="members"></a>Membres

L’interface **IWiaItem2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaItem2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaItem2** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | Vérifie si une extension spécifiée est disponible sur l’ordinateur et si elle peut être utilisée par la méthode [**IWiaItem2 :: GetExtension**](-wia-iwiaitem2-getextension.md) . <br/>                                   |
| [**CreateChildItem**](-wia-iwiaitem2-createchilditem.md)               | Créez un nouvel élément enfant. Ajoute des objets **IWiaItem2** à l’arborescence **IWiaItem2** d’un appareil. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Supprime l’objet **IWiaItem2** actuel de l’arborescence d’objets de l’appareil. <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | Envoie une commande à un périphérique matériel WIA 2,0. <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | Affiche une boîte de dialogue permettant à l’utilisateur de préparer l’acquisition d’images. <br/>                                                                                                                              |
| [**Diagnostic**](-wia-iwiaitem2-diagnostic.md)                         | Actuellement non pris en charge.<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | Crée un objet énumérateur et passe un pointeur vers son interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) pour les dossiers contenant des éléments dans l’arborescence **IWiaItem2** d’un appareil WIA 2,0. <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | Crée un énumérateur qui est utilisé pour déterminer les commandes et les événements pris en charge par un appareil WIA 2,0. <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | La méthode [**IWiaItem2 :: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) crée un énumérateur utilisé pour obtenir des informations sur les événements pour lesquels une application est inscrite.<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | Recherche dans l’arborescence d’un élément des sous-éléments en utilisant le nom comme clé de recherche. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Obtient les interfaces d’extension qui peuvent être fournies avec un pilote de périphérique WIA 2,0. <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | Obtient les informations de catégorie d’un élément. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Obtient les informations de type d’un élément. <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | Obtient l’élément parent dans l’arborescence qui représente un périphérique matériel WIA 2,0. <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Obtient le composant WIA 2,0 Preview.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Obtient l’élément racine d’une arborescence d’objets d’élément utilisés pour représenter un périphérique matériel WIA 2,0. <br/>                                                                                                        |



 

## <a name="remarks"></a>Notes

L’arborescence d’éléments WIA 2,0 qu’une application peut voir est distincte de l’arborescence qui est créée et gérée par un minipilote WIA 2,0. Lorsqu’un minipilote crée une arborescence d’éléments, le service WIA 2,0 utilise cette arborescence d’éléments WIA 2,0 comme guide pour créer des copies identiques qui peuvent être affichées par les applications de création d’images. Les éléments de l’arborescence copiée sont appelés éléments d’application. Les éléments de l’arborescence créés par un minipilote sont appelés éléments de pilote. Dans Windows Vista, les arborescences d’éléments WIA 2,0 sont générées d’objets **IWiaItem2** , chacun d’eux implémentant l’interface **IWiaItem2** ).

L’interface **IWiaItem2** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
