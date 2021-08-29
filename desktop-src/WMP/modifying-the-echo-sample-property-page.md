---
title: Modification de la page de propriétés de l’exemple Echo
description: Modification de la page de propriétés de l’exemple Echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés de l’exemple Echo
- plug-ins, pages de propriétés d’exemple Echo
- plug-ins de traitement de signal numérique, pages de propriétés d’exemple Echo
- Plug-ins DSP, pages de propriétés d’exemple Echo
- Exemple de plug-in DSP Echo, pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca4312f61c8f909cd577ae0a0523afaf0d0fbddc420e974e2bd511d120bc622e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647619"
---
# <a name="modifying-the-echo-sample-property-page"></a>Modification de la page de propriétés de l’exemple Echo

l’implémentation de la page de propriétés par défaut fournie par l’assistant de plug-in Lecteur Windows Media l’exemple de plug-in DSP contient un seul contrôle de zone d’édition qui reçoit le facteur d’échelle de l’utilisateur. Vous devez modifier la page de propriétés pour recevoir les deux valeurs de propriété utilisées par l’exemple Echo.

Pour obtenir une vue d’ensemble des pages de propriétés du plug-in DSP, consultez [Implementing a audio DSP plug-](implementing-an-audio-dsp-plug-in.md)in.

Les sections suivantes vous guident tout au long du processus de modification de la page de propriétés de l’exemple :

-   [Modification de la ressource de boîte de dialogue Echo](modifying-the-echo-dialog-resource.md)
-   [Ajout et modification des événements](adding-and-modifying-the-events.md)
-   [Comment l’exemple Echo conserve les données](how-the-echo-sample-persists-data.md)
-   [Implémentation de CEchoPropPage :: OnInitDialog](implementing-cechoproppage--oninitdialog.md)
-   [Implémentation de CEchoPropPage :: apply](implementing-cechoproppage--apply.md)
-   [Implémentation de CEcho :: FinalConstruct](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple Echo**](the-echo-sample.md)
</dt> </dl>

 

 




