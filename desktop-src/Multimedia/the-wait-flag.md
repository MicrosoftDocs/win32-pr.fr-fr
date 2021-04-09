---
title: L’indicateur d’attente
description: L’indicateur d’attente
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Indicateur de MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029868"
---
# <a name="the-wait-flag"></a><span data-ttu-id="21046-104">L’indicateur d’attente</span><span class="sxs-lookup"><span data-stu-id="21046-104">The Wait Flag</span></span>

<span data-ttu-id="21046-105">Les commandes MCI sont généralement renvoyées immédiatement à l’utilisateur, même s’il faut quelques minutes pour effectuer l’action initiée par la commande.</span><span class="sxs-lookup"><span data-stu-id="21046-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="21046-106">Vous pouvez utiliser l' \_ indicateur d’attente MCI pour indiquer à l’appareil d’attendre que l’action demandée soit terminée avant de retourner le contrôle à l’application.</span><span class="sxs-lookup"><span data-stu-id="21046-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="21046-107">Par exemple, la commande [**Play**](play.md) suivante ne retourne pas de contrôle à l’application tant que la lecture n’est pas terminée :</span><span class="sxs-lookup"><span data-stu-id="21046-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="21046-108">L’utilisateur peut annuler une opération d’attente en appuyant sur une touche d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="21046-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="21046-109">Par défaut, cette clé est CTRL + ATTN.</span><span class="sxs-lookup"><span data-stu-id="21046-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="21046-110">Les applications peuvent redéfinir cette clé à l’aide de la commande [**break**](break.md) ([**\_ Pause MCI**](mci-break.md)).</span><span class="sxs-lookup"><span data-stu-id="21046-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="21046-111">(**L' \_ interruption MCI** utilise la structure de l' [**\_ interruption \_ MCI**](mci-break-parms.md) .) Quand une opération d’attente est annulée, MCI tente de retourner le contrôle à l’application sans interrompre la commande associée à l’indicateur « WAIT ».</span><span class="sxs-lookup"><span data-stu-id="21046-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




