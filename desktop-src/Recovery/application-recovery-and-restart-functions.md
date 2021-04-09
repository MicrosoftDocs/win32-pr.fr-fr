---
title: Fonctions de récupération et de redémarrage de l’application
description: La récupération et le redémarrage de l’application définissent les fonctions suivantes
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102036"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="876e2-103">Fonctions de récupération et de redémarrage de l’application</span><span class="sxs-lookup"><span data-stu-id="876e2-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="876e2-104">La récupération et le redémarrage de l’application définissent les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="876e2-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="876e2-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="876e2-105">Function</span></span>                                                                               | <span data-ttu-id="876e2-106">Description</span><span class="sxs-lookup"><span data-stu-id="876e2-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="876e2-107">**ApplicationRecoveryFinished**</span><span class="sxs-lookup"><span data-stu-id="876e2-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="876e2-108">Indique que l’application appelante a terminé la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="876e2-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="876e2-109">**ApplicationRecoveryInProgress**</span><span class="sxs-lookup"><span data-stu-id="876e2-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="876e2-110">Indique que l’application appelante continue à récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="876e2-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="876e2-111">**GetApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="876e2-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="876e2-112">Récupère un pointeur vers la routine de rappel de récupération inscrite pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="876e2-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="876e2-113">**GetApplicationRestartSettings**</span><span class="sxs-lookup"><span data-stu-id="876e2-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="876e2-114">Récupère les informations de redémarrage inscrites pour le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="876e2-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="876e2-115">**RegisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="876e2-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="876e2-116">Inscrit l’instance active d’une application pour la récupération.</span><span class="sxs-lookup"><span data-stu-id="876e2-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="876e2-117">**RegisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="876e2-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="876e2-118">Inscrit l’instance active d’une application pour le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="876e2-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="876e2-119">**UnregisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="876e2-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="876e2-120">Supprime l’instance active d’une application de la liste de récupération.</span><span class="sxs-lookup"><span data-stu-id="876e2-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="876e2-121">**UnregisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="876e2-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="876e2-122">Supprime l’instance active d’une application de la liste de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="876e2-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 