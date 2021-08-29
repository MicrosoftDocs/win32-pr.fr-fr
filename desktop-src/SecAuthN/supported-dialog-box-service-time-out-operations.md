---
description: Winlogon met en œuvre deux opérations de délai d’attente, une pour les boîtes de dialogue sécurisées et l’autre pour l’activation et l’arrêt de l’écran de veille.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Opérations de Temps de service de boîte de dialogue prises en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7715cafb426a59bd9773791788dd9914fff0c1fac4a5b820e9cc06416e966eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916448"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Opérations de Temps de service de boîte de dialogue prises en charge

[*Winlogon*](../secgloss/w-gly.md) met en œuvre deux opérations de délai d’attente, une pour les boîtes de dialogue sécurisées et l’autre pour l’activation et l’arrêt de l’écran de veille.

Lorsque vous affichez une boîte de dialogue sécurisée, telle que l’ouverture ou le déverrouillage d’une station de travail, Winlogon peut expirer les boîtes de dialogue et retourner un code de résultat approprié à la procédure de la boîte de dialogue. Winlogon fournit un ensemble de fonctions de prise en charge de boîte de dialogue pour [*Gina*](../secgloss/g-gly.md). la gina doit utiliser ces fonctions au lieu de leurs équivalents Windows pour s’assurer que la gina et Winlogon maintiennent le contrôle approprié sur les boîtes de dialogue. Si vous n’utilisez pas les versions Winlogon de ces fonctions, les utilisateurs non autorisés peuvent accéder au système.

Les services de boîte de dialogue Winlogon sont fournis par les fonctions de prise en charge suivantes.



| Fonction de prise en charge                                               | Description                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | similaire à la fonction Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) .                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | similaire à la fonction Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) .                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | semblable à la fonction Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) .           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | semblable à la fonction Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) .                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | semblable à la fonction Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) . |



 

Les DLL GINA peuvent également recevoir \_ \_ des messages wlx WM SAS de Winlogon. Ces messages sont envoyés aux boîtes de dialogue actives si une [*séquence d’intervention sécurisée*](../secgloss/s-gly.md) (SAS) est reçue. Cela est utile si la GINA est en train de demander le code PIN correspondant pour une [*carte à puce*](../secgloss/s-gly.md)et que la carte est supprimée du [*lecteur*](../secgloss/r-gly.md)de carte à puce. Winlogon utilise WLX \_ DLG \_ SAS comme code de résultat EndDialog lorsqu’un événement SAS se produit pendant une opération de boîte de dialogue.

Les délais d’attente sont également fournis de cette manière. Un \_ message wlx WM \_ wlx est envoyé avec un \_ \_ \_ \_ délai d’expiration du type SAS SCRNSVR ou un délai \_ \_ d’expiration du type SAS wlx \_ . La boîte de dialogue se termine par un code de sortie approprié pour permettre aux développeurs GINA de raccorder les notifications de délai d’attente.

Les boîtes de dialogue GINA peuvent être arrêtées par Winlogon à l’aide du code WLX \_ DLG \_ User \_ Logoff. Cela indique que l’utilisateur s’est déconnecté lors de l’exécution de la boîte de dialogue (par exemple, en appelant la fonction [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) à partir d’un autre thread).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Initialisation de Winlogon](initializing-winlogon.md)
</dt> <dt>

[États Winlogon](winlogon-states.md)
</dt> <dt>

[Envoi de messages au GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Fonctions de prise en charge de Winlogon](authentication-functions.md)
</dt> </dl>

 

 
