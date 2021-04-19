---
title: Insert, méthode
description: Insert, méthode
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106542846"
---
# <a name="insert-method"></a>Insert, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Insère un objet **Command** dans la collection **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). Commands. Insert* *  *Name*, *RefName*, *avant*\_

*Légende*, *voix, activée, visible*



| Partie      | Description                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nom*    | Obligatoire. Valeur de chaîne correspondant à l’ID que vous attribuez à la [**commande**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *RefName* | Obligatoire. Valeur de chaîne correspondant au nom (ID) de la commande juste au-dessus ou au-dessous de l’emplacement où vous souhaitez insérer la nouvelle commande.                                                                                                                                                                 |
| *Avant*  | Optionnel. Valeur booléenne indiquant s’il faut insérer la nouvelle commande avant la commande spécifiée par *RefName*. **True** (valeur par défaut). La nouvelle commande est insérée avant la commande référencée.<br/> **Valeur false** La nouvelle commande est insérée après la commande référencée.<br/> |
| *Caption* | Optionnel. Valeur de chaîne correspondant au nom qui s’affiche dans le menu contextuel du caractère et dans la fenêtre commandes lorsque l’application cliente est active en entrée. Pour plus d’informations, consultez la propriété [**Caption**](caption-property.md)de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .    |
| *Voice*   | Optionnel. Valeur de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette commande. Pour plus d’informations sur les alternatives de mise en forme pour la chaîne, consultez la propriété **Voice** de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .                                  |
| *Enabled* | Optionnel. Valeur booléenne indiquant si la commande est activée. La valeur par défaut est **True**. Pour plus d’informations, consultez la propriété **Enabled** de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .                                                                                                  |
| *Visible* | Optionnel. Valeur booléenne indiquant si la commande est visible dans la fenêtre commandes lorsque l’application cliente est en entrée active. La valeur par défaut est **True**. Pour plus d’informations, consultez la propriété [**visible**](visible-property.md) de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .       |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La valeur de la propriété [**Name**](name-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) doit être unique au sein de sa collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Vous devez supprimer une **commande** avant de pouvoir créer une nouvelle **commande** avec le même paramètre de propriété **Name** . Toute tentative de création d’une **commande** avec une propriété **Name** qui existe déjà génère une erreur.

Cette méthode retourne également un objet [**Command**](/windows/desktop/lwef/the-command-object) . Cela vous permet de déclarer un objet et de lui assigner une **commande** lorsque vous appelez la méthode **Insert** .


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Voir aussi

Méthode [**Add**](add-method.md), méthode [**Remove**](remove-method.md), méthode [**RemoveAll**](removeall-method.md)


 

