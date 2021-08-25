---
title: Objet DownloadCollection
description: Objet DownloadCollection
ms.assetid: e943b391-386e-43c5-a314-55ea31b2eefa
keywords:
- Lecteur Windows Media les magasins en ligne, objet DownloadCollection
- magasins en ligne, objet DownloadCollection
- types 2 magasins en ligne, objet DownloadCollection
- DownloadCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565ddce120d71ab9825c424fefb6f0e3ace9a6ac349e87e044e9c74e6da28789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902019"
---
# <a name="downloadcollection-object"></a>Objet DownloadCollection

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’objet **DownloadCollection** contient des propriétés et des méthodes pour gérer des collections d’éléments de téléchargement. il peut être utilisé par les pages web qui sont hébergées en mode complet Lecteur Windows Media et qui ont accès à l’objet **externe** , telles que les magasins en ligne.

L’objet **DownloadCollection** prend en charge les propriétés suivantes.



| Propriété                              | Description                                  |
|---------------------------------------|----------------------------------------------|
| [count](downloadcollection-count.md) | Récupère le nombre de téléchargements en attente.   |
| [id](downloadcollection-id.md)       | Récupère l’ID de la collection de téléchargements. |



 

L’objet **DownloadCollection** prend en charge les méthodes suivantes.



| Méthode                                                | Description                                   |
|-------------------------------------------------------|-----------------------------------------------|
| [Effacer](downloadcollection-clear.md)                 | Supprime tous les éléments d’une collection de téléchargements. |
| [item](downloadcollection-item.md)                   | Récupère un objet de téléchargement en attente.          |
| [removeItem](downloadcollection-removeitem.md)       | Supprime un élément de téléchargement d’une collection.    |
| [startDownload](downloadcollection-startdownload.md) | Met en file d’attente un téléchargement.                            |



 

L’objet **DownloadCollection** est accessible par le biais des méthodes suivantes.



| Object                                        | Méthode                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------|
| [DownloadManager](downloadmanager-object.md) | [createDownloadCollection](downloadmanager-createdownloadcollection.md) |
| [DownloadManager](downloadmanager-object.md) | [getDownloadCollection](downloadmanager-getdownloadcollection.md)       |



 

À des fins d’illustration, **downloadmanager**. **getDownloadCollection**(*porte*) est utilisé dans les sections de syntaxe de référence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 




