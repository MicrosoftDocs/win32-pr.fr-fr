---
description: Exemple ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Exemple ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db441be45d28899bc8f2ace68b8f09af40e679449d26aec7adf25ab4fb9e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959549"
---
# <a name="asfparser-sample"></a>Exemple ASFParser

Montre comment analyser les données à partir d’un fichier ASF (Advanced Systems Format) à l’aide des composants ASF de bas niveau dans Media Foundation. L’exemple illustre les tâches suivantes :

-   Énumération des flux audio et vidéo dans un fichier ASF.
-   Sélection d’un flux audio ou vidéo pour l’analyse.
-   Recherche d’un paquet à une heure de lecture souhaitée.
-   Génération d’exemples compressés pour le flux sélectionné.
-   Décodage des échantillons audio et vidéo.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Microsoft Media Foundation suivantes :

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>Usage

1.  Pour ouvrir un fichier ASF, cliquez sur le bouton **ouvrir le fichier multimédia..** ..
2.  Sélectionnez un fichier ASF, puis cliquez sur **ouvrir**. Les informations relatives au fichier s’affichent dans le volet d' **informations** .
3.  Sous **configuration de l’analyseur**, sélectionnez un flux à analyser.
4.  Pour générer des exemples en sens inverse, sélectionnez **inverser**.
5.  Pour spécifier le point de départ, faites glisser le curseur vers l’emplacement souhaité.
6.  Pour commencer l’analyse, cliquez sur le bouton **générer des exemples** . Les informations sur les exemples s’affichent dans le volet d' **informations** .
7.  Pour tester les exemples du flux audio, cliquez sur le bouton **tester l’audio** .
8.  Pour tester les exemples du flux vidéo, cliquez sur le bouton **afficher la bitmap** .

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Didacticiel : lecture d’un fichier ASF](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



