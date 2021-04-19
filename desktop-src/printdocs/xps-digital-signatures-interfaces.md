---
description: Interfaces API de signature numérique XPS
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: Interfaces API de signature numérique XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534076"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="15f6a-103">Interfaces API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="15f6a-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="15f6a-104">Contenu</span><span class="sxs-lookup"><span data-stu-id="15f6a-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15f6a-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="15f6a-105">In this section</span></span>



| <span data-ttu-id="15f6a-106">Interface</span><span class="sxs-lookup"><span data-stu-id="15f6a-106">Interface</span></span>                                                                           | <span data-ttu-id="15f6a-107">Description</span><span class="sxs-lookup"><span data-stu-id="15f6a-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15f6a-108">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="15f6a-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="15f6a-109">Représente une signature numérique unique.</span><span class="sxs-lookup"><span data-stu-id="15f6a-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="15f6a-110">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="15f6a-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="15f6a-111">Représente un bloc de demandes de signature stockées dans une partie SignatureDefinitions.</span><span class="sxs-lookup"><span data-stu-id="15f6a-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="15f6a-112">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="15f6a-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="15f6a-113">Collection d’interfaces [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) .</span><span class="sxs-lookup"><span data-stu-id="15f6a-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="15f6a-114">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="15f6a-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="15f6a-115">Collection de pointeurs d’interface [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) .</span><span class="sxs-lookup"><span data-stu-id="15f6a-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="15f6a-116">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="15f6a-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="15f6a-117">Gère les signatures numériques et les demandes de signature numérique d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="15f6a-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="15f6a-118">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="15f6a-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="15f6a-119">Accède aux composants d’une demande de signature.</span><span class="sxs-lookup"><span data-stu-id="15f6a-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="15f6a-120">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="15f6a-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="15f6a-121">Collection d’interfaces [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) .</span><span class="sxs-lookup"><span data-stu-id="15f6a-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="15f6a-122">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="15f6a-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="15f6a-123">Permet d’accéder aux options de signature individuelles utilisées par les nouvelles signatures.</span><span class="sxs-lookup"><span data-stu-id="15f6a-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




