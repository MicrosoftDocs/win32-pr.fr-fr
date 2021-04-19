---
description: L’interface IXml2Dex enregistre et charge les fichiers projet DES services de modification DirectShow (DES) en Extensible Markup Language (XML). Cette interface fournit également des méthodes pour lire et écrire des fichiers de graphique DirectShow (. GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interface IXml2Dex (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525631"
---
# <a name="ixml2dex-interface"></a>Interface IXml2Dex

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IXml2Dex` interface enregistre et charge les fichiers projet des [services de modification DirectShow](directshow-editing-services.md) (des) en Extensible Markup Language (XML). Cette interface fournit également des méthodes pour lire et écrire des fichiers de graphique DirectShow (. GRF).

## <a name="members"></a>Membres

L’interface **IXml2Dex** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IXml2Dex** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IXml2Dex** possède ces méthodes.



| Méthode                                                      | Description                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Non implémenté.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Non implémenté.<br/>                                                |
| [**Supprimer**](ixml2dex-delete.md)                           | Non implémenté.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Non implémenté.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Non implémenté.<br/>                                                |
| [**ReadXML**](ixml2dex-readxml.md)                         | Non implémenté.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Charge un fichier projet XML.<br/>                                      |
| [**Réinitialiser**](ixml2dex-reset.md)                             | Non implémenté.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Écrit un graphique de filtre dans un fichier au format. GRF.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Convertit une chronologie en une chaîne XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Convertit une chronologie en XML et écrit les données XML dans un fichier.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Non implémenté.<br/>                                                |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4,0 ou version ultérieure<br/>                                               |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
