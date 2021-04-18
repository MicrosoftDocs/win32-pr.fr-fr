---
description: Sauvegardez les volumes lorsque les applications sur un système continuent d’écrire sur les volumes. Réduisez le temps d’arrêt des applications en créant rapidement un instantané (cliché instantané) d’un volume qui duplique toutes les données. Effectuez une sauvegarde multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Service VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527191"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="70ef7-105">Service VSS</span><span class="sxs-lookup"><span data-stu-id="70ef7-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="70ef7-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="70ef7-106">Purpose</span></span>

<span data-ttu-id="70ef7-107">Le Service VSS (VSS) est un ensemble d’interfaces COM qui implémentent une infrastructure permettant d’effectuer des sauvegardes de volume alors que les applications sur un système continuent d’écrire sur les volumes.</span><span class="sxs-lookup"><span data-stu-id="70ef7-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="70ef7-108">Pour obtenir une présentation de VSS pour les administrateurs système, consultez [service VSS](/windows-server/storage/file-server/volume-shadow-copy-service) dans la bibliothèque TechNet.</span><span class="sxs-lookup"><span data-stu-id="70ef7-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="70ef7-109">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="70ef7-109">Run-time requirements</span></span>

<span data-ttu-id="70ef7-110">VSS est pris en charge sur Microsoft Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70ef7-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="70ef7-111">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la documentation relative à cet élément.</span><span class="sxs-lookup"><span data-stu-id="70ef7-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="70ef7-112">Toutes les applications VSS 32 bits (demandeurs, fournisseurs et enregistreurs) doivent s’exécuter en tant qu’applications natives 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="70ef7-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="70ef7-113">Leur exécution sous WOW64 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70ef7-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="70ef7-114">Pour plus d’informations, consultez [configurations et restrictions prises en charge](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="70ef7-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="70ef7-115">**Windows Server 2003 et Windows XP :** L’exécution de demandeurs VSS 32 bits sous WOW64 est prise en charge, mais pas pour les sauvegardes de l’état du système.</span><span class="sxs-lookup"><span data-stu-id="70ef7-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="70ef7-116">L’exécution des fournisseurs et des enregistreurs VSS 32 bits sous WOW64 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70ef7-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="70ef7-117">La prise en charge de l’exécution de demandeurs 32 bits sous WOW64 a été supprimée dans Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="70ef7-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="70ef7-118">Un cliché instantané créé sur Windows Server 2003 R2 ou Windows Server 2003 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2008 R2 ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="70ef7-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="70ef7-119">Un cliché instantané créé sur Windows Server 2008 R2 ou Windows Server 2008 ne peut pas être utilisé sur un ordinateur qui exécute Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70ef7-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="70ef7-120">Toutefois, un cliché instantané créé sur Windows Server 2008 peut être utilisé sur un ordinateur qui exécute Windows Server 2008 R2, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="70ef7-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="70ef7-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="70ef7-121">In this section</span></span>



| <span data-ttu-id="70ef7-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="70ef7-122">Topic</span></span>                                                          | <span data-ttu-id="70ef7-123">Description</span><span class="sxs-lookup"><span data-stu-id="70ef7-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70ef7-124">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="70ef7-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="70ef7-125">Décrit le modèle d’objet VSS, les stratégies de sauvegarde et de restauration, et comment créer des fournisseurs, des demandeurs et des enregistreurs VSS.</span><span class="sxs-lookup"><span data-stu-id="70ef7-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="70ef7-126">Référence</span><span class="sxs-lookup"><span data-stu-id="70ef7-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="70ef7-127">Décrit les classes, les types de données, les énumérations, les fonctions, les interfaces et les structures VSS.</span><span class="sxs-lookup"><span data-stu-id="70ef7-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="70ef7-128">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="70ef7-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ef7-129">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="70ef7-129">Windows Vista and later</span></span>            | <span data-ttu-id="70ef7-130">VSS est disponible dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="70ef7-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="70ef7-131">Vous pouvez installer le kit de développement logiciel (SDK) pour Windows 7 et Windows Server 2008 R2 à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="70ef7-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="70ef7-132">Vous pouvez également télécharger la [version ISO](https://www.microsoft.com/download/details.aspx?id=8442) du kit de développement logiciel (SDK) à partir du centre de téléchargement Windows.</span><span class="sxs-lookup"><span data-stu-id="70ef7-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="70ef7-133">Les versions précédentes du kit de développement logiciel (SDK) peuvent être téléchargées à partir de la [page de téléchargement SDK Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70ef7-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="70ef7-134">Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="70ef7-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="70ef7-135">VSS est disponible dans le kit de développement logiciel (SDK) Service VSS 7,2, que vous pouvez télécharger à partir du [Centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=23490).</span><span class="sxs-lookup"><span data-stu-id="70ef7-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="70ef7-136">Notez que les fichiers vssapi. lib 64 bits dans les répertoires du répertoire Win2003 \\ obj peuvent être utilisés pour les versions 64 bits de Windows Server 2003 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70ef7-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
