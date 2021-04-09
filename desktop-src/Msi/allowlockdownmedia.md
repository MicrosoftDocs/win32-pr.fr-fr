---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ;, permet aux utilisateurs non administratifs d’installer des applications gérées à partir de sources stockées sur des supports, comme un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869605"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="a810d-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="a810d-103">AllowLockdownMedia</span></span>

<span data-ttu-id="a810d-104">La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » permet aux utilisateurs non administratifs d’installer des [*applications gérées*](m-gly.md) à partir de sources stockées sur un support, par exemple un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="a810d-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="a810d-105">Consultez [résilience source](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="a810d-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="a810d-106">Par exemple, si cette stratégie est définie, un utilisateur non administratif peut utiliser une source de média pour installer des applications ou des applications attribuées ou publiées en cours d’installation pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a810d-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="a810d-107">La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="a810d-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="a810d-108">La valeur par défaut de cette stratégie est 1 uniquement sur les ordinateurs exécutant Windows Vista et qui ne sont pas joints à un domaine.</span><span class="sxs-lookup"><span data-stu-id="a810d-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="a810d-109">Par défaut sur les autres ordinateurs, les utilisateurs non-administrateurs ne peuvent pas installer des applications gérées à partir d’une source située sur un support.</span><span class="sxs-lookup"><span data-stu-id="a810d-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="a810d-110">Étant donné que cette stratégie permet aux utilisateurs qui ne sont pas administrateurs d’installer avec des privilèges qu’ils n’ont pas par défaut, avant de définir cette stratégie, vous devez déterminer si elle fournit un niveau de sécurité approprié à votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a810d-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="a810d-111">Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="a810d-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="a810d-112">Pour plus d’informations sur la sécurisation des installations et l’utilisation des certificats numériques, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) et [téléchargement d’une installation à partir d’Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="a810d-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="a810d-113">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="a810d-113">Registry Key</span></span>

<span data-ttu-id="a810d-114">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="a810d-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a810d-115">Type de données</span><span class="sxs-lookup"><span data-stu-id="a810d-115">Data Type</span></span>

<span data-ttu-id="a810d-116">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="a810d-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a810d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a810d-117">Remarks</span></span>

<span data-ttu-id="a810d-118">La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package Windows Installer qui installe ou lance ces programmes.</span><span class="sxs-lookup"><span data-stu-id="a810d-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a810d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a810d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a810d-120">Résilience source</span><span class="sxs-lookup"><span data-stu-id="a810d-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="a810d-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="a810d-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



