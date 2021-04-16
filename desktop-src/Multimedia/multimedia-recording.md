---
title: Enregistrement multimédia
description: Enregistrement multimédia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate fonction)
- MCIWndNew macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379909"
---
# <a name="multimedia-recording"></a><span data-ttu-id="ad1e4-105">Enregistrement multimédia</span><span class="sxs-lookup"><span data-stu-id="ad1e4-105">Multimedia Recording</span></span>

<span data-ttu-id="ad1e4-106">Vous pouvez implémenter des fonctionnalités d’enregistrement dans votre application à l’aide de l’interface utilisateur intégrée à MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-106">You can implement recording capabilities in your application by using the user interface built into MCIWnd.</span></span> <span data-ttu-id="ad1e4-107">Vous pouvez utiliser la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) et la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) pour fournir des contrôles permettant de démarrer et d’arrêter l’enregistrement et d’enregistrer les informations enregistrées.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-107">You can use the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to provide controls for starting and stopping recording and for saving the recorded information.</span></span> <span data-ttu-id="ad1e4-108">À l’aide de **MCIWndCreate**, vous pouvez spécifier des styles de fenêtre pour afficher une fenêtre MCIWnd et inclure le bouton **Enregistrer** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-108">Using **MCIWndCreate**, you can specify window styles to display an MCIWnd window and to include the **Record** button on the toolbar.</span></span> <span data-ttu-id="ad1e4-109">À l’aide de **MCIWndNew**, vous pouvez spécifier le type d’appareil en cours d’enregistrement et spécifier que les informations doivent être capturées dans un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-109">Using **MCIWndNew**, you can specify the device type that is being recorded and specify that the information is to be captured in a new file.</span></span>

<span data-ttu-id="ad1e4-110">Si votre application nécessite une plus grande sophistication, vous pouvez automatiser et personnaliser l’enregistrement à l’aide de la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="ad1e4-110">If your application requires more sophistication, you can automate and customize the recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="ad1e4-111">Pour plus d’informations, consultez [Personnalisation du processus d’enregistrement](customizing-the-recording-process.md).</span><span class="sxs-lookup"><span data-stu-id="ad1e4-111">For more information, see [Customizing the Recording Process](customizing-the-recording-process.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad1e4-112">Certains périphériques, tels que les CD audio et MCIAVI, sont utilisés uniquement pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-112">Some devices, such as CD audio and MCIAVI, are used for playback only.</span></span> <span data-ttu-id="ad1e4-113">D’autres périphériques, tels que les périphériques audio Waveform, peuvent être utilisés pour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-113">Other devices, such as waveform-audio devices, can be used for recording.</span></span> <span data-ttu-id="ad1e4-114">Si vous spécifiez un appareil qui ne peut pas être enregistré, MCIWnd omet le bouton **Enregistrer** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="ad1e4-114">If you specify a device that cannot record, MCIWnd omits the **Record** button from the toolbar.</span></span>

 

 

 




