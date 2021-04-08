---
title: Automatisation de la lecture
description: Automatisation de la lecture
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate macro)
- MCIWndPlay macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675582"
---
# <a name="automating-playback"></a><span data-ttu-id="4b255-105">Automatisation de la lecture</span><span class="sxs-lookup"><span data-stu-id="4b255-105">Automating Playback</span></span>

<span data-ttu-id="4b255-106">Vous pouvez automatiser la lecture dans votre application à l’aide de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) et de la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , ainsi que de la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="4b255-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="4b255-107">Pour automatiser la lecture, spécifiez les \_ styles MCIWNDF NOPLAYBAR et MCIWNDF \_ NOTIFYMODE dans le paramètre \**MCIWndCreate \* \* \* dwStyle* .</span><span class="sxs-lookup"><span data-stu-id="4b255-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="4b255-108">Spécifiez le \_ style MCIWNDF NOPLAYBAR pour masquer la barre d’outils, et le \_ style MCIWNDF NOTIFYMODE pour émettre un message de notification approprié lorsque l’appareil s’arrête.</span><span class="sxs-lookup"><span data-stu-id="4b255-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="4b255-109">Vous pouvez lire l’appareil ou le fichier spécifié dans **MCIWndCreate** à l’aide de **MCIWndPlay**.</span><span class="sxs-lookup"><span data-stu-id="4b255-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="4b255-110">La macro MCIWndPlay commence à lire le contenu à partir de sa position de lecture actuelle et continue jusqu’à sa fin.</span><span class="sxs-lookup"><span data-stu-id="4b255-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="4b255-111">Vous pouvez détruire ou fermer une fenêtre MCIWnd à l’aide de la macro [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) ou [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="4b255-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="4b255-112">La macro **MCIWndDestroy** ferme l’appareil ou le fichier et détruit la fenêtre MCIWnd en invalidant son handle.</span><span class="sxs-lookup"><span data-stu-id="4b255-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="4b255-113">Si votre application peut réutiliser la fenêtre MCIWnd, utilisez **MCIWndClose** pour fermer l’appareil sans détruire la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4b255-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="4b255-114">Votre application peut détecter quand l’appareil s’arrête de fonctionner et fermer automatiquement la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4b255-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="4b255-115">Pour ce faire, spécifiez le \_ style MCIWNDF NOTIFYMODE pour le paramètre *DwStyle* de [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="4b255-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="4b255-116">L’appareil envoie alors un message [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) à chaque fois qu’il change de mode.</span><span class="sxs-lookup"><span data-stu-id="4b255-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="4b255-117">Votre application peut intercepter ce message pour déterminer si l’appareil a cessé de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="4b255-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="4b255-118">Lorsque l’appareil s’arrête, l’application ferme la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4b255-118">When the device stops playing, the application closes the window.</span></span>

 

 




