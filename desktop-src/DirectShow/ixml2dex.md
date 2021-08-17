---
description: l’interface IXml2Dex enregistre et charge DirectShow fichiers de projet des Services d’édition dans Extensible Markup Language (XML). cette interface fournit également des méthodes pour lire et écrire des fichiers DirectShow graph (. grf).
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
ms.openlocfilehash: 3bc12c2305a8b92110d4aa17522184e9a3c5ee83b60ccd5a989468fa0a8c6e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952388"
---
# <a name="ixml2dex-interface"></a>Interface IXml2Dex

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IXml2Dex` interface enregistre et charge [DirectShow](directshow-editing-services.md) fichiers de projet des Services d’édition dans Extensible Markup Language (XML). cette interface fournit également des méthodes pour lire et écrire des fichiers DirectShow graph (. grf).

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
| [**Initialisation**](ixml2dex-reset.md)                             | Non implémenté.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Écrit un graphique de filtre dans un fichier au format. GRF.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Convertit une chronologie en une chaîne XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Convertit une chronologie en XML et écrit les données XML dans un fichier.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Non implémenté.<br/>                                                |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4,0 ou version ultérieure<br/>                                               |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
