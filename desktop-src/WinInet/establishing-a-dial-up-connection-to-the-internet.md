---
title: Établissement d’une connexion d’accès à distance à Internet
description: Les fonctions suivantes sont utilisées pour gérer les connexions de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031722"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="fe202-103">Établissement d’une connexion d’accès à distance à Internet</span><span class="sxs-lookup"><span data-stu-id="fe202-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="fe202-104">Les fonctions suivantes sont utilisées pour gérer les connexions de modem.</span><span class="sxs-lookup"><span data-stu-id="fe202-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="fe202-105">**InternetAutodial**</span><span class="sxs-lookup"><span data-stu-id="fe202-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="fe202-106">**InternetAutodialHangup**</span><span class="sxs-lookup"><span data-stu-id="fe202-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="fe202-107">**InternetDial**</span><span class="sxs-lookup"><span data-stu-id="fe202-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="fe202-108">**InternetGetConnectedState**</span><span class="sxs-lookup"><span data-stu-id="fe202-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="fe202-109">**InternetGetConnectedStateEx**</span><span class="sxs-lookup"><span data-stu-id="fe202-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="fe202-110">**InternetHangUp**</span><span class="sxs-lookup"><span data-stu-id="fe202-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="fe202-111">**InternetGoOnline**</span><span class="sxs-lookup"><span data-stu-id="fe202-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="fe202-112">Les fonctions d’accès distant WinINet ne prennent pas en charge les connexions à double numérotation, l’authentification par carte à puce ou les connexions nécessitant une certification basée sur le registre.</span><span class="sxs-lookup"><span data-stu-id="fe202-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe202-113">À compter de Windows Vista et de Windows Server 2008, les fonctions d’accès distant WinINet utilisent les [fonctions RAS](/windows/desktop/RRAS/remote-access-service-functions) pour établir une connexion d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="fe202-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="fe202-114">WinINet prend en charge les fonctionnalités documentées dans la fonction [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .</span><span class="sxs-lookup"><span data-stu-id="fe202-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe202-115">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="fe202-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="fe202-116">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="fe202-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="fe202-117">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="fe202-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 