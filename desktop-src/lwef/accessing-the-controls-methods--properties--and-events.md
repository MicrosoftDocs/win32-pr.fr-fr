---
title: Accès aux méthodes, propriétés et événements de contrôles
description: Accès aux méthodes, propriétés et événements de contrôles
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed14138da0e6aef0bba46be796813cbe0945195dec2243bbb8bb763ddfb47517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480745"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>Accès aux méthodes, propriétés et événements de contrôles

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

l’utilisation du contrôle Microsoft Agent avec Visual Basic est très similaire à l’utilisation du contrôle avec VBScript, sauf que les événements dans Visual Basic doivent inclure le type de données des paramètres passés. L’ajout du contrôle Microsoft Agent à un formulaire inclut automatiquement les événements de Microsoft Agent avec les paramètres appropriés. Elle crée également automatiquement une connexion au serveur de l’agent lors de l’exécution de l’application.

Vous pouvez également être en mesure d’utiliser la syntaxe de création de object’s de votre langage de programmation pour créer une instance du contrôle au moment de l’exécution. par exemple, dans Visual Basic (5,0 ou version ultérieure), si vous incluez le contrôle Microsoft Agent 2,0 dans les références de votre projet, vous pouvez utiliser une [**avec des événements**](https://www.bing.com/search?q=**With+Events**). [**Nouvelle**](https://www.bing.com/search?q=**New**) déclaration. si vous n’incluez pas la référence, VB génère une erreur indiquant que Microsoft Agent n’a pas pu démarrer (code d’erreur 80042502).

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

pour les versions de VB antérieures à 5,0, vous pouvez utiliser le mot clé VB [**New**](https://www.bing.com/search?q=**New**) sans déclaration [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) ou la fonction VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) , mais ces conventions n’exposent pas les événements du contrôle de l’Agent. Vous devez également utiliser la propriété [**Connected**](https://www.bing.com/search?q=**Connected**) avant de référencer des méthodes ou des propriétés de l’agent. si ce n’est pas le cas, VB génère une erreur indiquant que Microsoft Agent n’a pas pu démarrer (code d’erreur 80042502).

De même, pour d’autres langages de programmation, vous devrez peut-être utiliser la propriété [**Connected**](https://www.bing.com/search?q=**Connected**) pour établir une connexion au serveur COM (Component Object Model) de l’agent avant que votre code puisse appeler l’une des méthodes ou propriétés du contrôle de l’agent. En outre, pour certains langages de programmation, les méthodes et les propriétés de l’agent peuvent ne pas être exposées directement, sauf si vous déclarez le contrôle de l’agent à l’aide de son type. Par exemple, dans Microsoft Access 97, vous devez déclarer l’objet comme agent de type pour que les méthodes et les propriétés s’affichent dans la zone de liste déroulante répertorier automatiquement les membres lorsque vous tapez.

la plupart des langages de programmation qui prennent en charge les contrôles ActiveX suivent des conventions similaires à celles des Visual Basic. Pour les langages de programmation qui ne prennent pas en charge les collections d’objets, vous pouvez utiliser la méthode de [**caractères**](https://www.bing.com/search?q=**Character**) et la méthode de [**commande**](https://www.bing.com/search?q=**Command**) pour accéder aux méthodes et aux propriétés des éléments de la collection.

des langages de programmation comme Visual Basic, qui permettent d’accéder aux types d’objets exposés par le contrôle de l’Agent, vous permettent de les utiliser dans vos déclarations d’objet. Par exemple, au lieu de déclarer un objet en tant que type générique :

``` syntax
   Dim Genie as Object
```

Vous pouvez déclarer un objet en tant que type spécifique :

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

Cela peut améliorer les performances globales de votre application.

Pour certains types d’objets, vous pouvez trouver deux types qui sont identiques, à l’exception du suffixe « ex ». Si les deux existent, utilisez le type « ex », car cela fournit toutes les fonctionnalités de l’agent. Les équivalents non-« ex » sont inclus uniquement pour la compatibilité descendante.

 

 




