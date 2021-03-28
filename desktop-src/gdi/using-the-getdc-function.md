---
description: Vous utilisez la fonction GetDC pour effectuer un dessin qui doit se produire instantanément plutôt qu’en cas de traitement d’un \_ message de peinture WM.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Utilisation de la fonction GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973059"
---
# <a name="using-the-getdc-function"></a>Utilisation de la fonction GetDC

Vous utilisez la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) pour effectuer un dessin qui doit se produire instantanément plutôt qu’en cas de traitement d’un message de [**\_ peinture WM**](wm-paint.md) . Ce dessin est généralement en réponse à une action de l’utilisateur, par exemple en effectuant une sélection ou un dessin avec la souris. Dans ce cas, l’utilisateur doit recevoir des commentaires instantanés et ne doit pas être contraint d’arrêter la sélection ou le dessin afin que l’application affiche le résultat. Les sections suivantes montrent comment utiliser GetDC pour dessiner dans une fenêtre :

-   [Dessin avec la souris](drawing-with-the-mouse.md)
-   [Dessin à des intervalles chronométrés](drawing-at-timed-intervals.md)

 

 



