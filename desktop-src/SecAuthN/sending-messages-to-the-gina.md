---
description: Winlogon envoie des messages au GINA lorsque des boîtes de dialogue s’affichent. Ces messages sont tous encapsulés dans le \_ message wlx WM \_ SAS comme suit.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Envoi de messages au GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb52da6a2a66d901207485ed97592a97286902ba51c54ec4924240ab9403a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918318"
---
# <a name="sending-messages-to-the-gina"></a>Envoi de messages au GINA

[*Winlogon*](../secgloss/w-gly.md) envoie des messages au [*Gina*](../secgloss/g-gly.md) lorsque des boîtes de dialogue s’affichent. Ces messages sont tous encapsulés dans le \_ message wlx WM \_ SAS comme suit.



| Type de séquence de vigilance sécurisée dans le paramètre wParam | Description                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ \_ type SAS \_ CTRL \_ Alt \_ Suppr                     | Indique qu’une séquence de touches CTRL + ALT + SUPPR a été reçue.                                                                                      |
| WLX \_ de \_ type SAS \_ SC \_ Insert                         | Indique qu’une [*carte à puce*](../secgloss/s-gly.md) a été insérée dans un appareil compatible. |
| \_type SAS \_ wlx \_ SC \_ Remove                         | Indique qu’une carte à puce a été supprimée d’un appareil compatible.                                                                        |
| \_déconnexion \_ utilisateur du type SAS \_ wlx \_                       | Indique qu’un utilisateur a demandé la fermeture de session.                                                                                                       |
| \_ \_ \_ \_ délai d’expiration du type SAS wlx SCRNSVR                   | Indique que l’économiseur d’écran doit être exécuté en raison de l’absence d’entrée utilisateur.                                                                      |
| \_ \_ \_ délai d’expiration du type SAS wlx                            | Indique qu’aucune entrée utilisateur n’a été reçue dans le délai d’attente spécifié.                                                               |



 

Pour les délais d’attente et les dépassements, Winlogon ferme la boîte de dialogue une fois que le message a été envoyé. Ce message est envoyé de sorte que l’opération de la boîte de dialogue peut répondre de manière utile (par exemple, en se fermant à son tour si une déconnexion s’est produite).

Pour les délais d’attente d’entrée, la boîte de dialogue est fermée avec le code d' \_ \_ expiration d’entrée wlx DLG \_ .

Pour les délais d’expiration de l’économiseur d’écran, la boîte de dialogue est fermée avec le code WLX \_ DLG \_ \_ économiseur \_ d’écran Timeout.

Pour les fermetures de session, l’opération de la boîte de dialogue est fermée avec le code WLX \_ DLG \_ User \_ Logoff.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Initialisation de Winlogon](initializing-winlogon.md)
</dt> <dt>

[États Winlogon](winlogon-states.md)
</dt> <dt>

[Opérations de Temps de service de boîte de dialogue prises en charge](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Fonctions de prise en charge de Winlogon](authentication-functions.md)
</dt> </dl>

 

 
