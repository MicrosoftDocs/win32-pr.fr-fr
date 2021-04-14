---
title: Contrôles ActiveX
description: Contrôles ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382911"
---
# <a name="activex-controls"></a>Contrôles ActiveX

La technologie des contrôles ActiveX repose sur une Fondation composée d’objets COM, connectables, de documents composés, de pages de propriétés, d’Automation OLE, de persistance d’objets et d’objets de police et d’image fournis par le système. Comme résumé ci-dessous, chacune de ces technologies de base joue un rôle dans les contrôles.

<dl> <dt>

<span id="COM"></span><span id="com"></span>COM
</dt> <dd>

Un contrôle est essentiellement un objet COM qui expose l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , par l’intermédiaire de laquelle les clients peuvent obtenir des pointeurs vers ses autres interfaces. Les contrôles peuvent prendre en charge la gestion des licences via [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) et l’auto-inscription. Pour plus d’informations sur COM, les licences et l’inscription automatique, consultez [modèle d’objet de composant](the-component-object-model.md) .

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objets connectables
</dt> <dd>

Les contrôles peuvent prendre en charge les interfaces sortantes via des objets connectables afin que le contrôle puisse communiquer avec son client. Par exemple, une interface sortante peut déclencher une action dans le client, notifier le client d’une modification du contrôle ou demander une autorisation au client avant que le contrôle ne prenne une mesure. Pour plus d’informations sur le fonctionnement des objets connectables, consultez [événements dans com et objets connectables](events-in-com-and-connectable-objects.md) .

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transfert de données uniforme
</dt> <dd>

Les contrôles peuvent prendre en charge les glisser-déplacer dans un conteneur avec l’aide de leur conteneur. Pour plus d’informations sur le glisser-déplacer, consultez [**IOleInPlaceObjectWindowless :: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documents composés
</dt> <dd>

Un contrôle peut être un objet actif sur place qui peut être incorporé dans un client contenant. Un utilisateur final active le contrôle pour lancer une action dans l’application conteneur. Pour plus d’informations sur l’activation sur place et d’autres interfaces de document composé, consultez [documents composés](compound-documents.md) .

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Pages de propriétés
</dt> <dd>

Les contrôles peuvent fournir des pages de propriétés afin que les utilisateurs finaux puissent afficher et modifier les propriétés du contrôle. Pour plus d’informations sur le fonctionnement des pages de propriétés, consultez pages de propriétés [et feuilles de propriétés](property-pages-and-property-sheets.md) .

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE Automation
</dt> <dd>

Les contrôles peuvent assurer la programmabilité via OLE Automation afin que les clients puissent tirer parti des fonctionnalités du contrôle par le biais d’un langage de programmation fourni par le client. Pour plus d’informations sur l’automatisation OLE, consultez la section OLE Automation.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Stockage persistant
</dt> <dd>

Un contrôle peut implémenter une ou plusieurs des interfaces de persistance multiples pour prendre en charge la persistance de son état. L’implémenteur de contrôle doit décider quels types de persistance sont les plus importants et implémenter les interfaces de persistance appropriées. Le client décide de l’interface qu’il préfère utiliser. Pour plus d’informations sur toutes les interfaces de persistance, consultez [modèle d’objet de composant](the-component-object-model.md) .

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objets de police et d’image
</dt> <dd>

Les contrôles peuvent utiliser ces objets fournis par le système pour fournir une représentation visuelle d’eux-mêmes au sein du client. L’objet font implémente plusieurs interfaces, y compris [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) et [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Un objet font peut être créé avec [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). L’objet Picture implémente également plusieurs interfaces, notamment [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) et [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Un objet image peut être créé à l’aide de [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) et peut être chargé à partir d’un flux avec [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

Il est important de comprendre que ces fonctionnalités peuvent être utilisées dans n’importe quel objet OLE. Il n’est pas nécessaire d’implémenter un contrôle pour pouvoir utiliser ces fonctionnalités. En outre, la seule interface requise sur un contrôle est IUnknown. Le contrôle prend éventuellement en charge d’autres interfaces en fonction de la nécessité de prendre en charge les fonctionnalités associées.

Outre ces fonctionnalités, les interfaces et fonctions suivantes sont spécifiques à la technologie des contrôles : [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)et [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). En outre, certains contrôles sont un ensemble de normes pour les propriétés et les méthodes qu’un contrôle ou un conteneur de contrôle peut prendre en charge.

> [!Note]  
> La bibliothèque système OleAut32.dll contient des implémentations des fonctions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)et [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). En outre, OleAut32.dll contient les implémentations des objets de police et d’image standard, ainsi qu’une bibliothèque de types pour toutes les interfaces utilisées avec les contrôles, ainsi que les structures de données et types de données supplémentaires.

 

Pour plus d'informations, voir les rubriques suivantes :

-   [Architecture des contrôles ActiveX](activex-controls-architecture.md)
-   [Interfaces de contrôles ActiveX](activex-controls-interfaces.md)
-   [Propriétés et méthodes](properties-and-methods.md)
-   [Événements de contrôle](control-events.md)
-   [Représentation visuelle](visual-representation.md)
-   [Gestion du clavier pour les contrôles](keyboard-handling-for-controls.md)
-   [Persistance](persistence.md)
-   [Inscription et licences](registration-and-licensing.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions relatives au contrôle ActiveX et au conteneur de contrôles](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 