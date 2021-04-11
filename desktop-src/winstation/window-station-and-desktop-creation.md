---
title: Station Windows et création de bureau
description: Le système crée automatiquement la station Windows Interactive.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315143"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="fd9db-103">Station Windows et création de bureau</span><span class="sxs-lookup"><span data-stu-id="fd9db-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="fd9db-104">Le système crée automatiquement la station Windows Interactive.</span><span class="sxs-lookup"><span data-stu-id="fd9db-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="fd9db-105">Lorsqu’un utilisateur interactif se connecte, le système associe la station de fenêtre interactive à la session d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd9db-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="fd9db-106">Le système crée également le Bureau d’entrée par défaut pour la station Windows Interactive (Winsta0 \\ par défaut).</span><span class="sxs-lookup"><span data-stu-id="fd9db-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="fd9db-107">Les processus démarrés par l’utilisateur connecté sont associés au \\ Bureau par défaut Winsta0.</span><span class="sxs-lookup"><span data-stu-id="fd9db-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="fd9db-108">Un processus peut utiliser la fonction [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) pour créer une nouvelle station Windows, et la fonction **CreateDesktop** ou [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) pour créer un nouveau bureau.</span><span class="sxs-lookup"><span data-stu-id="fd9db-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="fd9db-109">Le nombre de postes de travail qui peuvent être créés est limité par la taille du segment de bureau du système.</span><span class="sxs-lookup"><span data-stu-id="fd9db-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="fd9db-110">Pour plus d’informations, consultez [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="fd9db-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="fd9db-111">Lorsqu’un processus non interactif comme une application de service tente de se connecter à une station Windows et qu’il n’existe pas de station Windows pour la session de connexion au processus, le système tente de créer une station Windows et un bureau pour la session.</span><span class="sxs-lookup"><span data-stu-id="fd9db-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="fd9db-112">Le nom de la station de fenêtre créée est basé sur l’identificateur de session d’ouverture de session et le bureau est nommé par défaut, comme décrit ici :</span><span class="sxs-lookup"><span data-stu-id="fd9db-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="fd9db-113">Si un service s’exécute dans le contexte de sécurité du compte LocalSystem mais n’inclut pas l' \_ attribut processus interactif du service \_ , il utilise la station de Windows et le Bureau suivants : service-0x0-3E7 $ \\ default.</span><span class="sxs-lookup"><span data-stu-id="fd9db-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="fd9db-114">Cette station Windows n’étant pas interactive, le service ne peut pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd9db-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="fd9db-115">En outre, les processus créés par le service ne peuvent pas afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd9db-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="fd9db-116">Si le service s’exécute dans le contexte de sécurité d’un compte d’utilisateur, le nom de la station Windows est basé sur le SID d’utilisateur service-0x *Z1* - *Z2*$, où *Z1* est la partie haute du SID d’ouverture de session et *Z2* est la partie inférieure du SID d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="fd9db-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="fd9db-117">Étant donné qu’un SID est unique à la session de connexion, deux services exécutés dans le même contexte de sécurité reçoivent des stations de fenêtre uniques.</span><span class="sxs-lookup"><span data-stu-id="fd9db-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="fd9db-118">Ces stations Windows ne sont pas interactives.</span><span class="sxs-lookup"><span data-stu-id="fd9db-118">These window stations are not interactive.</span></span>

<span data-ttu-id="fd9db-119">La liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) pour la station et le bureau Windows comprend les droits d’accès suivants pour le compte d’utilisateur du service :</span><span class="sxs-lookup"><span data-stu-id="fd9db-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="fd9db-120">Station Windows :</span><span class="sxs-lookup"><span data-stu-id="fd9db-120">Window Station:</span></span>

<dl> <span data-ttu-id="fd9db-121">WINSTA \_ ACCESSCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="fd9db-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="fd9db-122">WINSTA \_ ACCESSGLOBALATOMS</span><span class="sxs-lookup"><span data-stu-id="fd9db-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="fd9db-123">WINSTA \_ CREATEDESKTOP</span><span class="sxs-lookup"><span data-stu-id="fd9db-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="fd9db-124">WINSTA \_ EXITWINDOWS</span><span class="sxs-lookup"><span data-stu-id="fd9db-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="fd9db-125">WINSTA \_ READATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="fd9db-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="fd9db-126">\_droits standard \_ requis</span><span class="sxs-lookup"><span data-stu-id="fd9db-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="fd9db-127">Bureau :</span><span class="sxs-lookup"><span data-stu-id="fd9db-127">Desktop:</span></span>

<dl> <span data-ttu-id="fd9db-128">CREATEMENU de bureau \_</span><span class="sxs-lookup"><span data-stu-id="fd9db-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="fd9db-129">Bureau \_ CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="fd9db-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="fd9db-130">énumération de postes de travail \_</span><span class="sxs-lookup"><span data-stu-id="fd9db-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="fd9db-131">HOOKCONTROL de bureau \_</span><span class="sxs-lookup"><span data-stu-id="fd9db-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="fd9db-132">READOBJECTS de bureau \_</span><span class="sxs-lookup"><span data-stu-id="fd9db-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="fd9db-133">WRITEOBJECTS de bureau \_</span><span class="sxs-lookup"><span data-stu-id="fd9db-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="fd9db-134">\_droits standard \_ requis</span><span class="sxs-lookup"><span data-stu-id="fd9db-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 