---
title: Objet de la requête
description: Objet de la requête
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc9ecf65403ca6dbb471c81a65b105bcc5b69701760a73f8fbc8a5684a9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882392"
---
# <a name="the-request-object"></a>Objet de la requête

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le serveur traite certaines méthodes de manière asynchrone. Cela permet à votre code d’application de continuer pendant que la méthode se termine. Quand une application cliente appelle l’une de ces méthodes, le contrôle crée et retourne un objet de [**demande**](/windows/desktop/lwef/the-request-object) pour la demande. Vous pouvez utiliser l’objet de **requête** pour suivre l’état de la méthode en affectant une variable objet à la méthode. dans Visual Basic, commencez par déclarer une variable objet :


```
   Dim MyRequest as Object
```



Dans VBScript, vous n’incluez pas le type de variable dans votre déclaration :


```
   Dim MyRequest
```



et utilisent l’instruction Set de Visual Basic pour assigner la variable à l’appel de méthode :


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



Cela ajoute une référence à l’objet de [**requête**](/windows/desktop/lwef/the-request-object) . L’objet de **requête** sera détruit lorsqu’il n’y aura plus de références à celui-ci. L’endroit où vous déclarez l’objet de **requête** et la manière dont vous l’utilisez détermine sa durée de vie. Si l’objet est déclaré local à une sous-routine ou une fonction, il sera détruit lorsqu’il sera hors de portée. autrement dit, lorsque la sous-routine ou la fonction se termine. Si l’objet est déclaré globalement, il n’est pas détruit tant que le programme n’est pas terminé ou qu’une nouvelle valeur (ou une valeur définie sur "Empty") n’est pas assignée à l’objet.

L’objet de [**requête**](/windows/desktop/lwef/the-request-object) fournit plusieurs propriétés que vous pouvez interroger. Par exemple, la propriété [**Status**](status-property.md) retourne l’état actuel de la demande. Vous pouvez utiliser cette propriété pour vérifier l’état de votre demande :


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



La propriété [**Status**](status-property.md) retourne l’état d’un objet [**Request**](/windows/desktop/lwef/the-request-object) sous la forme d’une valeur entière longue.



| Statut | Définition                                        |
|--------|---------------------------------------------------|
| 0      | La demande s’est terminée correctement.                   |
| 1      | Échec de la requête.                                   |
| 2      | Demande en attente (dans la file d’attente, mais pas terminée). |
| 3      | Demande interrompue.                              |
| 4      | Demande en cours.                              |



 

L’objet de [**requête**](/windows/desktop/lwef/the-request-object) comprend également une valeur d’entier long dans la propriété [**Number**](https://www.bing.com/search?q=**Number**) qui retourne l’erreur ou la cause du code d' [**État**](status-property.md) . Si aucune valeur n’est, cette valeur est égale à zéro (0). La propriété [**Description**](description-property.md) contient une valeur de chaîne qui correspond au numéro d’erreur. Si la chaîne n’existe pas, la **Description** contient « erreur définie par l’application ou définie par l’objet ».

Pour connaître les valeurs et la signification retournées par la propriété [**Number**](https://www.bing.com/search?q=**Number**) , consultez [codes d’erreur](microsoft-agent-error-codes.md).

Le serveur place les demandes d’animation dans la file d’attente du caractère spécifié. Cela permet au serveur de lire l’animation sur un thread distinct et le code de votre application peut continuer pendant que les animations sont lues. Si vous créez une référence d’objet de [**demande**](/windows/desktop/lwef/the-request-object) , le serveur vous avertit automatiquement quand une demande d’animation a démarré ou est terminée par le biais des événements [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) et [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) . Étant donné que les méthodes qui retournent des objets de **demande** sont asynchrones et peuvent ne pas se terminer pendant la portée de la fonction appelante, déclarez votre référence à l’objet de **requête** globalement.

Les méthodes suivantes peuvent être utilisées pour retourner un objet de [**requête**](/windows/desktop/lwef/the-request-object) : [**GestureAt**](gestureat-method.md), [**obtenir**](get-method.md), [**Masquer**](hide-method.md), [**interrompre**](interrupt-method.md), [**charger**](load-method.md), [**MoveTo**](moveto-method.md), [**lire**](play-method.md), [**Afficher**](show-method.md), [**parler**](speak-method.md)et [**attendre**](https://www.bing.com/search?q=**Wait**).

 

 