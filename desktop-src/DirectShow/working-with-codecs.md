---
description: Utilisation des codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Utilisation des codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462a1340ef7e6a64aada586addcc73d95a993884fe2b026e74acde5fd286638c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650618"
---
# <a name="working-with-codecs"></a>Utilisation des codecs

Microsoft Windows fournit plusieurs codecs en tant que composants du système d’exploitation. les codecs disponibles incluent toujours ceux fournis avec la version de DirectX et de Lecteur Windows Media inclus dans la version de Windows. des codecs supplémentaires peuvent être installés lors de l’installation de versions plus récentes de DirectX ou de Lecteur Windows Media ou des runtimes du kit de développement logiciel (SDK) Windows Media. Des tiers peuvent installer des codecs supplémentaires sur un système hôte. ces codecs peuvent être conçus pour fonctionner uniquement avec une application particulière, ou ils peuvent prendre en charge l’utilisation générale par n’importe quelle application DirectShow.

Les codecs peuvent être implémentés de l’une des trois façons suivantes :

-   vidéo pour le codec d’installation audio ou vidéo de type Windows qui est chargé par le gestionnaire de compression vidéo (VCM) ou le gestionnaire de compression audio (ACM). En général, cette technologie est considérée comme dépréciée et son utilisation n’est pas recommandée. les codecs installables participent à DirectShow des graphiques de filtre via le filtre de wrapper de décompresseur AVI.
-   en tant que filtre de DirectShow. de nombreux codecs tiers sont implémentés en tant que filtres de DirectShow natifs. Un filtre de ce type est le filtre décompresseur Frauenhofer MP3. En général, ces filtres peuvent être ajoutés au graphique de filtre de la manière habituelle. l’une des exceptions à cette règle est qu’il n’est pas possible d’ajouter manuellement à un graphique de filtre Windows des codecs Audio ou Windows Media Video™ et du codec Microsoft MPEG-4. Ces filtres peuvent uniquement être ajoutés par le lecteur ASF et les filtres d’écriture ASF.
-   As DirectX Media Objects (DMOs). DMOs est la méthode recommandée pour implémenter des codecs, car ils peuvent être utilisés dans un graphique de filtre DirectShow à l’aide du filtre de Wrapper DMO, ou indépendamment dans toute autre application de diffusion en continu non basée sur DirectShow. certains codecs Windows Media Audio et Windows Media Video sont implémentés en tant que DMOs. comme pour les filtres de média Windows, ces DMOs ne peuvent pas être utilisés en dehors du contexte du kit de développement logiciel (SDK) Windows media. cela signifie que dans DirectShow, ils peuvent uniquement être ajoutés à un graphique par le biais des filtres de lecteur asf ou d’enregistreur asf.

Dans GraphEdit, tous ces différents types de codecs apparaissent ensemble dans les catégories suivantes :

-   Compresseur audio
-   Compresseur vidéo
-   filtre de DirectShow

un grand nombre de ces codecs, toutefois, sont installés par des tiers, ou par d’autres applications Microsoft ou composants du système d’exploitation, et ne sont pas destinés à être utilisés par d’autres applications de DirectShow. la liste des codecs visibles dans GraphEdit dépend également de la version de Windows s’exécutant sur le système hôte, ainsi que de la version du kit de développement logiciel (SDK) DirectShow installée.

 

 



