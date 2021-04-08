---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101561"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>IAgentCommandsEx::SetGlobalVoiceCommandsEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Définit la propriété [**Enabled**](enabled-property.md) pour la grammaire vocale des commandes globales de Microsoft Agent.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*
</dt> <dd>

Valeur booléenne qui détermine si la grammaire vocale des commandes globales de l’agent est activée. **True** active la grammaire vocale ; **False** le désactive.

</dd> </dl>

Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère. Lorsque la valeur est **false**, l’agent désactive tous les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets de [**commande**](/windows/desktop/lwef/the-command-object) du client. Cela vous permet de les éliminer de la grammaire active actuelle de votre client. Toutefois, étant donné que cela bloque potentiellement l’accès vocal à d’autres clients, réinitialisez cette propriété sur **true** après avoir traité l’entrée vocale de l’utilisateur.

La désactivation de la propriété n’affecte pas le menu contextuel du caractère. Les commandes globales ajoutées par le serveur s’affichent toujours. Vous ne pouvez pas les supprimer du menu contextuel.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 