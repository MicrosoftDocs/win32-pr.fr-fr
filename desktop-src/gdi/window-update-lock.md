---
description: Un verrou de mise à jour de fenêtre est une suspension temporaire du dessin dans une fenêtre.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Verrou de mise à jour de fenêtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202481"
---
# <a name="window-update-lock"></a>Verrou de mise à jour de fenêtre

Un *verrou de mise à jour de fenêtre* est une suspension temporaire du dessin dans une fenêtre. Le système utilise le verrou pour empêcher d’autres fenêtres de dessiner sur le rectangle de suivi chaque fois que l’utilisateur déplace ou dimensionne une fenêtre. Les applications peuvent utiliser le verrou pour empêcher le dessin s’ils effectuent des opérations de déplacement ou de dimensionnement similaires avec leurs propres fenêtres.

Une application utilise la fonction [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) pour définir ou supprimer un verrou de mise à jour de fenêtre, en spécifiant la fenêtre à verrouiller. Le verrou s’applique à la fenêtre spécifiée et à toutes ses fenêtres enfants. Lorsque le verrou est défini, les fonctions [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) et [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retournent un contexte de périphérique d’affichage avec une région visible vide. À partir de cela, l’application peut continuer à dessiner dans la fenêtre, mais toute la sortie est découpée. Le verrou persiste jusqu’à ce que l’application l’efface en appelant **LockWindowUpdate**, en spécifiant la **valeur null** pour la fenêtre. Bien que **LockWindowUpdate** force la zone visible d’une fenêtre à être vide, la fonction ne rend pas la fenêtre spécifiée invisible et n’efface pas le \_ bit de style visible par WS.

Une fois le verrou défini, l’application peut utiliser la fonction [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , avec la \_ valeur DCX LOCKWINDOWUPDATE, pour récupérer un contexte de périphérique d’affichage à dessiner sur la fenêtre verrouillée. Cela permet à l’application de dessiner un rectangle de suivi lors du traitement des messages du clavier ou de la souris. Le système utilise cette méthode lorsque l’utilisateur déplace et dimensionne des fenêtres. **GetDCEx** récupère le contexte de périphérique d’affichage dans le cache de contexte de périphérique d’affichage, de sorte que l’application doit libérer le contexte de périphérique dès que possible après le dessin.

Lorsqu’un verrou de mise à jour de fenêtre est défini, le système crée un rectangle englobant cumulé pour chaque fenêtre verrouillée. Lorsque le verrou est désactivé, le système utilise ce rectangle englobant pour définir la région de mise à jour de la fenêtre et de ses fenêtres enfants, en forçant un message de [**\_ peinture WM**](wm-paint.md) éventuel. Si le rectangle englobant cumulé est vide (autrement dit, si aucun dessin ne s’est produit pendant que le verrou a été défini), la région de mise à jour n’est pas définie.

 

 



