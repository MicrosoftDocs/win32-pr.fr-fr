---
description: Création d’objets de flux multimédia et d’exemples de flux
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Création d’objets de flux multimédia et d’exemples de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953414"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Création d’objets de flux multimédia et d’exemples de flux

> [!Note]  
> Ces API sont déconseillées. Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Les objets qui prennent en charge l’interface [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) sont les conteneurs de base pour les flux de données multimédias. L’interface **IMultiMediaStream** comprend des méthodes qui énumèrent les flux de données de l’objet ; ces flux sont généralement des données audio et vidéo, mais peuvent inclure des données de n’importe quel format, telles que des sous-titres, du texte brut ou du code temporel SMPTE. L’interface **IMultiMediaStream** est un conteneur générique ; Toutefois, les développeurs peuvent créer d’autres versions de l’interface qui prennent en charge des formats de données spécifiques. Les objets qui implémentent l’interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) peuvent, par exemple, énumérer et contrôler des flux de tout format de données DirectShow. Étant donné que les flux de données individuels sont spécifiques au format, ils prennent en charge au moins deux interfaces différentes : un générique et un spécifique aux données. Chaque flux prend en charge l’interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) , qui fournit des méthodes pour récupérer son format et un pointeur vers le flux lui-même. L’interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) , en revanche, a des méthodes qui traitent spécifiquement du rendu des données vidéo. Toute interface dérivée de **IMultiMediaStream** prend également en charge la création d’exemples de flux, les unités de base des données de diffusion en continu.

Un exemple multimédia est une référence à un objet contenant les données multimédias. Pour une image vidéo, il s’agit d’une surface DirectDraw. Le contenu exact de l’exemple varie selon le type de média (son, texte, etc.). Étant donné qu’un exemple n’est qu’une référence à l’objet de données, un nombre quelconque d’exemples de flux peuvent faire référence au même objet. L’interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) fournit des méthodes qui obtiennent et définissent les caractéristiques d’un exemple, telles que l’heure de début et d’arrêt, l’État et l’Association de flux. La méthode [**IStreamSample :: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) actualise les données de l’exemple dans le cas de flux lisibles. Pour les flux accessibles en écriture, les données de l’exemple sont écrites dans le flux. En règle générale, vous utilisez la méthode **Update** dans une boucle qui restitue, transfère ou stocke les données de streaming.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’architecture de diffusion multimédia en continu](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



