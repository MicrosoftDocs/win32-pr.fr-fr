---
description: L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour contrôler un service. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Contrôle d’un service à l’aide de SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536575"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="d55f2-105">Contrôle d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="d55f2-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="d55f2-106">L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour contrôler un service.</span><span class="sxs-lookup"><span data-stu-id="d55f2-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="d55f2-107">Ses commandes correspondent aux fonctions fournies par le SCM.</span><span class="sxs-lookup"><span data-stu-id="d55f2-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="d55f2-108">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="d55f2-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55f2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d55f2-109">Syntax</span></span>

<span data-ttu-id="d55f2-110">**SC** \[ *Nom du serveur* \] *Commande* \[  \] ServiceName \[  \] option1 \[ *option2* \] ...</span><span class="sxs-lookup"><span data-stu-id="d55f2-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="d55f2-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="d55f2-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="d55f2-112">Nom de serveur facultatif.</span><span class="sxs-lookup"><span data-stu-id="d55f2-112">Optional server name.</span></span> <span data-ttu-id="d55f2-113">Utilisez le formulaire \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="d55f2-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="d55f2-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Commande*</span><span class="sxs-lookup"><span data-stu-id="d55f2-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="d55f2-115">L’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d55f2-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="d55f2-116">continue</span><span class="sxs-lookup"><span data-stu-id="d55f2-116">continue</span></span></dd> <dd><span data-ttu-id="d55f2-117">contrôle</span><span class="sxs-lookup"><span data-stu-id="d55f2-117">control</span></span></dd> <dd><span data-ttu-id="d55f2-118">interroger</span><span class="sxs-lookup"><span data-stu-id="d55f2-118">interrogate</span></span></dd> <dd><span data-ttu-id="d55f2-119">pause</span><span class="sxs-lookup"><span data-stu-id="d55f2-119">pause</span></span></dd> <dd><span data-ttu-id="d55f2-120">start</span><span class="sxs-lookup"><span data-stu-id="d55f2-120">start</span></span></dd> <dd><span data-ttu-id="d55f2-121">stop</span><span class="sxs-lookup"><span data-stu-id="d55f2-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d55f2-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*FormName*</span><span class="sxs-lookup"><span data-stu-id="d55f2-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="d55f2-123">Nom du service, tel qu’il a été spécifié lors de son installation.</span><span class="sxs-lookup"><span data-stu-id="d55f2-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="d55f2-124"><span id="option1"></span><span id="OPTION1"></span>*option 1*</span><span class="sxs-lookup"><span data-stu-id="d55f2-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="d55f2-125">Paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="d55f2-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d55f2-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span><span class="sxs-lookup"><span data-stu-id="d55f2-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="d55f2-127">Paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="d55f2-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d55f2-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d55f2-128">Remarks</span></span>

<span data-ttu-id="d55f2-129">Pour afficher la syntaxe complète d’une commande, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d55f2-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="d55f2-130"> *commande* SC</span><span class="sxs-lookup"><span data-stu-id="d55f2-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="d55f2-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d55f2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d55f2-132">Demandes de contrôle de service</span><span class="sxs-lookup"><span data-stu-id="d55f2-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="d55f2-133">Démarrage du service</span><span class="sxs-lookup"><span data-stu-id="d55f2-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



