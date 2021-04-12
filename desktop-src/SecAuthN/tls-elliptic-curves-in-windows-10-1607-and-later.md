---
description: Courbes elliptiques activées dans Windows 10 version 1607 et versions ultérieures.
title: Des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209697"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="c0018-103">Des courbes elliptiques TLS dans Windows 10 version 1607 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="c0018-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="c0018-104">Pour Windows 10, versions 1607 et ultérieures, les courbes elliptiques suivantes sont activées et, par défaut, dans cet ordre de priorité, utilisez le fournisseur Microsoft Schannel :</span><span class="sxs-lookup"><span data-stu-id="c0018-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="c0018-105">Chaîne de courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="c0018-105">Elliptic curve string</span></span> | <span data-ttu-id="c0018-106">Disponible en mode FIPS</span><span class="sxs-lookup"><span data-stu-id="c0018-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="c0018-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="c0018-107">curve25519</span></span> | <span data-ttu-id="c0018-108">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-108">No</span></span> |
| <span data-ttu-id="c0018-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="c0018-109">NistP256</span></span> | <span data-ttu-id="c0018-110">Oui</span><span class="sxs-lookup"><span data-stu-id="c0018-110">Yes</span></span> |
| <span data-ttu-id="c0018-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="c0018-111">NistP384</span></span> | <span data-ttu-id="c0018-112">Oui</span><span class="sxs-lookup"><span data-stu-id="c0018-112">Yes</span></span> |


<span data-ttu-id="c0018-113">Les courbes elliptiques suivantes sont prises en charge par le fournisseur Microsoft Schannel, mais ne sont pas activées par défaut :</span><span class="sxs-lookup"><span data-stu-id="c0018-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="c0018-114">Chaîne de courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="c0018-114">Elliptic curve string</span></span> | <span data-ttu-id="c0018-115">Disponible en mode FIPS</span><span class="sxs-lookup"><span data-stu-id="c0018-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="c0018-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="c0018-116">brainpoolP256r1</span></span> | <span data-ttu-id="c0018-117">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-117">No</span></span> |
| <span data-ttu-id="c0018-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="c0018-118">brainpoolP384r1</span></span> | <span data-ttu-id="c0018-119">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-119">No</span></span> |
| <span data-ttu-id="c0018-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="c0018-120">brainpoolP512r1</span></span> | <span data-ttu-id="c0018-121">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-121">No</span></span> |
| <span data-ttu-id="c0018-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="c0018-122">nistP192</span></span> | <span data-ttu-id="c0018-123">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-123">No</span></span> |
| <span data-ttu-id="c0018-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="c0018-124">nistP224</span></span> | <span data-ttu-id="c0018-125">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-125">No</span></span> |
| <span data-ttu-id="c0018-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="c0018-126">nistP521</span></span> | <span data-ttu-id="c0018-127">Oui</span><span class="sxs-lookup"><span data-stu-id="c0018-127">Yes</span></span> |
| <span data-ttu-id="c0018-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="c0018-128">secP160k1</span></span> | <span data-ttu-id="c0018-129">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-129">No</span></span> |
| <span data-ttu-id="c0018-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="c0018-130">secP160r1</span></span> | <span data-ttu-id="c0018-131">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-131">No</span></span> |
| <span data-ttu-id="c0018-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="c0018-132">secP160r2</span></span> | <span data-ttu-id="c0018-133">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-133">No</span></span> |
| <span data-ttu-id="c0018-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="c0018-134">secP192k1</span></span> | <span data-ttu-id="c0018-135">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-135">No</span></span> |
| <span data-ttu-id="c0018-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="c0018-136">secP192r1</span></span> | <span data-ttu-id="c0018-137">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-137">No</span></span> |
| <span data-ttu-id="c0018-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="c0018-138">secP224k1</span></span> | <span data-ttu-id="c0018-139">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-139">No</span></span> |
| <span data-ttu-id="c0018-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="c0018-140">secP224r1</span></span> | <span data-ttu-id="c0018-141">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-141">No</span></span> |
| <span data-ttu-id="c0018-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="c0018-142">secP256k1</span></span> | <span data-ttu-id="c0018-143">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-143">No</span></span> |
| <span data-ttu-id="c0018-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="c0018-144">secP256r1</span></span> | <span data-ttu-id="c0018-145">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-145">No</span></span> |
| <span data-ttu-id="c0018-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="c0018-146">secP384r1</span></span> | <span data-ttu-id="c0018-147">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-147">No</span></span> |
| <span data-ttu-id="c0018-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="c0018-148">secP521r1</span></span> | <span data-ttu-id="c0018-149">Non</span><span class="sxs-lookup"><span data-stu-id="c0018-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="c0018-150">Activation des courbes elliptiques</span><span class="sxs-lookup"><span data-stu-id="c0018-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="c0018-151">Pour ajouter des courbes elliptiques, vous pouvez soit déployer une stratégie de groupe, soit utiliser les applets de commande TLS :</span><span class="sxs-lookup"><span data-stu-id="c0018-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="c0018-152">Pour utiliser la stratégie de groupe, [configurez l’ordre des courbes ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) sous Configuration ordinateur > modèles d’administration > les paramètres de configuration réseau > SSL avec la liste priorité pour toutes les courbes elliptiques que vous souhaitez activer.</span><span class="sxs-lookup"><span data-stu-id="c0018-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="c0018-153">Pour utiliser PowerShell, consultez [applets](/powershell/module/tls) de commande TLS pour obtenir une liste complète de la syntaxe et des descriptions de l’applet de commande TLS.</span><span class="sxs-lookup"><span data-stu-id="c0018-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="c0018-154">Avant Windows 10, les chaînes de suite de chiffrement étaient ajoutées à la courbe elliptique pour déterminer la priorité de la courbe.</span><span class="sxs-lookup"><span data-stu-id="c0018-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="c0018-155">Windows 10 prend en charge un paramètre d’ordre de priorité de courbe elliptique, ce qui signifie que le suffixe de courbe elliptique n’est pas obligatoire et est remplacé par le nouvel ordre de priorité de la courbe elliptique, le cas échéant, pour permettre aux organisations d’utiliser la stratégie de groupe pour configurer différentes versions de Windows avec les mêmes suites de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c0018-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="c0018-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0018-156">See Also</span></span>

[<span data-ttu-id="c0018-157">Configuration de l’ordre des courbes ECC TLS</span><span class="sxs-lookup"><span data-stu-id="c0018-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="c0018-158">Gestion de l’ordre ECC TLS</span><span class="sxs-lookup"><span data-stu-id="c0018-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="c0018-159">Gestion des courbes ECC Windows à l’aide de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c0018-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="c0018-160">Applets de commande TLS</span><span class="sxs-lookup"><span data-stu-id="c0018-160">TLS cmdlets</span></span>](/powershell/module/tls)
