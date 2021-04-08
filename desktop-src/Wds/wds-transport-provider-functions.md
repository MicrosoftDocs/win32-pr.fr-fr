---
title: Fonctions du fournisseur de transport WDS
description: Les fournisseurs de contenu définis par l’utilisateur peuvent exposer les fonctions de rappel suivantes au serveur de multidiffusion.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675437"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="66da7-103">Fonctions du fournisseur de transport WDS</span><span class="sxs-lookup"><span data-stu-id="66da7-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="66da7-104">Les fournisseurs de contenu définis par l’utilisateur peuvent exposer les fonctions de rappel suivantes au serveur de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="66da7-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="66da7-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="66da7-105">Function</span></span>                                                                               | <span data-ttu-id="66da7-106">Description</span><span class="sxs-lookup"><span data-stu-id="66da7-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66da7-107">*WdsTransportProviderCloseContent*</span><span class="sxs-lookup"><span data-stu-id="66da7-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="66da7-108">Ferme un flux de contenu spécifié par un handle.</span><span class="sxs-lookup"><span data-stu-id="66da7-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="66da7-109">*WdsTransportProviderCloseInstance*</span><span class="sxs-lookup"><span data-stu-id="66da7-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="66da7-110">Ferme une instance d’un fournisseur de contenu spécifié par un handle.</span><span class="sxs-lookup"><span data-stu-id="66da7-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="66da7-111">*WdsTransportProviderCompareContent*</span><span class="sxs-lookup"><span data-stu-id="66da7-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="66da7-112">Compare un nom de contenu et une instance spécifiés à un flux de contenu ouvert pour déterminer s’ils sont identiques.</span><span class="sxs-lookup"><span data-stu-id="66da7-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="66da7-113">*WdsTransportProviderCreateInstance*</span><span class="sxs-lookup"><span data-stu-id="66da7-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="66da7-114">Ouvre une nouvelle instance d’un fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="66da7-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="66da7-115">*WdsTransportProviderDumpState*</span><span class="sxs-lookup"><span data-stu-id="66da7-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="66da7-116">Indique au fournisseur de transport d’imprimer un résumé de son état et de toute autre information pertinente dans le journal de suivi.</span><span class="sxs-lookup"><span data-stu-id="66da7-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="66da7-117">*WdsTransportProviderGetContentMetadata*</span><span class="sxs-lookup"><span data-stu-id="66da7-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="66da7-118">Récupère les métadonnées pour un flux de contenu ouvert.</span><span class="sxs-lookup"><span data-stu-id="66da7-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="66da7-119">*WdsTransportProviderGetContentSize*</span><span class="sxs-lookup"><span data-stu-id="66da7-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="66da7-120">Récupère la taille d’un flux de contenu ouvert.</span><span class="sxs-lookup"><span data-stu-id="66da7-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="66da7-121">*WdsTransportProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="66da7-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="66da7-122">Initialise un fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="66da7-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="66da7-123">*WdsTransportProviderOpenContent*</span><span class="sxs-lookup"><span data-stu-id="66da7-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="66da7-124">Ouvre une nouvelle vue statique d’un flux de contenu.</span><span class="sxs-lookup"><span data-stu-id="66da7-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="66da7-125">*WdsTransportProviderReadContent*</span><span class="sxs-lookup"><span data-stu-id="66da7-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="66da7-126">Lit le contenu à partir d’un flux de contenu ouvert.</span><span class="sxs-lookup"><span data-stu-id="66da7-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="66da7-127">*WdsTransportProviderRefreshSettings*</span><span class="sxs-lookup"><span data-stu-id="66da7-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="66da7-128">Indique au fournisseur de transport de relire les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="66da7-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="66da7-129">*WdsTransportProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="66da7-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="66da7-130">Shutsdown le fournisseur de contenu.</span><span class="sxs-lookup"><span data-stu-id="66da7-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="66da7-131">*WdsTransportProviderUserAccessCheck*</span><span class="sxs-lookup"><span data-stu-id="66da7-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="66da7-132">Spécifie l’accès à un flux de contenu basé sur le jeton d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66da7-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




