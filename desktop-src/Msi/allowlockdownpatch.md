---
description: Si cette stratégie système par ordinateur n’est pas définie, seuls les administrateurs peuvent corriger les produits existants qui ont été installés à l’aide de privilèges élevés.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951788"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="c52aa-103">AllowLockdownPatch</span><span class="sxs-lookup"><span data-stu-id="c52aa-103">AllowLockdownPatch</span></span>

<span data-ttu-id="c52aa-104">Si cette [stratégie système](system-policy.md) par ordinateur n’est pas définie, seuls les administrateurs peuvent corriger les produits existants qui ont été installés à l’aide de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="c52aa-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="c52aa-105">Si AllowLockdownPatch a la valeur « 1 », les utilisateurs non administratifs peuvent, dans certains cas, appliquer des correctifs aux produits lors de l’exécution d’une installation à l’aide de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="c52aa-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="c52aa-106">Avec la stratégie définie, le correctif peut installer des [mises à niveau mineures](minor-upgrades.md) lors de l’exécution d’une installation utilisant des privilèges élevés, le correctif ne peut pas installer les [mises à niveau majeures](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="c52aa-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="c52aa-107">La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="c52aa-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="c52aa-108">Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c52aa-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="c52aa-109">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="c52aa-109">Registry Key</span></span>

<span data-ttu-id="c52aa-110">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="c52aa-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="c52aa-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c52aa-111">Data Type</span></span>

<span data-ttu-id="c52aa-112">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="c52aa-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c52aa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c52aa-113">Remarks</span></span>

<span data-ttu-id="c52aa-114">N’importe quel utilisateur peut appliquer un correctif au cours d’une installation sans élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="c52aa-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="c52aa-115">La définition de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » donne aux utilisateurs non administratifs la flexibilité supplémentaire pour appliquer des correctifs à n’importe quel produit au cours d’une installation avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="c52aa-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="c52aa-116">Si cette stratégie n’est pas définie, les utilisateurs non administratifs ne peuvent pas appliquer un correctif aux applications attribuées ou publiées.</span><span class="sxs-lookup"><span data-stu-id="c52aa-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="c52aa-117">La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package de correctifs Windows Installer qui installe ou lance ces programmes.</span><span class="sxs-lookup"><span data-stu-id="c52aa-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



