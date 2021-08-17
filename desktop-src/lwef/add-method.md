---
title: Ajouter une méthode
description: Ajouter une méthode
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ae6cc3cd0a39be8b293a6ae64a96859e5d4fcf6d23ff410439422676b3527e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976829"
---
# <a name="add-method"></a>Ajouter une méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Ajoute un objet [Command](the-command-object.md) à la collection [Commands](the-commands-collection-object.md) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Commandes. Ajouter_ un *  *nom*, une *légende*, une *voix*, *activé*, *visible*



| Partie      | Description                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nom*    | Obligatoire. Valeur de chaîne correspondant à l’ID que vous attribuez à la commande.                                                                                                                                                                                                                                        |
| *Caption* | Facultatif. Valeur de chaîne correspondant au nom qui s’affiche dans le menu contextuel du caractère et dans la fenêtre commandes lorsque l’application cliente est active en entrée. Pour plus d’informations, consultez la propriété [Caption](caption-property.md) de l’objet [Command](the-command-object.md) .                       |
| *Voice*   | Facultatif. Valeur de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette commande. Pour plus d’informations sur les alternatives de mise en forme pour la chaîne, consultez la propriété [Voice](voice-property.md) de l’objet de [commande](the-command-object.md) .                                |
| *Activé* | Facultatif. Valeur booléenne indiquant si la commande est activée. La valeur par défaut est **True**. Pour plus d’informations, consultez la propriété [Enabled](enabled-property.md) de l’objet [Command](the-command-object.md) .                                                                                              |
| *Visible* | Facultatif. Valeur booléenne indiquant si la commande est visible dans le menu contextuel du caractère lorsque l’application cliente est en entrée active. La valeur par défaut est **True**. Pour plus d’informations, consultez la propriété [visible](visible-property.md) de l’objet [Command](the-command-object.md) . |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La valeur de la propriété [Name](name-property.md) d’un objet [Command](the-command-object.md) doit être unique au sein de sa collection [Commands](the-commands-collection-object.md) . Vous devez supprimer une commande avant de pouvoir créer une nouvelle commande avec le même paramètre de propriété Name. Toute tentative de création d’une commande avec une propriété Name qui existe déjà génère une erreur.

Cette méthode retourne également un objet [Command](the-command-object.md) . Cela vous permet de déclarer un objet et de lui assigner une commande lorsque vous appelez addMethod.


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Insert (méthode)**](insert-method.md)
</dt> <dt>

[**RemoveAll, méthode**](removeall-method.md)
</dt> <dt>

[**Remove (méthode)**](remove-method.md)
</dt> </dl>

 

 




