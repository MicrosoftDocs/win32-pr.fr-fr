---
title: Objet DownloadItem
description: Objet DownloadItem
ms.assetid: 668ee632-0a3d-426b-baab-08e88b9fc607
keywords:
- Windows Media Player Online stores, objet DownloadItem
- magasins en ligne, objet DownloadItem
- types 2 magasins en ligne, objet DownloadItem
- DownloadItem
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c367eee37f2f4d8329d71f3d42a3c78771a50a6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512471"
---
# <a name="downloaditem-object"></a>Objet DownloadItem

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’objet **DownloadItem** représente une demande de téléchargement de fichier. Il peut être utilisé par les pages Web qui sont hébergées dans le lecteur Windows Media en mode complet et qui ont accès à l’objet **externe** , tel que les services Premium.

L’objet **DownloadItem** prend en charge les propriétés suivantes.



| Propriété                                        | Description                                      |
|-------------------------------------------------|--------------------------------------------------|
| [downloadState](downloaditem-downloadstate.md) | Récupère l’état du téléchargement.             |
| [avancement](downloaditem-progress.md)           | Récupère la progression du téléchargement en octets. |
| [size](downloaditem-size.md)                   | Récupère la taille du téléchargement.              |
| [sourceURL](downloaditem-sourceurl.md)         | Récupère l’URL source du téléchargement.        |
| [type](downloaditem-type.md)                   | Récupère le type du téléchargement.              |



 

L’objet **DownloadItem** prend en charge les méthodes suivantes.



| Méthode                                      | Description                                                |
|---------------------------------------------|------------------------------------------------------------|
| [cancel](downloaditem-cancel.md)           | Annule le téléchargement.                                      |
| [getItemInfo](downloaditem-getiteminfo.md) | Récupère la valeur d’un attribut pour l’élément de téléchargement. |
| [pause](downloaditem-pause.md)             | Interrompt le téléchargement.                                       |
| [sort](downloaditem-resume.md)           | Reprend le téléchargement.                                      |



 

L’objet **DownloadItem** est accessible par le biais de la propriété suivante.



| Object                                              | Propriété                            |
|-----------------------------------------------------|-------------------------------------|
| [DownloadCollection](downloadcollection-object.md) | [item](downloadcollection-item.md) |



 

À des fins d’illustration, **downloadmanager**. **getDownloadCollection**(*le* biais). **Item**(*ItemId*) est utilisé dans les sections de syntaxe de référence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




