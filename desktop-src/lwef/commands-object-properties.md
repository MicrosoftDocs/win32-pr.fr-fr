---
title: Propriétés de l’objet Commands
description: Propriétés de l’objet Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716539"
---
# <a name="commands-object-properties"></a>Propriétés de l’objet Commands

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le serveur prend en charge les propriétés suivantes pour la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) :

-   [**Caption**](caption-property-cmds.md)
-   [**Count**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**ContexteAide**](helpcontextid-property.md)
-   [**Parent**](visible-property-cso.md)
-   [**Voice**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Une entrée pour la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) peut apparaître à la fois dans le menu contextuel et dans la fenêtre commandes vocales pour un caractère. Pour que cette entrée apparaisse dans le menu contextuel, définissez sa propriété [**Caption**](caption-property-cmds.md) . Pour inclure l’entrée dans la fenêtre commandes vocales, définissez sa propriété [**VoiceCaption**](voicecaption-property.md) . (Pour la compatibilité descendante, s’il n’y a aucun **VoiceCaption**, le paramètre de **légende** est utilisé)

Le tableau suivant résume la façon dont les propriétés d’un objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) affectent la présentation de l’entrée :



| Propriété Caption                                                                                                                                                                                                                                            | Voice-Caption, propriété | Voice, propriété | Propriété visible | Apparaît dans le menu contextuel du caractère | Apparaît dans la fenêtre commandes vocales |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Oui                                                                                                                                                                                                                                                         | Oui                    | Oui            | Vrai             | Oui, à l’aide de la légende                 | Oui, à l’aide de VoiceCaption          |
| Oui                                                                                                                                                                                                                                                         | Oui                    | Non             | Vrai             | Oui, à l’aide de la légende                 | Non                               |
| Oui                                                                                                                                                                                                                                                         | Oui                    | Oui            | False            | Non                                 | Oui, à l’aide de VoiceCaption          |
| Oui                                                                                                                                                                                                                                                         | Oui                    | Non             | False            | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Oui                    | Oui            | True             | Non                                 | Oui, à l’aide de VoiceCaption          |
| Non                                                                                                                                                                                                                                                          | Oui                    | Oui            | False            | Non                                 | Oui, à l’aide de VoiceCaption          |
| Non                                                                                                                                                                                                                                                          | Oui                    | Non             | True             | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Oui                    | Non             | False            | Non                                 | Non                               |
| Oui                                                                                                                                                                                                                                                         | Non1                    | Oui            | Vrai             | Oui, à l’aide de la légende                 | Oui, à l’aide de la légende               |
| Oui                                                                                                                                                                                                                                                         | Non                     | Non             | True             | Oui                                | Non                               |
| Oui                                                                                                                                                                                                                                                         | Non                     | Oui            | False            | Non                                 | Oui, à l’aide de la légende               |
| Oui                                                                                                                                                                                                                                                         | Non                     | Non             | False            | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Non                     | Oui            | True             | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Non                     | Oui            | False            | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Non                     | Non             | True             | Non                                 | Non                               |
| Non                                                                                                                                                                                                                                                          | Non                     | Non             | False            | Non                                 | Non                               |
|  Si le paramètre de la propriété a la valeur null. Dans certains langages de programmation, une chaîne vide ne peut pas être interprétée comme une chaîne NULL.  La commande est toujours accessible en voix et apparaît dans la fenêtre commandes vocales comme « (commande non définie) ».<br/> |                        |                |                  |                                    |                                  |



 

 

