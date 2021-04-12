---
title: Propriétés de l’objet Character
description: Propriétés de l’objet Character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6212d6f0539b7fcb29faa883e6d88101952c12f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381781"
---
# <a name="character-object-properties"></a>Propriétés de l’objet Character

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’objet [**character**](/windows/desktop/lwef/the-characters-object) expose les propriétés suivantes :

-   [**Proactive**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Description**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**UNIQUES**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Height**](height-property.md)
-   [**ContexteAide**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**IdleOn**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**Gauche**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Nom**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Inclinaison**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**Vitesse**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**Retour au début**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**Version**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**Parent**](visible-property-cob.md)
-   [**Width**](width-property-co.md)

Notez que les propriétés de [**hauteur**](height-property.md), de [**gauche**](left-property.md), de [**haut**](top-property.md)et de [**largeur**](width-property-co.md) d’un caractère diffèrent de celles qui peuvent être prises en charge par l’environnement de programmation pour le positionnement du contrôle. Les propriétés de [**caractères**](/windows/desktop/lwef/the-characters-object) s’appliquent à la présentation visible d’un caractère, et non à l’emplacement du contrôle Microsoft Agent.

Comme pour les méthodes d’objet [**character**](/windows/desktop/lwef/the-characters-object) , vous pouvez accéder aux propriétés d’un caractère à l’aide de la collection [**Characters**](/windows/desktop/lwef/the-characters-object) ou simplifier votre syntaxe en déclarant une variable objet et en la définissant sur un caractère de la collection. Dans l’exemple suivant, test1 et test2 seront définis sur la même valeur :


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Étant donné que le serveur charge un caractère de manière asynchrone, assurez-vous que le caractère a été chargé avant d’interroger ses propriétés, par exemple à l’aide de l’événement [**RequestComplete**](requestcomplete-event.md) . Dans le cas contraire, les propriétés peuvent retourner des valeurs incorrectes.

 

 