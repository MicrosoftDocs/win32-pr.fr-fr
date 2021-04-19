---
title: Sauvegarde et restauration de Windows 7 déconseillées
description: Sauvegarde et restauration de Windows 7 déconseillées
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106513746"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="c76ab-103">Sauvegarde et restauration de Windows 7 déconseillées</span><span class="sxs-lookup"><span data-stu-id="c76ab-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="c76ab-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="c76ab-104">Platform</span></span>

<span data-ttu-id="c76ab-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="c76ab-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="c76ab-106">Description</span><span class="sxs-lookup"><span data-stu-id="c76ab-106">Description</span></span>

<span data-ttu-id="c76ab-107">Bien qu’il n’y ait pas de modification comportementale de la sauvegarde et de la restauration, cette fonction est déconseillée et ne sera pas mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c76ab-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="c76ab-108">Il était rarement utilisé et ses fonctionnalités ont été remplacées par la nouvelle fonctionnalité historique des fichiers.</span><span class="sxs-lookup"><span data-stu-id="c76ab-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="c76ab-109">Elle sera commercialisée dans Windows 8 et passionnés de mise à niveau de Windows 7 vers Windows 8, ou qui dépend de la sauvegarde et de la restauration ou de la sauvegarde d’image disque, sera toujours en mesure de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="c76ab-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="c76ab-110">Toutefois, tous les points d’accès à la sauvegarde et à la restauration, à l’exception du panneau de configuration, ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="c76ab-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="c76ab-111">L’applet du panneau de configuration utilisée par la sauvegarde et la restauration a été renommée en récupération de fichiers Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c76ab-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="c76ab-112">Les OEM qui configurent la clé de Registre pour désactiver la notification de sauvegarde dans leurs images n’ont plus besoin de le faire.</span><span class="sxs-lookup"><span data-stu-id="c76ab-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="c76ab-113">Nous vous déconseillons d’utiliser les deux fonctionnalités en même temps.</span><span class="sxs-lookup"><span data-stu-id="c76ab-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="c76ab-114">L’historique des fichiers vérifie si la planification de sauvegarde existe et est active et si elle en trouve une, elle ne permet pas aux utilisateurs de l’activer.</span><span class="sxs-lookup"><span data-stu-id="c76ab-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="c76ab-115">Dans ce cas, les utilisateurs qui souhaitent utiliser l’historique des fichiers devront supprimer la planification de sauvegarde Windows.</span><span class="sxs-lookup"><span data-stu-id="c76ab-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c76ab-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="c76ab-116">Manifestation</span></span>

<span data-ttu-id="c76ab-117">Les workflows peuvent être interrompus et la documentation qui fait référence à la méthode précédente pour accéder à la fonctionnalité de sauvegarde et de restauration Windows doit être mise à jour pour refléter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="c76ab-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c76ab-118">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="c76ab-118">Mitigation</span></span>

<span data-ttu-id="c76ab-119">Les applications qui peuvent déclencher la sauvegarde et la restauration doivent être réécrites pour vérifier si l’historique des fichiers est activé et permettre aux utilisateurs de choisir leur méthode préférée.</span><span class="sxs-lookup"><span data-stu-id="c76ab-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




