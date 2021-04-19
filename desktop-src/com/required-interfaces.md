---
title: Interfaces requises (COM)
description: Interfaces requises
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df483f8c8aa5eb5ecb6799b834fccab42f42ca1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106510109"
---
# <a name="required-interfaces-com"></a>Interfaces requises (COM)

Le tableau ci-dessous répertorie les interfaces de conteneur de contrôles ActiveX et indique les interfaces facultatives, qui sont obligatoires et doivent être implémentées par les conteneurs de contrôle.



| Interface                                                                      | Requis ?      | Commentaires                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Renvoyé**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Oui<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Non<br/>  | Uniquement lorsque le conteneur désire (a) des notifications de modification de données (contrôles avec [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)), (b) afficher la notification de modification (contrôles qui ne sont pas actifs et [**qui ont un**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) et (c) d’autres notifications de contrôles agissant comme des objets incorporés standard.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Oui<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Oui<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Oui<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Oui<br/> | Voir la remarque 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** pour les propriétés ambiantes<br/>                                | Oui<br/> | Voir la remarque 2 et les [propriétés ambiantes pour les contrôles](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Jeux d’événements de contrôle<br/>                                                  | Oui<br/> | Voir la remarque 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Non<br/>  | [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) et la prise en charge des frames simples imbriqués sont facultatifs.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | Non<br/>  | Nécessaire uniquement pour les conteneurs qui (a) ont leur propre interface utilisateur de modification de propriété, qui nécessiterait une mise à jour chaque fois qu’un contrôle modifie une propriété elle-même ou (b) souhaite contrôler \[ [](/windows/desktop/Midl/requestedit) \] les modifications des propriétés modification et d’autres fonctionnalités de liaison de données.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Oui<br/> | Obligatoire si le conteneur prend en charge les interfaces doubles. Voir la remarque 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Non<br/>  | La prise en charge est vivement recommandée.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) est implémenté sur l’objet document ou formulaire (ou une valeur analogique appropriée) qui contient les sites conteneurs. Les contrôles utilisent **IOleContainer** pour naviguer vers d’autres contrôles dans le même document ou formulaire.
2.  La prise en charge des interfaces doubles n’est pas obligatoire, mais elle est fortement recommandée. L’écriture de conteneurs de contrôles ActiveX pour tirer parti des interfaces doubles offre de meilleures performances avec les contrôles qui offrent une prise en charge d’interface double.

Les conteneurs de contrôles ActiveX doivent prendre en charge les exceptions OLE Automation. Si un conteneur de contrôle prend en charge les interfaces doubles, il doit capturer les exceptions Automation via [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

