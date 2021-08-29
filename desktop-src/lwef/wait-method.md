---
title: Wait, méthode
description: Wait, méthode
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81949957146756e989fcb577a1bdd5a0c9a2a6fd60932220e39950327ba3061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715709"
---
# <a name="wait-method"></a>Wait, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Fait en sorte que la file d’attente d’animation du caractère spécifié attende jusqu’à la fin de la demande d’animation spécifiée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ * _Demande_ d’attente



| Partie      | Description                                                                     |
|-----------|---------------------------------------------------------------------------------|
| *Requête* | Objet de [**requête**](/windows/desktop/lwef/the-request-object) spécifiant une animation particulière. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez cette méthode uniquement lorsque vous prenez en charge plusieurs caractères (simultanés) et que vous essayez de séquencer l’interaction des caractères. (Pour un caractère unique, chaque demande d’animation est lue de manière séquentielle, à l’issue de la requête précédente.) Si vous avez deux caractères et que vous souhaitez que la demande d’animation d’un caractère attende la fin de l’animation de l’autre caractère, définissez la méthode **Wait** sur l’objet de [**requête**](/windows/desktop/lwef/the-request-object) d’animation de l’autre caractère. Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez interrompre :


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



Vous pouvez également simplifier votre code en appelant simplement **Wait** directement, à l’aide d’une demande d’animation spécifique.


```
   Robby.Wait Genie.Play "GestureRight"
```



Cela évite de devoir déclarer explicitement un objet de [**requête**](/windows/desktop/lwef/the-request-object) .

 

 