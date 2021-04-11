---
title: Méthodes facultatives dans les interfaces de contrôle
description: Méthodes facultatives dans les interfaces de contrôle
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1409b1c8d22f85a48829c07155e03379fc79103c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939744"
---
# <a name="optional-methods-in-control-interfaces"></a>Méthodes facultatives dans les interfaces de contrôle

L’implémentation d’une interface ne signifie pas nécessairement que l’implémentation de toutes les méthodes de cette interface ne fait rien de plus que retourner E \_ NOTIMPL ou S \_ OK, le cas échéant. Le tableau suivant identifie les méthodes des interfaces listées dans la rubrique qu’est-ce que la [prise en charge d’une interface signifie](what-support-for-an-interface-means.md) qu’un contrôle peut implémenter de cette manière. Toute méthode non répertoriée ici doit être entièrement implémentée si l’interface est prise en charge.



| IOleControl                                                                                                   | Commentaires                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obligatoire pour les contrôles avec des mnémoniques.<br/>                              |
| [**IOleControl :: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obligatoire pour les contrôles qui utilisent des propriétés ambiantes.<br/>                 |
| [**IOleControl :: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Voir [gel des événements](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obligatoire si le contrôle n’est pas marqué avec OLEMISC \_ CANTLINKINSIDE<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obligatoire si le contrôle n’est pas marqué avec OLEMISC \_ CANTLINKINSIDE<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Facultatif<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Facultatif<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Obligatoire uniquement pour le \_ contenu DVASPECT<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Obligatoire uniquement pour le \_ contenu DVASPECT<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Facultatif<br/>                                                            |
| [**Verbe**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Voir la remarque 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facultatif<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Facultatif<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Facultatif<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Facultatif<br/>                                                            |
| [**Libérer**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Facultatif<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Facultatif<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Voir la remarque 2<br/>                                                          |



 

1.  Un contrôle avec des pages de propriétés doit prendre en charge [**IOleObject ::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) pour les \_ Propriétés OLEIVERB et les \_ verbes primaires OLEIVERB. Un contrôle qui peut être actif **doit prendre en charge DoVerb pour** le \_ verbe OLEIVERB INPLACEACTIVATE. Un contrôle qui peut être activé par l’interface utilisateur doit également prendre en charge **DoVerb** pour le \_ verbe OLEIVERB UIACTIVATE.
2.  Si un contrôle prend en charge [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) et peut retourner une valeur précise, il doit le faire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

 





