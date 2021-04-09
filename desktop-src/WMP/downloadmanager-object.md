---
title: Objet DownloadManager
description: Objet DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Windows Media Player Online stores, objet DownloadManager
- magasins en ligne, objet DownloadManager
- types 2 magasins en ligne, objet DownloadManager
- DownloadManager
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3555ee7b99c97e85ce856766bd9f670aac4229b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840230"
---
# <a name="downloadmanager-object"></a>Objet DownloadManager

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’objet **downloadmanager** est l’objet racine du gestionnaire de téléchargement du lecteur Windows Media. Il peut être utilisé par les pages Web qui sont hébergées dans les volets de tâches du service de magasin en ligne.

L’objet **downloadmanager** prend en charge les méthodes suivantes.



| Méthode                                                                   | Description                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crée une collection de téléchargements vide.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Récupère la collection de téléchargements spécifiée. |



 

L’objet **downloadmanager** est accessible à l’aide de l' **External. DownloadManager**. À des fins d’illustration, il est supposé que cette valeur a été assignée à une variable nommée « DownloadManager », qui sera utilisée pour identifier cet objet dans les sections de syntaxe de référence.

Dans le lecteur Windows Media 10 ou version ultérieure, la propriété et l’objet **downloadmanager** sont accessibles uniquement à partir des volets de tâches du service de magasin en ligne. Vous ne pouvez pas utiliser **downloadmanager** à partir d’autres fonctionnalités où l’objet **externe** est disponible, par exemple HTMLView, le mode Info Center et les informations sur l’album.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




