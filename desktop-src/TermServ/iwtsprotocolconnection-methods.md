---
title: Méthodes IWTSProtocolConnection
description: L’interface IWTSProtocolConnection expose les méthodes suivantes.
ms.assetid: DBB96D6B-F5A5-4CAF-974F-44D76B9CBFB6
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89f63aea6b1904eb4319dcce541aeb4d15d34f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380432"
---
# <a name="iwtsprotocolconnection-methods"></a><span data-ttu-id="bad56-103">Méthodes IWTSProtocolConnection</span><span class="sxs-lookup"><span data-stu-id="bad56-103">IWTSProtocolConnection Methods</span></span>

<span data-ttu-id="bad56-104">\[IWTSProtocolConnection ne peut plus être utilisé à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="bad56-104">\[IWTSProtocolConnection is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="bad56-105">L’interface [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bad56-105">The [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bad56-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bad56-106">In this section</span></span>

-   [<span data-ttu-id="bad56-107">**Méthode AcceptConnection**</span><span class="sxs-lookup"><span data-stu-id="bad56-107">**AcceptConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection)
-   [<span data-ttu-id="bad56-108">**Méthode AuthenticateClientToSession**</span><span class="sxs-lookup"><span data-stu-id="bad56-108">**AuthenticateClientToSession method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession)
-   [<span data-ttu-id="bad56-109">**Close, méthode**</span><span class="sxs-lookup"><span data-stu-id="bad56-109">**Close method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close)
-   [<span data-ttu-id="bad56-110">**Méthode ConnectNotify**</span><span class="sxs-lookup"><span data-stu-id="bad56-110">**ConnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify)
-   [<span data-ttu-id="bad56-111">**Méthode CreateVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="bad56-111">**CreateVirtualChannel method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel)
-   [<span data-ttu-id="bad56-112">**Méthode DisconnectNotify**</span><span class="sxs-lookup"><span data-stu-id="bad56-112">**DisconnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify)
-   [<span data-ttu-id="bad56-113">**Méthode GetClientData**</span><span class="sxs-lookup"><span data-stu-id="bad56-113">**GetClientData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata)
-   [<span data-ttu-id="bad56-114">**Méthode GetLastInputTime**</span><span class="sxs-lookup"><span data-stu-id="bad56-114">**GetLastInputTime method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime)
-   [<span data-ttu-id="bad56-115">**Méthode GetLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="bad56-115">**GetLicenseConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection)
-   [<span data-ttu-id="bad56-116">**Méthode GetLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="bad56-116">**GetLogonErrorRedirector method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector)
-   [<span data-ttu-id="bad56-117">**Méthode GetProtocolHandles**</span><span class="sxs-lookup"><span data-stu-id="bad56-117">**GetProtocolHandles method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles)
-   [<span data-ttu-id="bad56-118">**Méthode GetProtocolStatus**</span><span class="sxs-lookup"><span data-stu-id="bad56-118">**GetProtocolStatus method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus)
-   [<span data-ttu-id="bad56-119">**Méthode GetShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="bad56-119">**GetShadowConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection)
-   [<span data-ttu-id="bad56-120">**Méthode GetUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="bad56-120">**GetUserCredentials method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials)
-   [<span data-ttu-id="bad56-121">**Méthode GetUserData**</span><span class="sxs-lookup"><span data-stu-id="bad56-121">**GetUserData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata)
-   [<span data-ttu-id="bad56-122">**Méthode IsUserAllowedToLogon**</span><span class="sxs-lookup"><span data-stu-id="bad56-122">**IsUserAllowedToLogon method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon)
-   [<span data-ttu-id="bad56-123">**Méthode LogonNotify**</span><span class="sxs-lookup"><span data-stu-id="bad56-123">**LogonNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify)
-   [<span data-ttu-id="bad56-124">**Méthode NotifySessionId**</span><span class="sxs-lookup"><span data-stu-id="bad56-124">**NotifySessionId method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid)
-   [<span data-ttu-id="bad56-125">**Méthode QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="bad56-125">**QueryProperty method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)
-   [<span data-ttu-id="bad56-126">**Méthode SendBeep**</span><span class="sxs-lookup"><span data-stu-id="bad56-126">**SendBeep method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep)
-   [<span data-ttu-id="bad56-127">**Méthode SendPolicyData**</span><span class="sxs-lookup"><span data-stu-id="bad56-127">**SendPolicyData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata)
-   [<span data-ttu-id="bad56-128">**Méthode SessionArbitrationEnumeration**</span><span class="sxs-lookup"><span data-stu-id="bad56-128">**SessionArbitrationEnumeration method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration)
-   [<span data-ttu-id="bad56-129">**SetErrorInfo (méthode)**</span><span class="sxs-lookup"><span data-stu-id="bad56-129">**SetErrorInfo method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo)

 

 




