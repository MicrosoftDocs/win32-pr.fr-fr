---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28aee044b9b25ff529a8c49943b6fd0bbb4d8175a5f3a9b6d482923170f4bdc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609489"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Récupère si la grammaire vocale pour les commandes globales de l’agent est activée.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Adresse qui reçoit la **valeur true** si la grammaire vocale pour les commandes globales de l’agent est activée, **false** si elle est désactivée.

</dd> </dl>

Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère. Lorsque cette méthode retourne la **valeur false**, les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets de [**commande**](/windows/desktop/lwef/the-command-object) d’autres clients, ne sont pas inclus dans la grammaire. Cela vous permet de les éliminer de la grammaire active actuelle de votre client. Toutefois, ce paramètre ne reflète pas l’inclusion de ces commandes dans le menu contextuel du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 