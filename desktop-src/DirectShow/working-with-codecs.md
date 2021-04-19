---
description: Utilisation des codecs
ms.assetid: c69e0ecf-5f72-4d77-90e6-0f493325c0f4
title: Utilisation des codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe6d45608c3d95fee8f67344bdec0fc77431919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516955"
---
# <a name="working-with-codecs"></a>Utilisation des codecs

Microsoft Windows fournit plusieurs codecs en tant que composants du système d’exploitation. Les codecs disponibles incluent toujours ceux fournis avec la version de DirectX et le lecteur Windows Media inclus dans la version de Windows. Des codecs supplémentaires peuvent être installés lorsque des versions plus récentes de DirectX ou du lecteur Windows Media ou des runtimes du kit de développement logiciel (SDK) Windows Media sont installés. Des tiers peuvent installer des codecs supplémentaires sur un système hôte. ces codecs peuvent être conçus pour fonctionner uniquement avec une application particulière, ou ils peuvent prendre en charge l’utilisation générale par n’importe quelle application DirectShow.

Les codecs peuvent être implémentés de l’une des trois façons suivantes :

-   Vidéo pour le codec d’installation audio ou vidéo de type Windows qui est chargé par le gestionnaire de compression vidéo (VCM) ou le gestionnaire de compression audio (ACM). En général, cette technologie est considérée comme dépréciée et son utilisation n’est pas recommandée. Les codecs installables participent aux graphiques de filtre DirectShow par le biais du filtre de wrapper de décompresseur AVI.
-   En tant que filtre DirectShow. De nombreux codecs tiers sont implémentés en tant que filtres DirectShow natifs. Un filtre de ce type est le filtre décompresseur Frauenhofer MP3. En général, ces filtres peuvent être ajoutés au graphique de filtre de la manière habituelle. Une exception à cette règle est que certains codecs audio ou Windows Media Video Windows Media™, et le codec Microsoft MPEG-4, ne peuvent pas être ajoutés manuellement à un graphique de filtre. Ces filtres peuvent uniquement être ajoutés par le lecteur ASF et les filtres d’écriture ASF.
-   As DirectX Media Objects (DMOs). DMOs est la méthode recommandée pour implémenter des codecs, car ils peuvent être utilisés dans un graphique de filtre DirectShow à l’aide du filtre de wrappers DMO, ou indépendamment dans toute autre application de diffusion en continu non DirectShow. Certains codecs Windows Media Audio et Windows Media Video sont implémentés en tant que DMOs. Comme pour les filtres Windows Media, ces DMOs ne peuvent pas être utilisés en dehors du contexte du kit de développement logiciel (SDK) Windows Media. Cela signifie que dans DirectShow, ils peuvent uniquement être ajoutés à un graphique par le biais des filtres de lecteur ASF ou d’enregistreur ASF.

Dans GraphEdit, tous ces différents types de codecs apparaissent ensemble dans les catégories suivantes :

-   Compresseur audio
-   Compresseur vidéo
-   Filtre DirectShow

Un grand nombre de ces codecs, toutefois, sont installés par des tiers, ou par d’autres applications Microsoft ou composants du système d’exploitation, et ne sont pas destinés à être utilisés par d’autres applications DirectShow. La liste des codecs visibles dans GraphEdit dépend également de la version de Windows en cours d’exécution sur le système hôte et de la version du kit de développement logiciel (SDK) DirectShow installée.

 

 



