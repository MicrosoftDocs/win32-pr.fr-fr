---
description: L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour interroger ou modifier la base de données de services installés. Ses commandes correspondent aux fonctions fournies par le SCM. La syntaxe est la suivante.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configuration d’un service à l’aide de SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514801"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="f0f06-105">Configuration d’un service à l’aide de SC</span><span class="sxs-lookup"><span data-stu-id="f0f06-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="f0f06-106">L’SDK Windows contient un utilitaire de ligne de commande, Sc.exe, qui peut être utilisé pour interroger ou modifier la base de données de services installés.</span><span class="sxs-lookup"><span data-stu-id="f0f06-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="f0f06-107">Ses commandes correspondent aux fonctions fournies par le SCM.</span><span class="sxs-lookup"><span data-stu-id="f0f06-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="f0f06-108">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="f0f06-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f06-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0f06-109">Syntax</span></span>

<span data-ttu-id="f0f06-110">**SC** \[ *Nom du serveur* \] *Commande* \[  \] ServiceName \[  \] option1 \[ *option2* \] ...</span><span class="sxs-lookup"><span data-stu-id="f0f06-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="f0f06-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nom du serveur*</span><span class="sxs-lookup"><span data-stu-id="f0f06-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="f0f06-112">Nom de serveur facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0f06-112">Optional server name.</span></span> <span data-ttu-id="f0f06-113">Utilisez le formulaire \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="f0f06-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="f0f06-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Commande*</span><span class="sxs-lookup"><span data-stu-id="f0f06-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="f0f06-115">L’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0f06-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="f0f06-116">boot</span><span class="sxs-lookup"><span data-stu-id="f0f06-116">boot</span></span></dd> <dd><span data-ttu-id="f0f06-117">config</span><span class="sxs-lookup"><span data-stu-id="f0f06-117">config</span></span></dd> <dd><span data-ttu-id="f0f06-118">create</span><span class="sxs-lookup"><span data-stu-id="f0f06-118">create</span></span></dd> <dd><span data-ttu-id="f0f06-119">supprimer</span><span class="sxs-lookup"><span data-stu-id="f0f06-119">delete</span></span></dd> <dd><span data-ttu-id="f0f06-120">description</span><span class="sxs-lookup"><span data-stu-id="f0f06-120">description</span></span></dd> <dd><span data-ttu-id="f0f06-121">EnumDepend</span><span class="sxs-lookup"><span data-stu-id="f0f06-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="f0f06-122">échec</span><span class="sxs-lookup"><span data-stu-id="f0f06-122">failure</span></span></dd> <dd><span data-ttu-id="f0f06-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="f0f06-123">failureflag</span></span></dd> <dd><span data-ttu-id="f0f06-124">GetDisplayName,</span><span class="sxs-lookup"><span data-stu-id="f0f06-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="f0f06-125">GetKeyName</span><span class="sxs-lookup"><span data-stu-id="f0f06-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="f0f06-126">Verrouillage</span><span class="sxs-lookup"><span data-stu-id="f0f06-126">Lock</span></span></dd> <dd><span data-ttu-id="f0f06-127">qc</span><span class="sxs-lookup"><span data-stu-id="f0f06-127">qc</span></span></dd> <dd><span data-ttu-id="f0f06-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="f0f06-128">qdescription</span></span></dd> <dd><span data-ttu-id="f0f06-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="f0f06-129">qfailure</span></span></dd> <dd><span data-ttu-id="f0f06-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="f0f06-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="f0f06-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="f0f06-131">qprivs</span></span></dd> <dd><span data-ttu-id="f0f06-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="f0f06-132">qsidtype</span></span></dd> <dd><span data-ttu-id="f0f06-133">query</span><span class="sxs-lookup"><span data-stu-id="f0f06-133">query</span></span></dd> <dd><span data-ttu-id="f0f06-134">QueryEx</span><span class="sxs-lookup"><span data-stu-id="f0f06-134">queryex</span></span></dd> <dd><span data-ttu-id="f0f06-135">privilèges</span><span class="sxs-lookup"><span data-stu-id="f0f06-135">privs</span></span></dd> <dd><span data-ttu-id="f0f06-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="f0f06-136">QueryLock</span></span></dd> <dd><span data-ttu-id="f0f06-137">sdset</span><span class="sxs-lookup"><span data-stu-id="f0f06-137">sdset</span></span></dd> <dd><span data-ttu-id="f0f06-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="f0f06-138">sdshow</span></span></dd> <dd><span data-ttu-id="f0f06-139">showsid</span><span class="sxs-lookup"><span data-stu-id="f0f06-139">showsid</span></span></dd> <dd><span data-ttu-id="f0f06-140">sidtype</span><span class="sxs-lookup"><span data-stu-id="f0f06-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="f0f06-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*FormName*</span><span class="sxs-lookup"><span data-stu-id="f0f06-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="f0f06-142">Nom du service, tel qu’il a été spécifié lors de son installation.</span><span class="sxs-lookup"><span data-stu-id="f0f06-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="f0f06-143"><span id="option1"></span><span id="OPTION1"></span>*option 1*</span><span class="sxs-lookup"><span data-stu-id="f0f06-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="f0f06-144">Paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="f0f06-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f0f06-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span><span class="sxs-lookup"><span data-stu-id="f0f06-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="f0f06-146">Paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="f0f06-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0f06-147">Notes</span><span class="sxs-lookup"><span data-stu-id="f0f06-147">Remarks</span></span>

<span data-ttu-id="f0f06-148">Pour afficher la syntaxe complète d’une commande, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f0f06-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="f0f06-149"> *commande* SC</span><span class="sxs-lookup"><span data-stu-id="f0f06-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0f06-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0f06-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f06-151">Configuration de service</span><span class="sxs-lookup"><span data-stu-id="f0f06-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="f0f06-152">Installation, suppression et énumération des services</span><span class="sxs-lookup"><span data-stu-id="f0f06-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



