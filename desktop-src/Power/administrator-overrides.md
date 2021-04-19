---
description: Remplacements de l’administrateur
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Remplacements de l’administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531943"
---
# <a name="administrator-overrides"></a><span data-ttu-id="b2d09-103">Remplacements de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="b2d09-103">Administrator Overrides</span></span>

<span data-ttu-id="b2d09-104">Windows dispose d’une seule liste de contrôle d’accès (ACL) par défaut sur tous les objets de stratégie d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="b2d09-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="b2d09-105">La liste de contrôle d’accès accorde des autorisations de lecture, d’écriture et de modification aux membres du groupe utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="b2d09-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="b2d09-106">L’autorisation lecture seule est accordée à tous les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b2d09-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="b2d09-107">Les applications qui appellent des fonctions de stratégie d’alimentation peuvent déterminer si un utilisateur dispose d’autorisations pour un paramètre d’alimentation spécifié à l’aide de la fonction [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="b2d09-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="b2d09-108">Les paramètres d’alimentation peuvent être remplacés via stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2d09-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="b2d09-109">Les remplacements peuvent être définis via la stratégie de groupe de domaine ou la stratégie de groupe locale.</span><span class="sxs-lookup"><span data-stu-id="b2d09-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="b2d09-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) indique si un paramètre d’alimentation spécifié a une substitution de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2d09-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="b2d09-111">L’outil de ligne de commande **PowerCfg.exe** affiche un message d’erreur lorsqu’une commande ne peut pas être exécutée soit parce que l’utilisateur n’a pas les autorisations nécessaires pour modifier le paramètre d’alimentation, soit parce que le paramètre d’alimentation a une substitution de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b2d09-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="b2d09-112">L’application options d’alimentation du panneau de configuration ne prend pas en charge la configuration des autorisations d’accès à la stratégie d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="b2d09-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="b2d09-113">La modification des autorisations doit être effectuée via **PowerCfg.exe**.</span><span class="sxs-lookup"><span data-stu-id="b2d09-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



