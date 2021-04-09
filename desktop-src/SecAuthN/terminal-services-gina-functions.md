---
description: Lorsque les services Terminal Server sont activés, GINA doit appeler les fonctions de prise en charge de Winlogon pour terminer l’installation de chaque utilisateur, pour interroger les informations d’identification d’une session cliente des services Terminal Server et pour se déconnecter d’une session réseau des services Terminal Server. Notez que les DLL GINA sont ignorées dans Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Fonctions GINA des services Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862398"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="11fb7-103">Fonctions GINA des services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="11fb7-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="11fb7-104">Lorsque les services Terminal Server sont activés, [*Gina*](../secgloss/g-gly.md) doit appeler les fonctions de prise en charge de [*Winlogon*](../secgloss/w-gly.md) pour terminer l’installation de chaque utilisateur, pour interroger les [*informations d’identification*](../secgloss/c-gly.md) d’une session cliente des services Terminal Server et pour se déconnecter d’une session réseau des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="11fb7-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="11fb7-105">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11fb7-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="11fb7-106">Ces fonctions de prise en charge sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="11fb7-106">These support functions include the following.</span></span>



| <span data-ttu-id="11fb7-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="11fb7-107">Function</span></span>                                                                     | <span data-ttu-id="11fb7-108">Description</span><span class="sxs-lookup"><span data-stu-id="11fb7-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11fb7-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="11fb7-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="11fb7-110">Termine l’installation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11fb7-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="11fb7-111">**WlxQueryClientCredentials**</span><span class="sxs-lookup"><span data-stu-id="11fb7-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="11fb7-112">Appelé pour interroger les informations d’identification des clients distants qui n’utilisent pas de licence de connecteur Internet.</span><span class="sxs-lookup"><span data-stu-id="11fb7-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="11fb7-113">**WlxQueryInetConnectorCredentials**</span><span class="sxs-lookup"><span data-stu-id="11fb7-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="11fb7-114">Appelé pour interroger les informations d’identification des clients distants qui utilisent une licence de connecteur Internet.</span><span class="sxs-lookup"><span data-stu-id="11fb7-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="11fb7-115">**WlxQueryTerminalServicesData**</span><span class="sxs-lookup"><span data-stu-id="11fb7-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="11fb7-116">Appelé pour récupérer les informations de configuration de l’utilisateur des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="11fb7-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="11fb7-117">**WlxDisconnect**</span><span class="sxs-lookup"><span data-stu-id="11fb7-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="11fb7-118">Appelé pour se déconnecter d’une session réseau des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="11fb7-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="11fb7-119">Pour accéder à ces fonctions de prise en charge de Winlogon, la DLL GINA doit utiliser la structure [**wlx \_ Dispatch \_ version \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) .</span><span class="sxs-lookup"><span data-stu-id="11fb7-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="11fb7-120">Dans la fonction [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) de la Gina, les deux paramètres doivent être au moins wlx \_ version \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="11fb7-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
