---
title: Interfaces du fournisseur de protocole Desktop déconseillées
description: Les interfaces suivantes sont déconseillées et ne doivent plus être utilisées. Pour les nouveaux projets, utilisez à la place les interfaces des interfaces du fournisseur protocole RDP (Remote Desktop Protocol).
ms.assetid: FD64A6B9-AE15-4311-BD69-4824CAF53544
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11a586084bc4938727e632ca196e97117f7b8a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841545"
---
# <a name="deprecated-desktop-protocol-provider-interfaces"></a><span data-ttu-id="6d7d1-104">Interfaces du fournisseur de protocole Desktop déconseillées</span><span class="sxs-lookup"><span data-stu-id="6d7d1-104">Deprecated Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="6d7d1-105">Les interfaces suivantes sont déconseillées et ne doivent plus être utilisées.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-105">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="6d7d1-106">Pour les nouveaux projets, utilisez à la place les interfaces des [interfaces du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="6d7d1-106">For new projects, use the [Remote Desktop Protocol Provider Interfaces](custom-remote-protocol-interfaces.md) interfaces instead.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d7d1-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6d7d1-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6d7d1-108">**IWTSProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-108">**IWTSProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection)
</dt> <dd>

<span data-ttu-id="6d7d1-109">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-109">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) is no longer available.</span></span> <span data-ttu-id="6d7d1-110">Utilisez plutôt [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-110">Instead, use [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-111">**IWTSProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-111">**IWTSProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="6d7d1-112">[**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-112">[**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) is no longer available.</span></span> <span data-ttu-id="6d7d1-113">Utilisez plutôt [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-113">Instead, use [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-114">**IWTSProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-114">**IWTSProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="6d7d1-115">[**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-115">[**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) is no longer available.</span></span> <span data-ttu-id="6d7d1-116">Utilisez plutôt [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-116">Instead, use [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-117">**IWTSProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-117">**IWTSProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener)
</dt> <dd>

<span data-ttu-id="6d7d1-118">[**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-118">[**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) is no longer available.</span></span> <span data-ttu-id="6d7d1-119">Utilisez plutôt [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-119">Instead, use [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-120">**IWTSProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-120">**IWTSProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="6d7d1-121">[**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-121">[**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) is no longer available.</span></span> <span data-ttu-id="6d7d1-122">Utilisez plutôt [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-122">Instead, use [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-123">**IWTSProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-123">**IWTSProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="6d7d1-124">[**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-124">[**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) is no longer available.</span></span> <span data-ttu-id="6d7d1-125">Utilisez plutôt [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-125">Instead, use [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-126">**IWTSProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-126">**IWTSProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager)
</dt> <dd>

<span data-ttu-id="6d7d1-127">[**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-127">[**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) is no longer available.</span></span> <span data-ttu-id="6d7d1-128">Utilisez plutôt [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-128">Instead, use [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-129">**IWTSProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-129">**IWTSProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="6d7d1-130">[**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-130">[**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) is no longer available.</span></span> <span data-ttu-id="6d7d1-131">Utilisez plutôt [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-131">Instead, use [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback).</span></span>

</dd> <dt>

[<span data-ttu-id="6d7d1-132">**IWTSProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="6d7d1-132">**IWTSProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="6d7d1-133">[**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="6d7d1-133">[**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) is no longer available.</span></span> <span data-ttu-id="6d7d1-134">Utilisez plutôt [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection).</span><span class="sxs-lookup"><span data-stu-id="6d7d1-134">Instead, use [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection).</span></span>

</dd> </dl>

 

 




