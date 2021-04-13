---
title: Propriété Connected
description: Propriété Connected
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310585"
---
# <a name="connected-property"></a>Propriété Connected

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si le contrôle en cours est connecté au serveur Microsoft Agent.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. * * * connecté* *  \[  =  *valeur booléenne*\]



| Partie      | Description                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si le contrôle est connecté. **True** Le contrôle est connecté.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Dans de nombreux cas, la spécification du contrôle crée automatiquement une connexion avec le serveur Microsoft Agent. Par exemple, la spécification du CLSID du contrôle Microsoft Agent dans la <OBJECT> balise d’une page Web ouvre automatiquement une connexion au serveur et la fermeture de la page ferme la connexion. De même, pour les Visual Basic ou d’autres langages qui vous permettent de supprimer un contrôle dans un formulaire, l’exécution automatique du programme ouvre une connexion et la fermeture du programme ferme la connexion. Si le serveur n’est pas en cours d’exécution, il démarre automatiquement.

Toutefois, si vous souhaitez créer un contrôle d’agent au moment de l’exécution, vous devrez peut-être également ouvrir explicitement une nouvelle connexion au serveur à l’aide de la propriété **Connected** . Par exemple, dans Visual Basic vous pouvez créer un objet ActiveX au moment de l’exécution à l’aide de l’instruction Set avec le mot clé **New** (ou la fonction CreateObject). Bien que cette opération crée l’objet, elle risque de ne pas créer la connexion au serveur. Vous pouvez utiliser la propriété **Connected** avant tout code qui appelle l’interface de programmation de Microsoft Agent, comme indiqué dans l’exemple suivant :


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



La création d’un contrôle à l’aide de cette technique n’expose pas les événements du contrôle de l’agent. Dans Visual Basic 5,0 (et versions ultérieures), vous pouvez accéder aux événements du contrôle en incluant le contrôle dans les références de votre projet, et utiliser le mot clé **WithEvents** dans votre déclaration de variable :


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



L’utilisation de **WithEvents** pour créer une instance du contrôle de l’agent au moment de l’exécution ouvre automatiquement la connexion avec le serveur Microsoft Agent. Par conséquent, vous n’avez pas besoin d’inclure une instruction **connectée** .

Vous pouvez fermer votre connexion au serveur en libérant toutes les références que vous avez créées aux objets de l’agent, par exemple IAgentCtlCharacterEx et IAgentCtlCommandEx. Vous devez également libérer votre référence au contrôle de l’agent lui-même. Dans Visual Basic, vous pouvez publier une référence à un objet en affectant à sa variable la valeur **Nothing**. Si vous avez chargé des caractères, déchargez-les avant de libérer l’objet caractère.


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> Vous ne pouvez pas fermer votre connexion au serveur en libérant les références où le composant a été ajouté. Par exemple, vous ne pouvez pas fermer votre connexion au serveur sur des pages Web où vous utilisez la <OBJECT> balise pour déclarer le contrôle ou dans une application de Visual Basic où vous déposez le contrôle sur un formulaire. Si la libération de toutes les références d’agent réduit la plage de travail de l’agent, la connexion est conservée jusqu’à ce que vous atteigniez la page suivante ou que vous quittiez l’application.

 

 

 





