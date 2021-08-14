---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749561"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Avertit une application cliente lorsque l’utilisateur sélectionne une commande ou un caractère pour terminer le mode d’aide.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère pour lequel le mode d’aide est terminé.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificateur de la commande sélectionnée par l’utilisateur.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La cause de l’événement, qui peut être les valeurs suivantes :



| Valeur                                                                         | Description                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const non signed Short** **CSHELPCAUSE \_ commande = 1 ;**<br/>             | L’utilisateur a sélectionné une commande fournie par votre application.                            |
| **const non signed Short** **CSHELPCAUSE \_ OTHERPROGRAM = 2 ;**<br/>        | L’utilisateur a sélectionné l’objet [**commandes**](/windows/desktop/lwef/the-commands-collection-object) d’un autre client. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3 ;**<br/>  | L’utilisateur a sélectionné la commande ouvrir les commandes vocales.                                   |
| **const non signed Short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4 ;**<br/> | L’utilisateur a sélectionné la commande fermer les commandes vocales.                                  |
| **const non signed Short** **CSHELPCAUSE \_ SHOWCHARACTER = 5 ;**<br/>       | L’utilisateur a sélectionné la commande show *CharacterName* .                                  |
| **const non signed Short** **CSHELPCAUSE \_ HIDECHARACTER = 6 ;**<br/>       | L’utilisateur a sélectionné la commande masquer *CharacterName* .                                  |
| caractère CSHELPCAUSE **short non signé** **\_ = 7 ;**<br/>           | L’utilisateur a sélectionné (clic) le caractère.                                           |



 

</dd> </dl>

En général, le mode aide se termine lorsque l’utilisateur clique ou fait glisser le caractère ou sélectionne une commande dans le menu contextuel du caractère. Le fait de cliquer sur un autre caractère ou sur un autre emplacement de l’écran n’annule pas le mode d’aide. Le client qui définit le mode d’aide pour le caractère peut annuler le mode d’aide en affectant à [**IAgentCharacter :: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) la **valeur false**. (Cela ne déclenche pas l’événement **IAgentNotifySinkEx :: HelpComplete** .)

Lorsque l’utilisateur sélectionne une commande à partir du menu contextuel du caractère en mode d’aide, le serveur supprime le menu, appelle l’aide avec la [**HelpContextID**](helpcontextid-property.md)spécifiée de la commande et envoie cet événement. Le contexte (également appelé « qu’est-ce que c’est ? ») La fenêtre d’aide s’affiche à l’emplacement du pointeur. Si l’utilisateur sélectionne la commande par entrée vocale, la fenêtre d’aide s’affiche sur le caractère. Si le caractère est hors écran, la fenêtre s’affiche à l’écran le plus proche de la position actuelle du caractère.

Si le serveur retourne *dwCommandID* sous la forme d’une chaîne vide (""), il indique que l’utilisateur a sélectionné une commande fournie par le serveur.

Cet événement est envoyé uniquement à l’application cliente qui place le caractère dans le mode d’aide.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx :: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

