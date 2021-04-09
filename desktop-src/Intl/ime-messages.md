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
# <a name="ime-messages"></a>Messages IME

Le système d’exploitation envoie des messages de fenêtre IME à la procédure de fenêtre d’une application lorsque certains événements se produisent et affectent les fenêtres IME. Par exemple, le système d’exploitation envoie le message [**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md) à l’application lorsqu’une fenêtre est activée. Les applications qui ne prennent pas en charge l’IME transmettent ces messages à la fonction [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , qui les envoie à la fenêtre IME par défaut correspondante. Les applications prenant en charge l’IME traitent ces messages ou les transfèrent à leurs propres fenêtres IME.

Votre application peut diriger une fenêtre IME pour exécuter une commande, par exemple, modifier la position d’une fenêtre de composition, à l’aide du message de [**\_ \_ contrôle de l’IME WM**](wm-ime-control.md) . L’IME notifie l’application des modifications apportées à la chaîne de composition à l’aide du message de [**\_ \_ composition de l’IME WM**](wm-ime-composition.md) et des modifications générales de l’état des fenêtres IME en envoyant le message de notification de l' [**\_ IME \_ WM**](wm-ime-notify.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 
