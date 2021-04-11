---
title: Personnalisation du plug-in d’interface utilisateur
description: Personnalisation du plug-in d’interface utilisateur
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-ins du lecteur Windows Media, personnalisation
- plug-ins, personnalisation
- plug-ins d’interface utilisateur, personnalisation
- Plug-ins d’interface utilisateur, personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029619"
---
# <a name="customizing-the-ui-plug-in"></a>Personnalisation du plug-in d’interface utilisateur

À ce stade, votre projet est prêt pour la personnalisation. Vous pouvez modifier l’implémentation générée par l’Assistant de l’interface **IWMPPluginUI** , vous pouvez ajouter une interface utilisateur à la classe **CPluginWindow** , et vous pouvez implémenter une page de propriétés dans la classe **CPropertyDialog** . Si votre plug-in est configuré pour écouter les événements du lecteur Windows Media, l’Assistant aura généré des implémentations par défaut ou vides de tous les gestionnaires d’événements nécessaires, que vous pouvez également modifier ou créer.

Le type de plug-in et les fonctionnalités qu’il prend en charge sont indiqués par une valeur stockée dans le Registre Windows. L’Assistant génère un fichier avec une extension de nom de fichier. RGS qui contient les informations pour inscrire le plug-in. La valeur « Capabilities » dans ce fichier est l’équivalent décimal d’un booléen ou des constantes de type de plug-in et des indicateurs de plug-in définis dans wmpplug. h. Bien que cette valeur soit déterminée par les options que vous sélectionnez dans l’Assistant, vous devez la modifier si vous souhaitez créer un plug-in avec plusieurs présélections ou l’un des éléments multimédias ou des sélections que vous pouvez envoyer.

À mesure que vous modifiez et étendez votre code de plug-in, vous pouvez créer et inscrire votre DLL afin de pouvoir tester votre plug-in dans le lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’un plug-in d’interface utilisateur**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




