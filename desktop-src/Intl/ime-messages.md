---
description: Le système d’exploitation envoie des messages de fenêtre IME à la procédure de fenêtre d’une application lorsque certains événements se produisent et affectent les fenêtres IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Messages IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034054"
---
# <a name="ime-messages"></a><span data-ttu-id="7de5c-103">Messages IME</span><span class="sxs-lookup"><span data-stu-id="7de5c-103">IME Messages</span></span>

<span data-ttu-id="7de5c-104">Le système d’exploitation envoie des messages de fenêtre IME à la procédure de fenêtre d’une application lorsque certains événements se produisent et affectent les fenêtres IME.</span><span class="sxs-lookup"><span data-stu-id="7de5c-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="7de5c-105">Par exemple, le système d’exploitation envoie le message [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) à l’application lorsqu’une fenêtre est activée.</span><span class="sxs-lookup"><span data-stu-id="7de5c-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="7de5c-106">Les applications qui ne prennent pas en charge l’IME transmettent ces messages à la fonction [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui les envoie à la fenêtre IME par défaut correspondante.</span><span class="sxs-lookup"><span data-stu-id="7de5c-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="7de5c-107">Les applications prenant en charge l’IME traitent ces messages ou les transfèrent à leurs propres fenêtres IME.</span><span class="sxs-lookup"><span data-stu-id="7de5c-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="7de5c-108">Votre application peut diriger une fenêtre IME pour exécuter une commande, par exemple, modifier la position d’une fenêtre de composition, à l’aide du message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) .</span><span class="sxs-lookup"><span data-stu-id="7de5c-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="7de5c-109">L’IME notifie l’application des modifications apportées à la chaîne de composition à l’aide du message de [**\_ \_ composition de l’IME WM**](wm-ime-composition.md) et des modifications générales de l’état des fenêtres IME en envoyant le message de notification de l' [**\_ IME \_ WM**](wm-ime-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7de5c-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7de5c-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7de5c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7de5c-111">À propos du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="7de5c-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
