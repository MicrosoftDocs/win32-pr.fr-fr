---
description: Courbes elliptiques activées dans Windows 10 versions 1507 et 1511.
title: Courbes elliptiques TLS dans Windows 10 version 1507 et 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520090"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="729f0-103">Courbes elliptiques TLS dans Windows 10 version 1507 et 1511</span><span class="sxs-lookup"><span data-stu-id="729f0-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="729f0-104">Pour Windows 10, versions 1507 et 1511, les courbes elliptiques suivantes sont activées et, par défaut, dans cet ordre de priorité, utilisez le fournisseur Microsoft Schannel :</span><span class="sxs-lookup"><span data-stu-id="729f0-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="729f0-105">Chaîne de courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="729f0-105">Elliptic curve string</span></span> | <span data-ttu-id="729f0-106">Disponible en mode FIPS</span><span class="sxs-lookup"><span data-stu-id="729f0-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="729f0-107">NistP256</span><span class="sxs-lookup"><span data-stu-id="729f0-107">NistP256</span></span> | <span data-ttu-id="729f0-108">Oui</span><span class="sxs-lookup"><span data-stu-id="729f0-108">Yes</span></span> |
| <span data-ttu-id="729f0-109">NistP384</span><span class="sxs-lookup"><span data-stu-id="729f0-109">NistP384</span></span> | <span data-ttu-id="729f0-110">Oui</span><span class="sxs-lookup"><span data-stu-id="729f0-110">Yes</span></span> |


<span data-ttu-id="729f0-111">Les courbes elliptiques suivantes sont prises en charge par le fournisseur Microsoft Schannel, mais ne sont pas activées par défaut :</span><span class="sxs-lookup"><span data-stu-id="729f0-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="729f0-112">Chaîne de courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="729f0-112">Elliptic curve string</span></span> | <span data-ttu-id="729f0-113">Disponible en mode FIPS</span><span class="sxs-lookup"><span data-stu-id="729f0-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="729f0-114">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="729f0-114">brainpoolP256r1</span></span> | <span data-ttu-id="729f0-115">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-115">No</span></span> |
| <span data-ttu-id="729f0-116">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="729f0-116">brainpoolP384r1</span></span> | <span data-ttu-id="729f0-117">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-117">No</span></span> |
| <span data-ttu-id="729f0-118">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="729f0-118">brainpoolP512r1</span></span> | <span data-ttu-id="729f0-119">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-119">No</span></span> |
| <span data-ttu-id="729f0-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="729f0-120">nistP192</span></span> | <span data-ttu-id="729f0-121">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-121">No</span></span> |
| <span data-ttu-id="729f0-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="729f0-122">nistP224</span></span> | <span data-ttu-id="729f0-123">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-123">No</span></span> |
| <span data-ttu-id="729f0-124">nistP521</span><span class="sxs-lookup"><span data-stu-id="729f0-124">nistP521</span></span> | <span data-ttu-id="729f0-125">Oui</span><span class="sxs-lookup"><span data-stu-id="729f0-125">Yes</span></span> |
| <span data-ttu-id="729f0-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="729f0-126">secP160k1</span></span> | <span data-ttu-id="729f0-127">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-127">No</span></span> |
| <span data-ttu-id="729f0-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="729f0-128">secP160r1</span></span> | <span data-ttu-id="729f0-129">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-129">No</span></span> |
| <span data-ttu-id="729f0-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="729f0-130">secP160r2</span></span> | <span data-ttu-id="729f0-131">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-131">No</span></span> |
| <span data-ttu-id="729f0-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="729f0-132">secP192k1</span></span> | <span data-ttu-id="729f0-133">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-133">No</span></span> |
| <span data-ttu-id="729f0-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="729f0-134">secP192r1</span></span> | <span data-ttu-id="729f0-135">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-135">No</span></span> |
| <span data-ttu-id="729f0-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="729f0-136">secP224k1</span></span> | <span data-ttu-id="729f0-137">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-137">No</span></span> |
| <span data-ttu-id="729f0-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="729f0-138">secP224r1</span></span> | <span data-ttu-id="729f0-139">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-139">No</span></span> |
| <span data-ttu-id="729f0-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="729f0-140">secP256k1</span></span> | <span data-ttu-id="729f0-141">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-141">No</span></span> |
| <span data-ttu-id="729f0-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="729f0-142">secP256r1</span></span> | <span data-ttu-id="729f0-143">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-143">No</span></span> |
| <span data-ttu-id="729f0-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="729f0-144">secP384r1</span></span> | <span data-ttu-id="729f0-145">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-145">No</span></span> |
| <span data-ttu-id="729f0-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="729f0-146">secP521r1</span></span> | <span data-ttu-id="729f0-147">Non</span><span class="sxs-lookup"><span data-stu-id="729f0-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="729f0-148">Activation des courbes elliptiques</span><span class="sxs-lookup"><span data-stu-id="729f0-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="729f0-149">Pour ajouter des courbes elliptiques, vous pouvez soit déployer une stratégie de groupe, soit utiliser les applets de commande TLS :</span><span class="sxs-lookup"><span data-stu-id="729f0-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="729f0-150">Pour utiliser la stratégie de groupe, [configurez l’ordre des courbes ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) sous Configuration ordinateur > modèles d’administration > les paramètres de configuration réseau > SSL avec la liste priorité pour toutes les courbes elliptiques que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="729f0-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="729f0-151">Pour utiliser PowerShell, consultez [applets](/powershell/module/tls) de commande TLS pour obtenir une liste complète de la syntaxe et des descriptions de l’applet de commande TLS.</span><span class="sxs-lookup"><span data-stu-id="729f0-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="729f0-152">Avant Windows 10, les chaînes de suite de chiffrement étaient ajoutées à la courbe elliptique pour déterminer la priorité de la courbe.</span><span class="sxs-lookup"><span data-stu-id="729f0-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="729f0-153">Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, ce qui signifie que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="729f0-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="729f0-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="729f0-154">See Also</span></span>

[<span data-ttu-id="729f0-155">Configuration de l’ordre des courbes ECC TLS</span><span class="sxs-lookup"><span data-stu-id="729f0-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="729f0-156">Gestion de l’ordre ECC TLS</span><span class="sxs-lookup"><span data-stu-id="729f0-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="729f0-157">Gestion des courbes ECC Windows à l’aide de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="729f0-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="729f0-158">Applets de commande TLS</span><span class="sxs-lookup"><span data-stu-id="729f0-158">TLS cmdlets</span></span>](/powershell/module/tls)
