---
title: SendMessage, PostMessage et fonctions connexes
description: Cette section décrit les considérations relatives au transfert des messages à l’aide de SendMessage, PostMessage et des fonctions associées avec des messages tactiles.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1274327b53630058779bc3913ce4466394c4c4fa37ba78528d122b8d68e376e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435297"
---
# <a name="sendmessage-postmessage-and-related-functions"></a>SendMessage, PostMessage et fonctions connexes

Cette section décrit les considérations relatives au transfert des messages à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)et des fonctions associées avec des messages tactiles.

Si un message tactile est transféré à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou une autre fonction associée, le handle d’entrée tactile est fermé. Si vous avez récupéré les informations contenues référencées par une poignée d’entrée tactile via un appel à [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), ces données restent valides jusqu’à ce que vous libériez la mémoire.

Une application qui reçoit des messages tactiles transmis via l’un de ces mécanismes est propriétaire du handle d’entrée tactile qu’elle reçoit dans le message *lParam* et est responsable de sa fermeture. Si vous ne fermez pas le descripteur avec un appel à [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), transmettez le message à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)ou transférez le message à l’aide de [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)ou d’une fonction associée, vous obtiendrez une fuite de mémoire.

> [!Note]  
> Les messages tactiles sont soumis aux règles de l’isolation des privilèges de l’interface utilisateur (UIPI) normales lorsqu’ils sont transférés.

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a>Fonctions liées à SendMessage et PostMessage

Les fonctions suivantes peuvent affecter l’état du handle d’entrée tactile.

-   [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   SendNotifyMessage
-   SendMessageCallback
-   SendMessageTimeout
-   PostThreadMessage

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions](mtfunctions.md)
</dt> <dt>

[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 