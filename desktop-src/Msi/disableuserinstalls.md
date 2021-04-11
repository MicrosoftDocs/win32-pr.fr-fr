---
description: Il s’agit d’une stratégie système par ordinateur qui peut être utilisée lorsque l’administrateur souhaite uniquement installer les applications par ordinateur.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112275"
---
# <a name="disableuserinstalls"></a><span data-ttu-id="7ddc1-103">DisableUserInstalls</span><span class="sxs-lookup"><span data-stu-id="7ddc1-103">DisableUserInstalls</span></span>

<span data-ttu-id="7ddc1-104">Il s’agit d’une [stratégie système](system-policy.md) par ordinateur qui peut être utilisée lorsque l’administrateur souhaite uniquement installer les applications par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-104">This is a per-machine [system policy](system-policy.md) that can be used when the administrator only wants per-machine applications installed.</span></span>

<span data-ttu-id="7ddc1-105">Si cette stratégie n’est pas définie, le programme d’installation recherche les applications dans le registre dans l’ordre suivant : applications gérées inscrites en tant qu’applications par utilisateur, applications non gérées inscrites en tant qu’utilisateur et enfin applications inscrites en tant qu’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-105">If this policy is not set, the installer searches the registry for applications in the following order: managed applications registered as per-user, unmanaged applications registered as per-user, and finally applications registered as per-machine.</span></span>

<span data-ttu-id="7ddc1-106">Si cette stratégie est définie sur 1, le programme d’installation ignore toutes les applications inscrites en tant qu’utilisateur et recherche uniquement les applications inscrites en tant qu’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-106">If this policy is set to 1, the installer ignores all applications registered as per-user and only searches for applications registered as per-machine.</span></span> <span data-ttu-id="7ddc1-107">Les appels à l’interface de programmation d’applications Windows Installer ou au système ignorent les applications par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-107">Calls to the Windows Installer application programming interface or system ignore per-user applications.</span></span> <span data-ttu-id="7ddc1-108">Si vous tentez d’effectuer une installation dans le [contexte d’installation](installation-context.md) par utilisateur, le programme d’installation affiche un message d’erreur et arrête l’installation.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-108">An attempt to perform an installation in the per-user [installation context](installation-context.md) causes the installer to display an error message and stops the installation.</span></span> <span data-ttu-id="7ddc1-109">Dans ce cas, le Windows Installer empêche également les installations par utilisateur à partir d’un serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="7ddc1-109">In this case, the Windows Installer also prevents per-user installations from a terminal server.</span></span>

## <a name="registry-key"></a><span data-ttu-id="7ddc1-110">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="7ddc1-110">Registry Key</span></span>

<span data-ttu-id="7ddc1-111">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="7ddc1-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="7ddc1-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="7ddc1-112">Data Type</span></span>

<span data-ttu-id="7ddc1-113">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="7ddc1-113">**REG\_DWORD**</span></span>

 

 



