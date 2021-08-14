---
title: Modification de la propriété exemple de plug-in DSP audio
description: Modification de la propriété exemple de plug-in DSP audio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, propriétés audio
- Plug-ins DSP, propriétés audio
- plug-ins DSP audio, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342622"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Modification de la propriété exemple de plug-in DSP audio

vous souhaiterez probablement modifier la propriété que l’assistant de Plug-in Lecteur Windows Media crée par défaut. La liste suivante détaille les éléments qui peuvent nécessiter des modifications :

-   **Ressource de boîte de dialogue.** cliquez sur l’onglet **ResourceView** dans la fenêtre de l’espace de travail Project. Développez la liste des dossiers pour ouvrir le dossier boîte de dialogue. Double-cliquez sur la ressource de boîte de dialogue pour ouvrir l’éditeur de ressources. Vous pouvez apporter des modifications à la boîte de dialogue de la page de propriétés pour répondre à vos besoins. Par exemple, vous pouvez modifier le texte de l’étiquette ou remplacer le contrôle d’édition par une case à cocher.
-   **Code objet de la page de propriétés.** L’implémentation par défaut utilise une variable de type double pour stocker le facteur d’échelle. Vous pouvez avoir besoin d’un type de données différent. Cela vous obligerait également à modifier le code qui rend les données persistantes dans le registre et à lire les données à partir du Registre (y compris le code qui lit à partir du Registre dans *CProjectName*::**FinalConstruct**).
-   **Variable membre qui stocke la valeur de propriété.** Cette variable est nommée « m \_ fScaleFactor » et est déclarée comme étant de type double. Vous pouvez modifier le nom et le type de cette variable tout au long du projet.
-   **Méthodes d’extraction et de propriété put.** Vous souhaiterez peut-être modifier les noms, les paramètres et les implémentations de ces méthodes. N’oubliez pas également de refléter ces modifications ailleurs dans le projet. Par exemple, la méthode **apply** de la page de propriétés appelle **l' \_ échelle** *CProjectName*:: put.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




