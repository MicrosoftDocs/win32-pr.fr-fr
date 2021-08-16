---
title: Objet DownloadManager
description: Objet DownloadManager
ms.assetid: e6b07f3c-9254-41bb-9480-8167c3cd655b
keywords:
- Lecteur Windows Media les magasins en ligne, objet DownloadManager
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
ms.openlocfilehash: 500061e414d7321ed6fe4c46cafc79cd6795935847bb3d8c527364497722ecf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340523"
---
# <a name="downloadmanager-object"></a>Objet DownloadManager

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’objet **DownloadManager** est l’objet racine pour le gestionnaire de téléchargement Lecteur Windows Media. Il peut être utilisé par les pages Web qui sont hébergées dans les volets de tâches du service de magasin en ligne.

L’objet **downloadmanager** prend en charge les méthodes suivantes.



| Méthode                                                                   | Description                                  |
|--------------------------------------------------------------------------|----------------------------------------------|
| [createDownloadCollection](downloadmanager-createdownloadcollection.md) | Crée une collection de téléchargements vide.        |
| [getDownloadCollection](downloadmanager-getdownloadcollection.md)       | Récupère la collection de téléchargements spécifiée. |



 

L’objet **downloadmanager** est accessible à l’aide de l' **External. DownloadManager**. À des fins d’illustration, il est supposé que cette valeur a été assignée à une variable nommée « DownloadManager », qui sera utilisée pour identifier cet objet dans les sections de syntaxe de référence.

dans Lecteur Windows Media 10 ou version ultérieure, la propriété et l’objet **DownloadManager** sont accessibles uniquement à partir des volets de tâches du service de magasin en ligne. Vous ne pouvez pas utiliser **downloadmanager** à partir d’autres fonctionnalités où l’objet **externe** est disponible, par exemple HTMLView, le mode Info Center et les informations sur l’album.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




