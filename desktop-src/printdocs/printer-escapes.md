---
description: Les séquences d’échappement fournies par Windows 16 bits ont permis l’accès aux fonctionnalités spéciales de l’appareil.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Échappements de l’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203469"
---
# <a name="printer-escapes"></a><span data-ttu-id="628cd-103">Échappements de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="628cd-103">Printer Escapes</span></span>

<span data-ttu-id="628cd-104">Les séquences d’échappement fournies par Windows 16 bits ont permis l’accès aux fonctionnalités spéciales de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="628cd-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="628cd-105">La plupart de ces séquences d’échappement sont obsolètes, mais quelques-unes sont fournies pour simplifier le portage des applications Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="628cd-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="628cd-106">GDI prend en charge un ensemble complet de fonctions de chemin d’accès que les applications peuvent utiliser à la place des séquences d’échappement pour dessiner des chemins d’accès sur n’importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="628cd-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="628cd-107">Pour obtenir la liste des fonctions qui remplacent certaines séquences d’échappement, consultez la fonction [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .</span><span class="sxs-lookup"><span data-stu-id="628cd-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="628cd-108">Des séquences d’échappement d’imprimante 64 d’origine, seuls **QUERYESCSUPPORT** et **passthrough** peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="628cd-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="628cd-109">Il existe également une fonction d’échappement étendue appelée [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="628cd-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="628cd-110">Cette fonction permet aux applications d’accéder aux fonctionnalités d’un appareil particulier qui ne sont pas directement disponibles via GDI.</span><span class="sxs-lookup"><span data-stu-id="628cd-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



