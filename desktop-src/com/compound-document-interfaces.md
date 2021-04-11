---
title: Interfaces de document composé
description: Interfaces de document composé
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eecb44945ec666a38ebf59544caf2e09eb5930d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031915"
---
# <a name="compound-document-interfaces"></a>Interfaces de document composé

Les tableaux suivants répertorient les interfaces implémentées par les conteneurs OLE, les serveurs OLE et les objets de document composé. Les interfaces requises doivent être implémentées sur les composants pour lesquels elles sont répertoriées. Toutes les autres fonctionnalités sont facultatives. Toutefois, si vous souhaitez inclure une fonctionnalité particulière dans votre application, vous devez implémenter les interfaces indiquées pour cette fonctionnalité dans le tableau ci-dessous. Toutes les autres interfaces sont requises uniquement si vous incluez une fonctionnalité particulière.

Le tableau suivant répertorie les comportements obligatoires et facultatifs pour les conteneurs OLE et les interfaces que vous devez implémenter pour chacun d’entre eux.



| Comportement                               | Interfaces                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportements requis<br/>          | [**Renvoyé**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| Filtrage des messages<br/>           | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| Liaison<br/>                     | aucun<br/>                                                                                                                                                         |
| Lier à des objets incorporés<br/> | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| Activation sur place<br/>         | [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| Glisser-déplacer<br/>               | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

Le tableau suivant répertorie les comportements obligatoires et facultatifs pour les serveurs OLE et leurs objets de document composés et les interfaces que vous devez implémenter pour chacun d’entre eux. Le tableau distingue les serveurs OLE et leurs objets afin de clarifier le composant qui implémente les interfaces. Le tableau indique également les différentes exigences des objets fournis par les serveurs out-of-process et in-process.



| Fonctionnalité                        | Serveur OLE                                                                                                                                | Objet (hors processus)                                                                                                                         | Objet (in-process)                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comportements requis             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| Filtrage des messages<br/>   | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| Liaison<br/>             | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**IExternalConnection**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| Activation sur place<br/> |                                                                                                                                           | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| Glisser-déplacer<br/>       | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

