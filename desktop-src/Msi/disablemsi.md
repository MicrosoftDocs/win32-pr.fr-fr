---
description: Si la valeur de cette stratégie système par ordinateur est définie sur &\# 0034 ; 2&\# 0034 ; le programme d’installation est toujours désactivé pour toutes les applications. Si cette valeur de stratégie est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation est désactivé pour les applications non gérées, mais il est toujours activé pour les applications managées.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034647"
---
# <a name="disablemsi"></a><span data-ttu-id="ff39b-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="ff39b-104">DisableMSI</span></span>

<span data-ttu-id="ff39b-105">Si la valeur de cette [stratégie système](system-policy.md) par ordinateur est définie sur « 2 », le programme d’installation est toujours désactivé pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="ff39b-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="ff39b-106">Si cette valeur de stratégie est définie sur « 1 », le programme d’installation est désactivé pour les applications non gérées, mais il est toujours activé pour les applications managées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="ff39b-107">Le tableau suivant répertorie les configurations possibles.</span><span class="sxs-lookup"><span data-stu-id="ff39b-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="ff39b-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="ff39b-108">DisableMSI</span></span> | <span data-ttu-id="ff39b-109">Description</span><span class="sxs-lookup"><span data-stu-id="ff39b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff39b-110">*Par défaut*</span><span class="sxs-lookup"><span data-stu-id="ff39b-110">*Default*</span></span>  | <span data-ttu-id="ff39b-111">Sur Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 et Windows Server 2008 R2, si la valeur de stratégie est null, absente ou un nombre autre que 1 ou 2, le Windows Installer est activé pour les applications managées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="ff39b-112">Les installations d’applications non gérées sont bloquées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="ff39b-113">Sur Windows XP, Windows Vista et Windows 7, le Windows Installer est activé pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="ff39b-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="ff39b-114">Toutes les opérations d’installation sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="ff39b-115">0</span><span class="sxs-lookup"><span data-stu-id="ff39b-115">0</span></span>          | <span data-ttu-id="ff39b-116">Windows Installer est activé pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="ff39b-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="ff39b-117">Toutes les opérations d’installation sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ff39b-118">1</span><span class="sxs-lookup"><span data-stu-id="ff39b-118">1</span></span>          | <span data-ttu-id="ff39b-119">La Windows Installer est désactivée pour les applications non managées, mais elle est toujours activée pour les applications managées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="ff39b-120">Les installations par utilisateur non élevées sont bloquées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="ff39b-121">Les installations par utilisateur avec élévation de privilèges et par ordinateur sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="ff39b-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="ff39b-122">2</span><span class="sxs-lookup"><span data-stu-id="ff39b-122">2</span></span>          | <span data-ttu-id="ff39b-123">Windows Installer est toujours désactivée pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="ff39b-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="ff39b-124">Aucune installation n’est autorisée, y compris les réparations, les réinstallations ou les installations à la demande.</span><span class="sxs-lookup"><span data-stu-id="ff39b-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="ff39b-125">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="ff39b-125">Registry Key</span></span>

<span data-ttu-id="ff39b-126">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="ff39b-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="ff39b-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="ff39b-127">Data Type</span></span>

<span data-ttu-id="ff39b-128">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="ff39b-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff39b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff39b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff39b-130">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ff39b-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




