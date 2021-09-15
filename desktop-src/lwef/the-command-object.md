---
title: Objet Command
description: Objet Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525837"
---
# <a name="the-command-object"></a>Objet Command

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Un objet [**Command**](/windows/desktop/lwef/the-command-object) est un élément d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Le serveur permet à l’utilisateur d’accéder à vos objets de **commande** lorsque votre application cliente devient entrée-active.

-   [Propriétés de l’objet Command](command-object-properties.md)

Pour accéder à la propriété d’un objet [**Command**](/windows/desktop/lwef/the-command-object) , vous le référencez dans sa collection à l’aide de sa propriété [**Name**](name-property.md) . dans VBScript et Visual Basic vous pouvez utiliser directement la propriété **Name** :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Pour les langages de programmation qui ne prennent pas en charge les collections, utilisez la méthode [**Command**](command-method.md) :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Vous pouvez également référencer un objet de commande en créant une référence à celui-ci. dans Visual Basic, déclarez une variable objet et utilisez l’instruction Set pour créer la référence :


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



dans Visual Basic 5,0, vous pouvez également déclarer l’objet comme type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) et créer la référence. Cette Convention permet une liaison précoce, ce qui améliore les performances :


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Dans VBScript, vous pouvez déclarer une référence en tant que type particulier, mais vous pouvez toujours déclarer la variable et la définir sur la [**commande**](/windows/desktop/lwef/the-command-object) dans la collection :


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Une commande peut apparaître dans le menu contextuel du caractère et dans la fenêtre commandes, ou dans les deux. Pour apparaître dans le menu contextuel, il doit avoir une légende et la propriété [**visible**](visible-property.md) doit avoir la valeur **true**. En outre, sa propriété **visible** de l’objet de collection Commands doit également avoir la valeur **true**. Pour apparaître dans la fenêtre commandes, la [**légende**](caption-property.md) et les propriétés [**vocales**](voice-property.md) doivent être définies pour une [**commande**](/windows/desktop/lwef/the-command-object) . Notez que les entrées du menu contextuel d’un caractère ne changent pas pendant que le menu s’affiche. Si vous ajoutez ou supprimez des commandes ou modifiez leurs propriétés alors que le menu contextuel du caractère s’affiche, le menu affiche ces modifications chaque fois que l’utilisateur l’affiche à l’étape suivante. Toutefois, la fenêtre commandes reflète dynamiquement les modifications que vous apportez.

Le tableau suivant résume la façon dont les propriétés d’une [**commande**](/windows/desktop/lwef/the-command-object) affectent sa présentation :



Propriété Caption

Voice-Caption, propriété

Voice, propriété

Propriété visible

Propriété activée

Apparaît dans le menu contextuel du caractère

Apparaît dans la fenêtre commandes

Oui

Oui

Oui

True

True

Normal, utilisation de la [ **légende**](caption-property.md)

Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)

Oui

Oui

Oui

Vrai

False

Désactivé, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Oui

Oui

False

True

N’apparaît pas

Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)

Oui

Oui

Oui

False

False

N’apparaît pas

Non

Oui

Oui

Non 

True

True

Normal, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Oui

Non 

Vrai

False

Désactivé, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Oui

Non 

False

True

N’apparaît pas

Non

Oui

Oui

Non 

False

False

N’apparaît pas

Non

Non 

Oui

Oui

True

True

N’apparaît pas

Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)

Non 

Oui

Oui

Vrai

False

N’apparaît pas

Non

Non 

Oui

Oui

False

True

N’apparaît pas

Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)

Non 

Oui

Oui

False

False

N’apparaît pas

Non

Non 

Oui

Non 

True

True

N’apparaît pas

Non

Non 

Oui

Non 

Vrai

False

N’apparaît pas

Non

Non 

Oui

Non 

False

True

N’apparaît pas

Non

Non 

Oui

Non 

False

False

N’apparaît pas

Non

Oui

Non 

Oui

True

True

Normal, utilisation de la [ **légende**](caption-property.md)

Oui, à l’aide de la [ **légende**](caption-property.md)

Oui

Non 

Oui

Vrai

False

Désactivé, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Non 

Oui

False

True

N’apparaît pas

Oui, à l’aide de la [ **légende**](caption-property.md)

Oui

Non 

Oui

False

False

N’apparaît pas

Non

Oui

Non 

Non 

True

True

Normal, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Non 

Non 

Vrai

False

Désactivé, utilisation de la [ **légende**](caption-property.md)

Non

Oui

Non 

Non 

False

True

N’apparaît pas

Non

Oui

Non 

Non 

False

False

N’apparaît pas

Non

Non 

Non 

Oui

True

True

N’apparaît pas

Non 

Non 

Non 

Oui

Vrai

False

N’apparaît pas

Non

Non 

Non 

Oui

False

True

N’apparaît pas

Non 

Non 

Non 

Oui

False

False

N’apparaît pas

Non

Non 

Non 

Non 

True

True

N’apparaît pas

Non

Non 

Non 

Non 

Vrai

False

N’apparaît pas

Non

Non 

Non 

Non 

False

True

N’apparaît pas

Non

Non 

Non 

Non 

False

False

N’apparaît pas

Non

 Si le paramètre de la propriété a la valeur null. Dans certains langages de programmation, une chaîne vide ne peut pas être interprétée de la même façon qu’une chaîne NULL.  La commande est toujours accessible en voix.<br/>



 

Lorsque le serveur reçoit une entrée pour l’une de vos commandes, il envoie un événement de [**commande**](/windows/desktop/lwef/the-command-object) et transmet le nom de la **commande** en tant qu’attribut de l’objet [**UserInput**](/windows/desktop/lwef/iagentuserinput) . Vous pouvez ensuite utiliser des instructions conditionnelles pour faire correspondre et traiter la **commande**.

 

