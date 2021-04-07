---
title: Événement RequestStart
description: Événement RequestStart
ms.assetid: ecfb9691-cbc4-48f5-8e26-a99389e85eed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be5954636084d3cbc299c718f2b4e6d9330ef90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727028"
---
# <a name="requeststart-event"></a>Événement RequestStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le serveur commence une demande en file d’attente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent * * * \_ RequestStart* *  **(** *demande ByVal * * *)**



| Partie      | Description                                            |
|-----------|--------------------------------------------------------|
| *Requête* | Retourne l’objet de [**requête**](/windows/desktop/lwef/the-request-object) . |



 

</dd> </dl>

### <a name="remarks"></a>Notes

L’événement retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . Étant donné que les demandes sont traitées de façon asynchrone, vous pouvez utiliser cet événement pour déterminer à quel moment le serveur commence à traiter une demande (par exemple, une méthode d' [**extraction**](get-method.md), de [**lecture**](play-method.md)ou de [**parole**](speak-method.md) ) et, par conséquent, synchroniser cela avec d’autres actions générées par votre application. L’événement est envoyé uniquement au client qui a créé la référence à l’objet de **requête** et uniquement si vous avez défini une variable globale pour la référence à la demande :


```
   Dim MyRequest 
   Dim Genie 

   Sub window_Onload
   
   Agent1.Characters.Load "Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf"   

   Set Genie = Agent1.Characters("Genie")

   ' This syntax will generate RequestStart and RequestComplete events.
   Set MyRequest = Genie.Get("state", "Showing")

   ' This syntax will not generate RequestStart and RequestComplete events.
   Genie.Get ("state", "Hiding")

   End Sub

   Sub Agent1_RequestStart(ByVal Request)

   If Request = MyRequest Then
      Status = "Loading the Showing animation"

   End Sub
```



L' [**État**](status-property.md) retourne 4 (demande en cours) pour l’objet de [**requête**](/windows/desktop/lwef/the-request-object) retourné.

Étant donné que les objets de [**requête**](/windows/desktop/lwef/the-request-object) d’animation ne sont pas assignés tant que le serveur n’a pas traité la demande, assurez-vous que l’objet de **requête** existe avant d’essayer de l’évaluer. Par exemple, dans Visual Basic, si vous utilisez un conditionnel pour tester si une requête spécifique a été effectuée, vous pouvez utiliser le mot clé **Nothing** :


```
   Sub Agent1_RequestStart (ByVal Request)

   If Not (MyRequest Is Nothing) Then
      If Request = MyRequest Then
      '-- Do whatever
      End If
   End If

   End Sub
```



> [!Note]  
> Dans VBScript 1,0, cet événement se déclenche même si vous ne définissez pas de références à un objet de [**requête**](/windows/desktop/lwef/the-request-object) . Ce problème a été résolu dans VBScript 2,0, qui peut être téléchargé à partir de <https://microsoft.com/msdownload/vbscript/scripting.asp> .

 

### <a name="see-also"></a>Voir aussi

[**Événement RequestComplete**](requestcomplete-event.md)


 

 