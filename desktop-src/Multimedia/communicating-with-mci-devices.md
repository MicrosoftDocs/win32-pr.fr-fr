---
title: Communication avec les périphériques MCI
description: Communication avec les périphériques MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString macro)
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106544152"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="0148e-105">Communication avec les périphériques MCI</span><span class="sxs-lookup"><span data-stu-id="0148e-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="0148e-106">Le pilote de chaque périphérique MCI gère une liste de ses paramètres et capacités actuels. il peut donc émettre une réponse exacte lorsqu’il est interrogé pour obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="0148e-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="0148e-107">Lorsque vous souhaitez communiquer avec un périphérique MCI, vous pouvez utiliser des macros et des fonctions MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="0148e-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="0148e-108">La plupart des commandes et requêtes MCI les plus courantes sont définies en tant que macros.</span><span class="sxs-lookup"><span data-stu-id="0148e-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="0148e-109">Toutefois, si la tâche que vous voulez effectuer n’est pas disponible en tant que fonction ou macro, vous pouvez envoyer des commandes MCI directement au pilote de périphérique à l’aide de la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) ou en utilisant la forme message ou chaîne des commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="0148e-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="0148e-110">L’utilisation de la macro **MCIWndSendString** revient à utiliser la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) comme suit :</span><span class="sxs-lookup"><span data-stu-id="0148e-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="0148e-111">Les paramètres de [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) incluent uniquement le handle de fenêtre et la forme de chaîne de la commande.</span><span class="sxs-lookup"><span data-stu-id="0148e-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="0148e-112">Pour récupérer les informations retournées par une commande de chaîne, utilisez la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="0148e-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="0148e-113">Pour plus d’informations sur MCI, consultez [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="0148e-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="0148e-114">Vous devez exclure l’alias d’appareil de la commande MCI quand vous utilisez **MCIWndSendString**.</span><span class="sxs-lookup"><span data-stu-id="0148e-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="0148e-115">La bibliothèque MCIWnd ajoute cet alias lors de l’envoi de la commande à l’appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="0148e-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 