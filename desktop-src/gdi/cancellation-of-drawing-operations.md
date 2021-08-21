---
description: Lorsque des applications de dessin complexes effectuent des opérations graphiques de longue durée, elles consomment des ressources système précieuses.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Annulation des opérations de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470031"
---
# <a name="cancellation-of-drawing-operations"></a>Annulation des opérations de dessin

Lorsque des applications de dessin complexes effectuent des opérations graphiques de longue durée, elles consomment des ressources système précieuses. En tirant parti des fonctionnalités multitâches du système, une application peut utiliser des threads et la fonction [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) pour gérer ces opérations. Par exemple, si l’opération graphique effectuée par le thread A consomme les ressources nécessaires, thread B peut appeler la fonction CancelDC pour arrêter cette opération.

 

 



