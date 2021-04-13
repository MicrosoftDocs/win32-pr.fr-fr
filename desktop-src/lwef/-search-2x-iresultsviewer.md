---
title: Interface IResultsViewer (WdsSharedIDL. h)
description: Expose les méthodes et les propriétés de la vue résultats.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer
- Fonctionnalités d’environnement Windows héritées de l’interface IResultsViewer, Description
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508806"
---
# <a name="iresultsviewer-interface"></a>Interface IResultsViewer

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Expose les méthodes et les propriétés de la vue résultats.

## <a name="members"></a>Membres

L’interface **IResultsViewer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultsViewer** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IResultsViewer** possède ces méthodes.



| Méthode                                                   | Description                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Non implémenté.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Non implémenté.<br/>                                                            |
| [**Générer**](-search-2x-iresultsviewer-refresh.md)     | Non implémenté.<br/>                                                            |
| [**Erreur**](-search-2x-iresultsviewer-stop.md)           | Non implémenté.<br/>                                                            |
| [**Mise à jour**](-search-2x-iresultsviewer-update.md)       | Applique les modifications de requête et parcourt la vue jusqu’au nouvel ensemble de résultats.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IResultsViewer** possède les propriétés suivantes.



| Propriété                                                                            | Type d’accès           | Description                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Contenu**](-search-2x-iresultsviewer-contents.md)<br/>                   | Écriture seule<br/> | Cette propriété effectue le suivi du type de contenu affiché dans l’affichage des résultats. <br/>    |
| [**NomComplet**](-search-2x-iresultsviewer-displayname.md)<br/>             | Lecture seule<br/>  | Nom complet localisé du type.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Écriture seule<br/> | Non implémenté.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lecture/écriture<br/> | Cette propriété définit ou retourne le nom du type preceived pour filtrer les résultats par.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lecture/écriture<br/> | Style de l’en-tête affiché dans la vue.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Écriture seule<br/> | La valeur TRUE est retournée si la requête views a été modifiée et doit être mise à jour. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lecture/écriture<br/> | Cette propriété définit ou retourne le nom du magasin sur lequel filtrer les résultats.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lecture/écriture<br/> | Contrôle le mode d’affichage du volet de visualisation.<br/>                                             |
| [**Le propertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Écriture seule<br/> | Lors de l’appel de la collection de filtres de propriétés, elle retourne ce qui suit :<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit le texte de la requête actuelle.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Écriture seule<br/> | Non implémenté.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lecture/écriture<br/> | Cette propriété définit ou retourne l’ordre des colonnes de tri des résultats. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lecture/écriture<br/> | Cette propriété définit ou retourne le IndexColumn de la propriété selon laquelle trier les résultats. <br/> |



 

## <a name="remarks"></a>Notes

Ces méthodes et propriétés sont utilisées pour manipuler les informations affichées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

