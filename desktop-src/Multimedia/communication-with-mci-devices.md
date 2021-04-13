---
title: Communication avec les périphériques MCI
description: Communication avec les périphériques MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Périphériques MCI, communication
- MCIWndGetDeviceID macro)
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314711"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="3a39e-106">Communication avec les périphériques MCI</span><span class="sxs-lookup"><span data-stu-id="3a39e-106">Communication with MCI Devices</span></span>

<span data-ttu-id="3a39e-107">Chaque périphérique MCI peut utiliser un ou plusieurs des éléments suivants comme identificateurs :</span><span class="sxs-lookup"><span data-stu-id="3a39e-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="3a39e-108">identificateur d’appareil</span><span class="sxs-lookup"><span data-stu-id="3a39e-108">a device identifier</span></span>
-   <span data-ttu-id="3a39e-109">nom de l’appareil</span><span class="sxs-lookup"><span data-stu-id="3a39e-109">a device name</span></span>
-   <span data-ttu-id="3a39e-110">un alias</span><span class="sxs-lookup"><span data-stu-id="3a39e-110">an alias</span></span>
-   <span data-ttu-id="3a39e-111">nom de fichier du contenu actuellement chargé.</span><span class="sxs-lookup"><span data-stu-id="3a39e-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="3a39e-112">MCIWnd fournit des macros que vous pouvez utiliser pour récupérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="3a39e-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="3a39e-113">Vous pouvez ensuite utiliser ces informations pour communiquer via MCI directement avec les périphériques MCI associés à MCIWnd Windows.</span><span class="sxs-lookup"><span data-stu-id="3a39e-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="3a39e-114">Vous pouvez récupérer l’identificateur de l’appareil MCI actuel à l’aide de la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="3a39e-115">L’identificateur de périphérique MCI est une valeur numérique qui identifie l’instance de l’appareil MCI que votre application utilise.</span><span class="sxs-lookup"><span data-stu-id="3a39e-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="3a39e-116">Votre application peut utiliser cet identificateur lors de la communication avec un périphérique MCI à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="3a39e-117">Pour récupérer le nom de l’appareil MCI actuel, utilisez la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="3a39e-118">Le nom du périphérique MCI est une chaîne se terminant par un caractère null qui identifie le type d’appareil associé à une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3a39e-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="3a39e-119">Votre application peut utiliser ce nom lors de la communication avec un périphérique MCI à l’aide de **mciSendCommand**.</span><span class="sxs-lookup"><span data-stu-id="3a39e-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="3a39e-120">Vous pouvez récupérer l’alias de l’appareil MCI actuel à l’aide de la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="3a39e-121">Votre application peut utiliser cet alias lors de la communication avec un périphérique MCI à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="3a39e-122">Enfin, vous pouvez récupérer le nom de fichier utilisé par un périphérique MCI à l’aide de la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="3a39e-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="3a39e-123">Le nom de fichier identifie le contenu actuellement associé à une fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3a39e-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="3a39e-124">Votre application peut utiliser ce nom de fichier lors de la communication avec un périphérique MCI à l’aide de **mciSendCommand** ou **mciSendString**.</span><span class="sxs-lookup"><span data-stu-id="3a39e-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 