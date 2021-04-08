---
title: Connexion d’une fenêtre de capture à un pilote de capture
description: Connexion d’une fenêtre de capture à un pilote de capture
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Message WM_CAP_DRIVER_CONNECT
- capDriverConnect macro)
- capGetDriverDescription fonction)
- Message WM_CAP_DRIVER_GET_NAME
- capDriverGetName macro)
- Message WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion macro)
- Message WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672970"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="803ed-112">Connexion d’une fenêtre de capture à un pilote de capture</span><span class="sxs-lookup"><span data-stu-id="803ed-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="803ed-113">Vous pouvez connecter ou déconnecter dynamiquement une fenêtre de capture à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="803ed-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="803ed-114">Vous pouvez connecter ou associer une fenêtre de capture à un pilote de capture à l’aide du message de [**\_ \_ \_ connexion du pilote WM Cap**](wm-cap-driver-connect.md) (ou de la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ).</span><span class="sxs-lookup"><span data-stu-id="803ed-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="803ed-115">Une fois qu’une fenêtre de capture et le pilote de capture sont connectés, vous pouvez envoyer des messages spécifiques à l’appareil au pilote de capture associé à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="803ed-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="803ed-116">Si plusieurs périphériques de capture sont installés sur un système, vous pouvez connecter une fenêtre de capture à un pilote de périphérique de capture vidéo spécifique en spécifiant un entier pour le paramètre *wParam* du \_ message de connexion du pilote WM Cap \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="803ed-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="803ed-117">L’entier est un index qui identifie un pilote de capture vidéo listé dans le registre ou dans \[ la \] section drivers du fichier SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="803ed-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="803ed-118">Utilisez zéro pour la première entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="803ed-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="803ed-119">Vous pouvez récupérer le nom et la version d’un pilote de capture installé à l’aide de la fonction [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) .</span><span class="sxs-lookup"><span data-stu-id="803ed-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="803ed-120">Votre application peut utiliser cette fonction pour énumérer les périphériques de capture et les pilotes installés, afin que l’utilisateur puisse sélectionner un appareil de capture pour se connecter à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="803ed-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="803ed-121">Vous pouvez récupérer le nom du pilote de périphérique de capture connecté à une fenêtre de capture à l’aide du message [**WM \_ Cap \_ Driver \_ obtenir le \_ nom**](wm-cap-driver-get-name.md) (ou la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ).</span><span class="sxs-lookup"><span data-stu-id="803ed-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="803ed-122">Pour récupérer la version d’un pilote de capture installé, utilisez le message [**WM \_ Cap \_ Driver \_ obtenir la \_ version**](wm-cap-driver-get-version.md) (ou la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).</span><span class="sxs-lookup"><span data-stu-id="803ed-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="803ed-123">Vous pouvez déconnecter une fenêtre de capture d’un pilote de capture à l’aide du message de [**\_ \_ \_ déconnexion du pilote WM Cap**](wm-cap-driver-disconnect.md) (ou de la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).</span><span class="sxs-lookup"><span data-stu-id="803ed-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="803ed-124">Quand une fenêtre de capture est détruite, tous les pilotes de périphérique de capture vidéo connectés sont automatiquement déconnectés.</span><span class="sxs-lookup"><span data-stu-id="803ed-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




