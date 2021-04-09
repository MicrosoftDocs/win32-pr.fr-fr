---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ; permet aux utilisateurs non administratifs d’utiliser une boîte de dialogue Parcourir pour localiser les sources des applications gérées.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864498"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="54ea1-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="54ea1-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="54ea1-104">La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » permet aux utilisateurs non administratifs d’utiliser une [boîte de dialogue Parcourir](browse-dialog.md) pour localiser les sources des [*applications gérées*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="54ea1-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="54ea1-105">Les sources peuvent inclure des médias, tels que des CD-ROM, des URL et des emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="54ea1-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="54ea1-106">Pour plus d’informations, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="54ea1-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="54ea1-107">La valeur par défaut sur Windows Installer est que les utilisateurs non administratifs ne peuvent pas rechercher de nouvelles sources d’applications gérées.</span><span class="sxs-lookup"><span data-stu-id="54ea1-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="54ea1-108">Les seules sources disponibles sont celles qui sont déjà inscrites dans la liste source du produit.</span><span class="sxs-lookup"><span data-stu-id="54ea1-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="54ea1-109">Si cette stratégie est définie, un utilisateur non administratif peut rechercher de nouvelles sources d’applications ou d’applications attribuées ou publiées en cours d’installation pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54ea1-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="54ea1-110">La définition de AllowLockdownBrowse permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="54ea1-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="54ea1-111">Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="54ea1-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="54ea1-112">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="54ea1-112">Registry Key</span></span>

<span data-ttu-id="54ea1-113">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="54ea1-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="54ea1-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="54ea1-114">Data Type</span></span>

<span data-ttu-id="54ea1-115">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="54ea1-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="54ea1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="54ea1-116">Remarks</span></span>

<span data-ttu-id="54ea1-117">La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package Windows Installer qui installe ou lance ces programmes.</span><span class="sxs-lookup"><span data-stu-id="54ea1-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="54ea1-118">[DisableBrowse](disablebrowse.md) remplace AllowLockdownBrowse et empêche la navigation même si AllowLockdownBrowse est défini.</span><span class="sxs-lookup"><span data-stu-id="54ea1-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="54ea1-119">Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="54ea1-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54ea1-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54ea1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ea1-121">Résilience source</span><span class="sxs-lookup"><span data-stu-id="54ea1-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="54ea1-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="54ea1-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



