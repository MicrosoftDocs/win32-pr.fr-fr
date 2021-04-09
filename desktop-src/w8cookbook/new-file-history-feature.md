---
title: Nouvelle fonctionnalité historique des fichiers
description: Nouvelle fonctionnalité historique des fichiers
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102469"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="82099-103">Nouvelle fonctionnalité historique des fichiers</span><span class="sxs-lookup"><span data-stu-id="82099-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="82099-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="82099-104">Platform</span></span>

<span data-ttu-id="82099-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="82099-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="82099-106">Description</span><span class="sxs-lookup"><span data-stu-id="82099-106">Description</span></span>

<span data-ttu-id="82099-107">La nouvelle fonctionnalité historique des fichiers remplace la fonction de sauvegarde et de restauration existante, et offre une protection pour les fichiers utilisateur stockés dans les bibliothèques utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82099-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="82099-108">Un ensemble d’API permettant aux développeurs d’activer l’historique des fichiers par programmation et de sélectionner une cible de stockage spécifique est fourni.</span><span class="sxs-lookup"><span data-stu-id="82099-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="82099-109">La documentation relative à ces API est disponible sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="82099-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="82099-110">Cela peut affecter les flux de travail liés à la protection et à la documentation des données qui dépendent de la fonctionnalité de sauvegarde et de restauration Windows.</span><span class="sxs-lookup"><span data-stu-id="82099-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="82099-111">Nous vous déconseillons d’utiliser les deux fonctionnalités en même temps.</span><span class="sxs-lookup"><span data-stu-id="82099-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="82099-112">L’historique des fichiers vérifie s’il existe une planification de sauvegarde et qu’elle est active et si elle en trouve une, elle ne permet pas aux utilisateurs de l’activer.</span><span class="sxs-lookup"><span data-stu-id="82099-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="82099-113">Dans ce cas, les utilisateurs qui souhaitent utiliser l’historique des fichiers devront supprimer la planification de sauvegarde Windows.</span><span class="sxs-lookup"><span data-stu-id="82099-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="82099-114">Manifestation</span><span class="sxs-lookup"><span data-stu-id="82099-114">Manifestation</span></span>

<span data-ttu-id="82099-115">Les workflows peuvent être interrompus et la documentation de la méthode précédente pour accéder à la fonctionnalité de sauvegarde et de restauration Windows doit être mise à jour pour refléter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="82099-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="82099-116">Solution</span><span class="sxs-lookup"><span data-stu-id="82099-116">Solution</span></span>

<span data-ttu-id="82099-117">Révisez les applications qui contiennent des flux de travail qui ont un impact négatif sur la nouvelle fonctionnalité historique des fichiers pour supprimer les conflits et incorporer le nouvel ensemble d’API.</span><span class="sxs-lookup"><span data-stu-id="82099-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="82099-118">Tests</span><span class="sxs-lookup"><span data-stu-id="82099-118">Tests</span></span>

<span data-ttu-id="82099-119">L’API permet aux développeurs de déterminer si l’historique des fichiers est activé.</span><span class="sxs-lookup"><span data-stu-id="82099-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




