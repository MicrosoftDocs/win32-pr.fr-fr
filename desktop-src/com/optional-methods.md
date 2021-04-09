---
title: Méthodes facultatives
description: Méthodes facultatives
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102381"
---
# <a name="optional-methods"></a>Méthodes facultatives

Un composant OLE peut implémenter une interface sans implémenter toutes les sémantiques de chaque méthode de l’interface, à la place \_ NOTIMPL ou S \_ OK. Le tableau suivant décrit les méthodes qu’un conteneur de contrôles ActiveX n’est pas tenu d’implémenter (autrement dit, le conteneur de contrôle peut retourner E \_ NOTIMPL).

Le tableau ci-dessous décrit les méthodes facultatives. Notez que la méthode doit toujours exister, mais peut simplement retourner E \_ NOTIMPL au lieu d’implémenter la sémantique réelle. Notez que toute méthode d’une interface obligatoire qui n’est pas listée ci-dessous doit être considérée comme obligatoire et ne pas retourner E \_ NOTIMPL.

## <a name="ioleclientsite"></a>Renvoyé



| Méthode                                                     | Commentaires                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | Nécessaire pour que la persistance soit prise en charge.<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | Nécessaire uniquement si le conteneur prend en charge la liaison aux contrôles dans son propre formulaire ou document.<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| Méthode                                                                     | Commentaires                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | Facultatif<br/>                                      |
| [**Scroll**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | Peut retourner S \_ false sans action.<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | Peut retourner S \_ OK sans action.<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | La désactivation est obligatoire ; Undo est facultatif. <br/> |



 

## <a name="iolecontrolsite"></a>IOleControlSite



| Méthode                                                                          | Commentaires                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | Nécessaire pour les conteneurs qui prennent en charge les contrôles étendus.<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | Nécessaire pour les conteneurs qui souhaitent inclure leurs propres pages de propriétés pour gérer les propriétés de contrôle étendues, en plus de celles fournies par un contrôle.<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | Peut retourner S \_ false sans action.<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | Facultatif<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (propriétés ambiantes)



| Méthode                      | Commentaires                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.<br/> |
| GetTypeInfo<br/>      | Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.<br/> |
| GetIDsOfNames<br/>    | Nécessaire pour les conteneurs qui prennent en charge des propriétés ambiantes non standard.<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (récepteur d’événements)



| Méthode                      | Commentaires                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.<br/> |
| GetTypeInfo<br/>      | Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.<br/> |
| GetIDsOfNames<br/>    | Le contrôle connaît ses propres informations de type, il n’a donc pas besoin de l’appeler.<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| Méthode                                                                           | Commentaires                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)<br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)<br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | Nécessaire pour les conteneurs avec l’interface utilisateur de la barre d’outils (option facultative)<br/> |
| [**InsertMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)<br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)<br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | Nécessaire pour les conteneurs avec l’interface utilisateur du menu (option facultative)<br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | Nécessaire uniquement pour les conteneurs qui ont une ligne d’État<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | Facultatif<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | Facultatif<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| Méthode                                                                    | Commentaires                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | Uniquement si la liaison aux contrôles ou à d’autres incorporations dans le conteneur est prise en charge, ce qui est nécessaire pour la liaison de moniker.<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | Comme pour ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | Retourne tous les contrôles ActiveX via un énumérateur avec [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), mais pas nécessairement tous les objets (parce qu’il n’y a aucune garantie que tous les objets sont des contrôles ActiveX ; certains peuvent être des contrôles Windows normaux).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

