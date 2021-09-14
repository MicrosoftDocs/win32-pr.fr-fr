---
title: Événement HelpComplete
description: Événement HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191932"
---
# <a name="helpcomplete-event"></a>Événement HelpComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Indique que le mode d’aide contextuelle a été quitté.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent. * * * (ByVal* *  *CharacterID * * *, ByVal* *  *Name * * *, ByVal* *  *cause * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère sur lequel l’utilisateur a cliqué sous forme de chaîne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nom*        | Retourne une valeur de chaîne identifiant le nom (ID) de la commande.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Cause*       | Retourne une valeur qui indique ce qui a provoqué l’exécution du mode d’aide. 1 l’utilisateur a sélectionné une commande fournie par votre application.<br/> 2 l’utilisateur a sélectionné l’objet [**commandes**](/windows/desktop/lwef/the-commands-collection-object) d’un autre client.<br/> 3 l’utilisateur a sélectionné la commande ouvrir les commandes vocales.<br/> 4 l’utilisateur a sélectionné la commande fermer les commandes vocales.<br/> 5 l’utilisateur a sélectionné la commande show *CharacterName* .<br/> 6 l’utilisateur a sélectionné la commande masquer *CharacterName* .<br/> 7 l’utilisateur a sélectionné (sur) le caractère.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Notes

En général, le mode d’aide se termine lorsque l’utilisateur clique ou fait glisser le caractère ou sélectionne une commande dans le menu contextuel du caractère. Le fait de cliquer sur un autre caractère ou sur un autre emplacement de l’écran n’annule pas le mode d’aide. Le client qui définit le mode d’aide pour le caractère peut annuler le mode d’aide en affectant à [**HelpModeOn**](helpmodeon-property.md) la **valeur false**. (Cela ne déclenche pas l’événement **HelpComplete** .)

Lorsque l’utilisateur sélectionne une commande à partir du menu contextuel du caractère en mode d’aide, le serveur supprime le menu, appelle l’aide avec la [**HelpContextID**](helpcontextid-property.md)spécifiée de la commande et envoie cet événement. Le contexte (également appelé « qu’est-ce que c’est ? ») La fenêtre d’aide s’affiche à l’emplacement du pointeur. Si l’utilisateur sélectionne la commande par entrée vocale, la fenêtre d’aide s’affiche sur le caractère. Si le caractère est hors écran, la fenêtre s’affiche à l’écran le plus proche de la position actuelle du caractère.

Si le serveur retourne le nom sous la forme d’une chaîne vide (""), il indique que l’utilisateur a sélectionné une commande fournie par le serveur.

Cet événement est envoyé uniquement à l’application cliente qui place le caractère en mode d’aide.

### <a name="see-also"></a>Voir aussi

[**Propriété HelpModeOn**](helpmodeon-property.md), [ **HelpContextID, propriété**](helpcontextid-property.md)


 

