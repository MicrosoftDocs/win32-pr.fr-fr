---
description: Chaque affichage physique est représenté par un handle de moniteur de type HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR et le contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991213"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="f8934-103">HMONITOR et le contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="f8934-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="f8934-104">Chaque affichage physique est représenté par un handle de moniteur de type **HMONITOR**.</span><span class="sxs-lookup"><span data-stu-id="f8934-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="f8934-105">Un **HMONITOR** valide est garanti être non null.</span><span class="sxs-lookup"><span data-stu-id="f8934-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="f8934-106">Un affichage physique a le même **HMONITOR** , à condition qu’il fasse partie du bureau.</span><span class="sxs-lookup"><span data-stu-id="f8934-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="f8934-107">Lorsqu’un message **WM \_ DISPLAYCHANGE** est envoyé, toute analyse peut être supprimée du bureau et son **HMONITOR** devient non valide ou ses paramètres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="f8934-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="f8934-108">Par conséquent, une application doit vérifier si tous les **HMONITORS** sont valides lorsque ce message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="f8934-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="f8934-109">Toute fonction qui retourne un contexte de périphérique d’affichage (DC) retourne normalement un contrôleur de l’écran principal.</span><span class="sxs-lookup"><span data-stu-id="f8934-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="f8934-110">Pour obtenir le contrôleur de l’autre moniteur, utilisez la fonction [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="f8934-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="f8934-111">Vous pouvez utiliser le nom de l’appareil à partir de la fonction [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) pour créer un contrôleur de périphérique avec [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="f8934-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="f8934-112">Toutefois, si la fonction, telle que [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtient un DC pour une fenêtre qui s’étend sur plusieurs affichages, le contrôleur de périphérique s’étend également sur les deux affichages.</span><span class="sxs-lookup"><span data-stu-id="f8934-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



