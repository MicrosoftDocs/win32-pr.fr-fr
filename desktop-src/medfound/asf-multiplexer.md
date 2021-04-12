---
description: Multiplexeur ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexeur ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033823"
---
# <a name="asf-multiplexer"></a>Multiplexeur ASF

Le *multiplexeur* ASF est un objet de couche WMContainer qui fonctionne avec l' [objet de données ASF](asf-file-structure.md) et donne à une application la possibilité de générer des paquets de données pour un conteneur ASF. Le multiplexeur accepte les données multimédias sous la forme d' [exemples](media-samples.md) de média et génère des exemples de média basés sur les paramètres de paquets de streaming et ASF définis dans l' [objet d’en-tête ASF](asf-file-structure.md). Les exemples de supports de sortie contiennent des références à un ou plusieurs tampons de média qui contiennent des données multimédias numériques paquets. Vous pouvez utiliser cet objet dans un scénario d’encodage de fichier dans lequel il reçoit des exemples de flux encodés à partir de l’encodeur ou pour le transcodage ASF-ASF (remuxing).

Le diagramme suivant illustre la génération de paquets de données ASF pour un fichier ASF à l’aide du multiplexeur.

![Diagramme montrant la génération de paquets de données ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Pour plus d’informations sur la structure d’un fichier ASF, consultez [structure des fichiers ASF](asf-file-structure.md).

Cette section contient les rubriques suivantes :



| Rubrique                                                                  | Description                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Création de l’objet multiplexeur](creating-the-multiplexer-object.md) | Comment créer et initialiser le multiplexeur.                     |
| [Génération de nouveaux paquets de données ASF](generating-new-asf-data-packets.md) | Comment générer des paquets de données pour constituer un nouvel objet de données ASF. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Didacticiel : copie de flux de fichiers ASF d’un fichier à un autre](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Didacticiel : écriture d’un fichier WMA à l’aide de l’encodage CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



