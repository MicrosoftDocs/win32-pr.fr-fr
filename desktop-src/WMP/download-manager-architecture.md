---
title: Architecture du gestionnaire de téléchargement
description: Architecture du gestionnaire de téléchargement
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- architecture du gestionnaire de téléchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671906"
---
# <a name="download-manager-architecture"></a>Architecture du gestionnaire de téléchargement

Le gestionnaire de téléchargement du lecteur Windows Media utilise la technologie COM. La fonctionnalité est divisée en un ensemble d’interfaces de programmation ; vous pouvez écrire du code de programmation qui utilise ces interfaces à l’aide de Microsoft JScript ou C++.

Les langages de script utilisent le concept d’objets pour diviser les fonctionnalités de programmation. Le modèle objet **downloadmanager** utilise plusieurs objets pour diviser les méthodes et les propriétés en une organisation logique qui regroupe les fonctions sémantiquement associées. Les sections suivantes contiennent des informations sur les objets du gestionnaire de téléchargement.



| Section                                                                     | Description                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [À propos de l’objet DownloadManager](#about-the-downloadmanager-object)       | L’objet **downloadmanager** représente l’objet racine du gestionnaire de téléchargement du lecteur Windows Media. |
| [À propos de l’objet DownloadCollection](#about-the-downloadcollection-object) | L’objet **DownloadCollection** représente une collection d’éléments de téléchargement.                             |
| [À propos de l’objet DownloadItem](#about-the-downloaditem-object)             | L’objet **DownloadItem** représente une demande de téléchargement individuelle.                                   |



 

## <a name="about-the-downloadmanager-object"></a>À propos de l’objet DownloadManager

**Downloadmanager** est l’objet racine du gestionnaire de téléchargement du lecteur Windows Media. Tous les autres objets sont accessibles par le biais de cet objet. Pour accéder à l’objet **downloadmanager** , utilisez la syntaxe JScript suivante :


```C++
var DownloadManager = external.DownloadManager;
```



Cela crée une instance de l’objet **downloadmanager** , qui peut ensuite être utilisée pour récupérer les objets enfants. Par exemple, la syntaxe suivante récupère le premier élément de la collection de téléchargements portant le numéro d’ID 253675 :


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>À propos de l’objet DownloadCollection

L’objet **DownloadCollection** représente une collection de fichiers à télécharger. Vous pouvez utiliser cet objet pour déterminer le nombre de téléchargements dans la collection, supprimer des éléments de la collection, récupérer un élément de téléchargement spécifique et démarrer un nouveau téléchargement. Le démarrage d’un nouveau téléchargement ajoute automatiquement le téléchargement à la collection.

## <a name="about-the-downloaditem-object"></a>À propos de l’objet DownloadItem

L’objet **DownloadItem** représente un téléchargement individuel. Les éléments de téléchargement existent toujours dans le cadre d’une collection de téléchargements. Utilisez cet objet pour récupérer des informations sur l’élément de téléchargement et pour suspendre, reprendre ou annuler le téléchargement en cours.

Lorsque vous annulez un téléchargement, l’élément de téléchargement reste en place dans sa collection de téléchargements. Dans ce cas, **downloadCollection**. **downloadState** récupère la valeur 4, ce qui signifie que l’opération a été annulée.

Vous pouvez utiliser **downloadItem**. **progression** pour informer l’utilisateur de la quantité de fichier qui a été transférée ou de la quantité restant à télécharger. Vous pouvez utiliser cette valeur pour estimer également le temps restant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestionnaire de téléchargement**](download-manager.md)
</dt> </dl>

 

 




