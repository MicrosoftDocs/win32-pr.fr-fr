---
title: Personnalisation du plug-in d’interface utilisateur
description: Personnalisation du plug-in d’interface utilisateur
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- plug-ins Lecteur Windows Media, personnalisation
- plug-ins, personnalisation
- plug-ins d’interface utilisateur, personnalisation
- Plug-ins d’interface utilisateur, personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7182d2f4710432638bd273e17226954f2b14f0fc831d64aa4078ed796e00cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936233"
---
# <a name="customizing-the-ui-plug-in"></a>Personnalisation du plug-in d’interface utilisateur

À ce stade, votre projet est prêt pour la personnalisation. Vous pouvez modifier l’implémentation générée par l’Assistant de l’interface **IWMPPluginUI** , vous pouvez ajouter une interface utilisateur à la classe **CPluginWindow** , et vous pouvez implémenter une page de propriétés dans la classe **CPropertyDialog** . si votre plug-in est configuré pour écouter des événements Lecteur Windows Media, l’assistant aura généré des implémentations par défaut ou vides de tous les gestionnaires d’événements nécessaires, que vous modifiez ou créez également.

le type de plug-in et les fonctionnalités qu’il prend en charge sont indiqués par une valeur stockée dans le registre Windows. L’Assistant génère un fichier avec une extension de nom de fichier. RGS qui contient les informations pour inscrire le plug-in. La valeur « Capabilities » dans ce fichier est l’équivalent décimal d’un booléen ou des constantes de type de plug-in et des indicateurs de plug-in définis dans wmpplug. h. Bien que cette valeur soit déterminée par les options que vous sélectionnez dans l’Assistant, vous devez la modifier si vous souhaitez créer un plug-in avec plusieurs présélections ou l’un des éléments multimédias ou des sélections que vous pouvez envoyer.

lorsque vous modifiez et étendez votre code de plug-in, vous pouvez créer et inscrire votre DLL pour tester votre plug-in dans Lecteur Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’un plug-in d’interface utilisateur**](building-a-ui-plug-in.md)
</dt> </dl>

 

 




