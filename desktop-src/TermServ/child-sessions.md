---
title: Sessions enfants
description: À compter de Windows Server 2012 et Windows 8, Bureau à distance prend en charge le concept de session enfant, qui est une session de Bureau à distance de bouclage spéciale qui est liée à la session existante d’un utilisateur.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190791"
---
# <a name="child-sessions"></a><span data-ttu-id="a90d1-103">Sessions enfants</span><span class="sxs-lookup"><span data-stu-id="a90d1-103">Child Sessions</span></span>

<span data-ttu-id="a90d1-104">À compter de Windows Server 2012 et Windows 8, Bureau à distance prend en charge le concept de *session enfant*, qui est une session de bureau à distance de bouclage spéciale qui est liée à la session existante d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a90d1-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="a90d1-105">Les sessions enfants ne sont pas prises en charge sur les systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="a90d1-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="a90d1-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="a90d1-106">Windows RT</span></span>  
<span data-ttu-id="a90d1-107">Option d’installation minimale de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a90d1-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="a90d1-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="a90d1-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="a90d1-109">Un système ne peut avoir qu’une seule session enfant active et connectée à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="a90d1-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="a90d1-110">La session enfant peut être arrêtée en se déconnectant directement de celle-ci, ou elle sera arrêtée lorsque sa session parente se terminera.</span><span class="sxs-lookup"><span data-stu-id="a90d1-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="a90d1-111">Avant de pouvoir utiliser des sessions enfants sur un système, vous devez activer la fonctionnalité de session enfant en appelant la fonction [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) .</span><span class="sxs-lookup"><span data-stu-id="a90d1-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="a90d1-112">Vous pouvez également déterminer si les sessions enfants ont été activées à l’aide de la fonction [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .</span><span class="sxs-lookup"><span data-stu-id="a90d1-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="a90d1-113">Une session enfant ne peut être créée qu’à partir d’une session d’utilisateur existante à l’aide du [contrôle ActiveX Bureau à distance](remote-desktop-activex-control.md) et en définissant la propriété « ConnectToChildSession » avec [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) avant la connexion.</span><span class="sxs-lookup"><span data-stu-id="a90d1-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="a90d1-114">Lorsque la méthode [**IMsTscAx. Connect**](imstscax-connect.md) est appelée, le contrôle ActiveX Bureau à distance se connecte automatiquement à la session enfant sans demander d’informations d’identification, sauf si l’utilisateur est connecté à la session parente à l’aide d’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="a90d1-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="a90d1-115">Contrairement à une session de Bureau à distance normale, un utilisateur n’a pas besoin du droit interactif distant pour se connecter à la session enfant, car il s’agit d’une session de bouclage.</span><span class="sxs-lookup"><span data-stu-id="a90d1-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="a90d1-116">Une session enfant ne peut pas être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="a90d1-116">A child session cannot be locked.</span></span> <span data-ttu-id="a90d1-117">Il n’a pas d’écran de veille et aucun écran d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="a90d1-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="a90d1-118">Par ailleurs, contrairement à une session normale, si la stratégie de texte de connexion WinLogon est définie, le texte d’ouverture de session ne sera pas affiché dans cette session enfant.</span><span class="sxs-lookup"><span data-stu-id="a90d1-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="a90d1-119">En outre, il n’y aura aucun effet sur les stratégies de groupe Connexion Bureau à distance Timeout sur la session enfant si ces stratégies sont définies.</span><span class="sxs-lookup"><span data-stu-id="a90d1-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="a90d1-120">Les API suivantes sont utilisées conjointement avec les sessions enfants :</span><span class="sxs-lookup"><span data-stu-id="a90d1-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="a90d1-121">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="a90d1-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="a90d1-122">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a90d1-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="a90d1-123">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="a90d1-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="a90d1-124">Propriété « ConnectToChildSession » dans [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="a90d1-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




