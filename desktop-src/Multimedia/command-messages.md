---
title: Messages de commande
description: Messages de commande
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Messages de commande MCI, à propos de
- Messages de commande MCI, syntaxe
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507866"
---
# <a name="command-messages"></a><span data-ttu-id="ae5ca-106">Messages de commande</span><span class="sxs-lookup"><span data-stu-id="ae5ca-106">Command Messages</span></span>

<span data-ttu-id="ae5ca-107">L’interface de message de commande est conçue pour être utilisée par les applications qui requièrent une interface en langage C pour contrôler les appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-107">The command-message interface is designed to be used by applications requiring a C-language interface to control multimedia devices.</span></span> <span data-ttu-id="ae5ca-108">Il utilise un paradigme de transmission de messages pour communiquer avec les périphériques MCI.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-108">It uses a message-passing paradigm to communicate with MCI devices.</span></span> <span data-ttu-id="ae5ca-109">Vous pouvez envoyer une commande à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae5ca-109">You can send a command by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="ae5ca-110">La fonction **mciSendCommand** retourne la valeur zéro en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-110">The **mciSendCommand** function returns zero if successful.</span></span> <span data-ttu-id="ae5ca-111">Si la fonction échoue, le mot de poids faible de la valeur de retour contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-111">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="ae5ca-112">Vous pouvez transmettre ce code d’erreur à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-112">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-messages"></a><span data-ttu-id="ae5ca-113">Syntaxe des messages de commande</span><span class="sxs-lookup"><span data-stu-id="ae5ca-113">Syntax of Command Messages</span></span>

<span data-ttu-id="ae5ca-114">Les messages de commande MCI sont constitués des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ae5ca-114">MCI command messages consist of the following elements:</span></span>

-   <span data-ttu-id="ae5ca-115">Valeur de message constante</span><span class="sxs-lookup"><span data-stu-id="ae5ca-115">A constant message value</span></span>
-   <span data-ttu-id="ae5ca-116">Structure contenant les paramètres de la commande</span><span class="sxs-lookup"><span data-stu-id="ae5ca-116">A structure containing parameters for the command</span></span>
-   <span data-ttu-id="ae5ca-117">Ensemble d’indicateurs spécifiant des options pour la commande et des champs de validation dans le bloc de paramètres</span><span class="sxs-lookup"><span data-stu-id="ae5ca-117">A set of flags specifying options for the command and validating fields in the parameter block</span></span>

<span data-ttu-id="ae5ca-118">L’exemple suivant utilise la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour envoyer la commande de [**\_ lecture MCI**](mci-play.md) à l’appareil identifié par un identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-118">The following example uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to send the [**MCI\_ PLAY**](mci-play.md) command to the device identified by a device identifier.</span></span>


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



<span data-ttu-id="ae5ca-119">L’identificateur d’appareil indiqué dans le premier paramètre est récupéré lorsque l’appareil est ouvert à l’aide de la commande [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="ae5ca-119">The device identifier given in the first parameter is retrieved when the device is opened using the [**MCI\_ OPEN**](mci-open.md) command.</span></span> <span data-ttu-id="ae5ca-120">Le dernier paramètre est l’adresse d’une structure de [**\_ lecture MCI \_**](mci-play-parms.md) , qui peut contenir des informations sur le début et la fin de la lecture.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-120">The last parameter is the address of an [**MCI\_ PLAY\_ PARMS**](mci-play-parms.md) structure, which might contain information about where to begin and end playback.</span></span> <span data-ttu-id="ae5ca-121">De nombreux messages de commande MCI utilisent une structure pour contenir des paramètres de ce genre.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-121">Many MCI command messages use a structure to contain parameters of this kind.</span></span> <span data-ttu-id="ae5ca-122">Le premier membre de chacune de ces structures identifie la fenêtre qui reçoit un [**message \_ MCINOTIFY mm**](mm-mcinotify.md) lorsque l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="ae5ca-122">The first member of each of these structures identifies the window that receives an [**MM\_ MCINOTIFY**](mm-mcinotify.md) message when the operation finishes.</span></span>

 

 