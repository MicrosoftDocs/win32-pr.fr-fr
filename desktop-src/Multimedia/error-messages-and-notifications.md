---
title: Messages d’erreur et notifications
description: Messages d’erreur et notifications
ms.assetid: 7f804364-d8be-4e52-ab0e-fba05bcf76ce
keywords:
- MCIWndGetError macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e40e78c72dc378baa37b56dbb2d5718ae2d85b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110913"
---
# <a name="error-messages-and-notifications"></a>Messages d’erreur et notifications

MCIWnd utilise MCI pour contrôler les appareils qui lisent et enregistrent les données multimédias. En général, MCIWnd affiche les erreurs MCI dans une boîte de dialogue d’erreur. Une erreur MCI est générée chaque fois qu’une commande MCI échoue. Par exemple, si votre application tente de reprendre la lecture suspendue à l’aide de la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) et que l’appareil actuel ne prend pas en charge la reprise, une erreur est signalée à l’utilisateur.

MCIWnd vous permet de gérer les messages d’erreur de deux manières :

-   Vous pouvez empêcher les messages d’erreur d’atteindre l’utilisateur. Pour empêcher l’affichage des messages d’erreur MCI, spécifiez le \_ style de fenêtre MCIWNDF NOERRORDLG lorsque vous créez une instance d’une fenêtre MCIWnd à l’aide de la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) ou [CreateWindowEx](/windows/win32/api/winuser/nf-winuser-createwindowexa) .
-   Vous pouvez les rediriger vers votre application pour les afficher. Pour rediriger les messages d’erreur MCI vers votre application, spécifiez le \_ style de fenêtre MCIWNDF NOTIFYERROR lorsque vous créez une instance d’une fenêtre MCIWnd à l’aide de **MCIWndCreate** ou de **CreateWindowEx**.

Lorsque la notification d’erreur est activée, MCIWnd envoie chaque message de notification ([**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)) au gestionnaire de messages principal du parent de la fenêtre MCIWnd. Votre application doit avoir un gestionnaire de messages pour traiter les messages de notification qu’elle reçoit.

Vous pouvez obtenir une description textuelle du message d’erreur MCI le plus récent à l’aide de la macro [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror) . Cette macro retourne le texte dans une mémoire tampon définie par l’application. Si la chaîne d’erreur est plus longue que la mémoire tampon, MCIWnd tronque la chaîne.

Vous pouvez acheminer toutes les notifications vers une autre fenêtre à l’aide de la macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .

 

 