---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ; empêche les utilisateurs non administratifs d’utiliser une boîte de dialogue Parcourir pour localiser les sources des applications gérées stockées sur le support, telles que les CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516615"
---
# <a name="disablebrowse"></a><span data-ttu-id="277d0-103">DisableBrowse</span><span class="sxs-lookup"><span data-stu-id="277d0-103">DisableBrowse</span></span>

<span data-ttu-id="277d0-104">La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » empêche les utilisateurs non administratifs d’utiliser une [boîte de dialogue Parcourir](browse-dialog.md) pour localiser les sources des [*applications gérées*](m-gly.md) stockées sur le média, telles que les CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="277d0-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="277d0-105">La zone de liste déroulante « utiliser la fonctionnalité à partir de » pour l’entrée directe est verrouillée et l’option « Parcourir... » le bouton est désactivé.</span><span class="sxs-lookup"><span data-stu-id="277d0-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="277d0-106">Pour plus d’informations sur la navigation source, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="277d0-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="277d0-107">DisableBrowse remplace AllowLockdownBrowse et empêche la navigation même si AllowLockdownBrowse est défini.</span><span class="sxs-lookup"><span data-stu-id="277d0-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="277d0-108">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="277d0-108">Registry Key</span></span>

<span data-ttu-id="277d0-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="277d0-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="277d0-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="277d0-110">Data Type</span></span>

<span data-ttu-id="277d0-111">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="277d0-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="277d0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="277d0-112">Remarks</span></span>

<span data-ttu-id="277d0-113">Dans certains cas, avec DisableBrowse défini, un utilisateur non administratif peut toujours être en charge d’installer des applications gérées à partir de sources sur un support correctement étiqueté.</span><span class="sxs-lookup"><span data-stu-id="277d0-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="277d0-114">La définition de la stratégie DisableBrowse désactive uniquement la possibilité d’accéder aux sources.</span><span class="sxs-lookup"><span data-stu-id="277d0-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="277d0-115">Il peut être utilisé pour empêcher un utilisateur non administratif d’accéder à une nouvelle source lors d’une installation, d’une réinstallation ou d’une réparation à la demande.</span><span class="sxs-lookup"><span data-stu-id="277d0-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="277d0-116">Si [AllowLockdownMedia](allowlockdownmedia.md) est défini, l’utilisateur non administratif peut toujours installer une application gérée à partir d’un média correctement étiqueté.</span><span class="sxs-lookup"><span data-stu-id="277d0-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="277d0-117">DisableBrowse empêche l’utilisateur non administratif d’accéder à un nouvel emplacement de support ou à tout autre emplacement source.</span><span class="sxs-lookup"><span data-stu-id="277d0-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="277d0-118">Pour plus d’informations sur la sécurisation des sources multimédias des applications gérées, consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="277d0-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="277d0-119">Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="277d0-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



