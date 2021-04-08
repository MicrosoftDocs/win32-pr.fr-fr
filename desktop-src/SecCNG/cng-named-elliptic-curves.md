---
description: À compter de Windows 10, CNG prend en charge les courbes elliptiques nommées suivantes (ANSI X 9.62, X 9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Courbes elliptiques nommées CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861973"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="800d0-103">CNG nommé courbes elliptique</span><span class="sxs-lookup"><span data-stu-id="800d0-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="800d0-104">À compter de Windows 10, CNG prend en charge les courbes elliptiques nommées suivantes (ANSI X 9.62, X 9.63, FIPS 186-2).</span><span class="sxs-lookup"><span data-stu-id="800d0-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="800d0-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ Curve \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-106">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-106">Requirement</span></span> | <span data-ttu-id="800d0-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="800d0-108">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-108">Name</span></span>              | <span data-ttu-id="800d0-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="800d0-109">curve25519</span></span>                                                  |
| <span data-ttu-id="800d0-110">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-110">Standard</span></span>          | [<span data-ttu-id="800d0-111">Courbe 25519</span><span class="sxs-lookup"><span data-stu-id="800d0-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="800d0-112">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-112">Key size (bits)</span></span>   | <span data-ttu-id="800d0-113">255</span><span class="sxs-lookup"><span data-stu-id="800d0-113">255</span></span>                                                         |
| <span data-ttu-id="800d0-114">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="800d0-115">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-115">Object identifier</span></span> | <span data-ttu-id="800d0-116">Aucun</span><span class="sxs-lookup"><span data-stu-id="800d0-116">None</span></span>                                                        |



 

<span data-ttu-id="800d0-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-118">Requirement</span></span> | <span data-ttu-id="800d0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-120">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-120">Name</span></span>              | <span data-ttu-id="800d0-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="800d0-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-122">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-122">Standard</span></span>          | [<span data-ttu-id="800d0-123">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-124">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-124">Key size (bits)</span></span>   | <span data-ttu-id="800d0-125">160</span><span class="sxs-lookup"><span data-stu-id="800d0-125">160</span></span>                                                                                                               |
| <span data-ttu-id="800d0-126">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-126">TLS capable</span></span>       | <span data-ttu-id="800d0-127">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-127">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-128">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-128">Object identifier</span></span> | <span data-ttu-id="800d0-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="800d0-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="800d0-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP160T1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-131">Requirement</span></span> | <span data-ttu-id="800d0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-133">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-133">Name</span></span>              | <span data-ttu-id="800d0-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="800d0-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-135">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-135">Standard</span></span>          | [<span data-ttu-id="800d0-136">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-137">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-137">Key size (bits)</span></span>   | <span data-ttu-id="800d0-138">160</span><span class="sxs-lookup"><span data-stu-id="800d0-138">160</span></span>                                                                                                               |
| <span data-ttu-id="800d0-139">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-139">TLS capable</span></span>       | <span data-ttu-id="800d0-140">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-140">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-141">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-141">Object identifier</span></span> | <span data-ttu-id="800d0-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="800d0-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="800d0-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-144">Requirement</span></span> | <span data-ttu-id="800d0-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-146">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-146">Name</span></span>              | <span data-ttu-id="800d0-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="800d0-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-148">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-148">Standard</span></span>          | [<span data-ttu-id="800d0-149">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-150">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-150">Key size (bits)</span></span>   | <span data-ttu-id="800d0-151">192</span><span class="sxs-lookup"><span data-stu-id="800d0-151">192</span></span>                                                                                                               |
| <span data-ttu-id="800d0-152">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-152">TLS capable</span></span>       | <span data-ttu-id="800d0-153">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-153">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-154">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-154">Object identifier</span></span> | <span data-ttu-id="800d0-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="800d0-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="800d0-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP192T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-157">Requirement</span></span> | <span data-ttu-id="800d0-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-159">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-159">Name</span></span>              | <span data-ttu-id="800d0-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="800d0-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-161">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-161">Standard</span></span>          | [<span data-ttu-id="800d0-162">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-163">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-163">Key size (bits)</span></span>   | <span data-ttu-id="800d0-164">192</span><span class="sxs-lookup"><span data-stu-id="800d0-164">192</span></span>                                                                                                               |
| <span data-ttu-id="800d0-165">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-165">TLS capable</span></span>       | <span data-ttu-id="800d0-166">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-166">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-167">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-167">Object identifier</span></span> | <span data-ttu-id="800d0-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="800d0-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="800d0-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-170">Requirement</span></span> | <span data-ttu-id="800d0-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-172">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-172">Name</span></span>              | <span data-ttu-id="800d0-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="800d0-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-174">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-174">Standard</span></span>          | [<span data-ttu-id="800d0-175">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-176">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-176">Key size (bits)</span></span>   | <span data-ttu-id="800d0-177">224</span><span class="sxs-lookup"><span data-stu-id="800d0-177">224</span></span>                                                                                                               |
| <span data-ttu-id="800d0-178">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-178">TLS capable</span></span>       | <span data-ttu-id="800d0-179">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-179">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-180">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-180">Object identifier</span></span> | <span data-ttu-id="800d0-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="800d0-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="800d0-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP224T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-183">Requirement</span></span> | <span data-ttu-id="800d0-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-185">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-185">Name</span></span>              | <span data-ttu-id="800d0-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="800d0-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-187">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-187">Standard</span></span>          | [<span data-ttu-id="800d0-188">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-189">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-189">Key size (bits)</span></span>   | <span data-ttu-id="800d0-190">224</span><span class="sxs-lookup"><span data-stu-id="800d0-190">224</span></span>                                                                                                               |
| <span data-ttu-id="800d0-191">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-191">TLS capable</span></span>       | <span data-ttu-id="800d0-192">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-192">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-193">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-193">Object identifier</span></span> | <span data-ttu-id="800d0-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="800d0-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="800d0-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-196">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-196">Requirement</span></span> | <span data-ttu-id="800d0-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-198">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-198">Name</span></span>              | <span data-ttu-id="800d0-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="800d0-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-200">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-200">Standard</span></span>          | [<span data-ttu-id="800d0-201">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-202">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-202">Key size (bits)</span></span>   | <span data-ttu-id="800d0-203">256</span><span class="sxs-lookup"><span data-stu-id="800d0-203">256</span></span>                                                                                                               |
| <span data-ttu-id="800d0-204">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-204">TLS capable</span></span>       | <span data-ttu-id="800d0-205">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="800d0-206">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-206">Object identifier</span></span> | <span data-ttu-id="800d0-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="800d0-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="800d0-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-209">Requirement</span></span> | <span data-ttu-id="800d0-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-211">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-211">Name</span></span>              | <span data-ttu-id="800d0-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="800d0-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-213">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-213">Standard</span></span>          | [<span data-ttu-id="800d0-214">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-215">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-215">Key size (bits)</span></span>   | <span data-ttu-id="800d0-216">256</span><span class="sxs-lookup"><span data-stu-id="800d0-216">256</span></span>                                                                                                               |
| <span data-ttu-id="800d0-217">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-217">TLS capable</span></span>       | <span data-ttu-id="800d0-218">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-218">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-219">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-219">Object identifier</span></span> | <span data-ttu-id="800d0-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="800d0-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="800d0-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP320R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-222">Requirement</span></span> | <span data-ttu-id="800d0-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-224">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-224">Name</span></span>              | <span data-ttu-id="800d0-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="800d0-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-226">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-226">Standard</span></span>          | [<span data-ttu-id="800d0-227">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-228">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-228">Key size (bits)</span></span>   | <span data-ttu-id="800d0-229">320</span><span class="sxs-lookup"><span data-stu-id="800d0-229">320</span></span>                                                                                                               |
| <span data-ttu-id="800d0-230">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-230">TLS capable</span></span>       | <span data-ttu-id="800d0-231">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-231">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-232">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-232">Object identifier</span></span> | <span data-ttu-id="800d0-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="800d0-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="800d0-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-235">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-235">Requirement</span></span> | <span data-ttu-id="800d0-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-237">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-237">Name</span></span>              | <span data-ttu-id="800d0-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="800d0-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-239">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-239">Standard</span></span>          | [<span data-ttu-id="800d0-240">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-241">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-241">Key size (bits)</span></span>   | <span data-ttu-id="800d0-242">320</span><span class="sxs-lookup"><span data-stu-id="800d0-242">320</span></span>                                                                                                               |
| <span data-ttu-id="800d0-243">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-243">TLS capable</span></span>       | <span data-ttu-id="800d0-244">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-244">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-245">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-245">Object identifier</span></span> | <span data-ttu-id="800d0-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="800d0-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="800d0-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ \_ \_ BRAINPOOLP384R1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-248">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-248">Requirement</span></span> | <span data-ttu-id="800d0-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-250">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-250">Name</span></span>              | <span data-ttu-id="800d0-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="800d0-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-252">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-252">Standard</span></span>          | [<span data-ttu-id="800d0-253">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-254">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-254">Key size (bits)</span></span>   | <span data-ttu-id="800d0-255">384</span><span class="sxs-lookup"><span data-stu-id="800d0-255">384</span></span>                                                                                                               |
| <span data-ttu-id="800d0-256">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-256">TLS capable</span></span>       | <span data-ttu-id="800d0-257">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="800d0-258">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-258">Object identifier</span></span> | <span data-ttu-id="800d0-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="800d0-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="800d0-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-261">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-261">Requirement</span></span> | <span data-ttu-id="800d0-262">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-263">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-263">Name</span></span>              | <span data-ttu-id="800d0-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="800d0-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-265">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-265">Standard</span></span>          | [<span data-ttu-id="800d0-266">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-267">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-267">Key size (bits)</span></span>   | <span data-ttu-id="800d0-268">384</span><span class="sxs-lookup"><span data-stu-id="800d0-268">384</span></span>                                                                                                               |
| <span data-ttu-id="800d0-269">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-269">TLS capable</span></span>       | <span data-ttu-id="800d0-270">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-270">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-271">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-271">Object identifier</span></span> | <span data-ttu-id="800d0-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="800d0-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="800d0-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP512R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-274">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-274">Requirement</span></span> | <span data-ttu-id="800d0-275">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-276">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-276">Name</span></span>              | <span data-ttu-id="800d0-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="800d0-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-278">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-278">Standard</span></span>          | [<span data-ttu-id="800d0-279">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-280">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-280">Key size (bits)</span></span>   | <span data-ttu-id="800d0-281">512</span><span class="sxs-lookup"><span data-stu-id="800d0-281">512</span></span>                                                                                                               |
| <span data-ttu-id="800d0-282">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-282">TLS capable</span></span>       | <span data-ttu-id="800d0-283">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="800d0-284">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-284">Object identifier</span></span> | <span data-ttu-id="800d0-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="800d0-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="800d0-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ Curve \_ BRAINPOOLP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-287">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-287">Requirement</span></span> | <span data-ttu-id="800d0-288">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-289">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-289">Name</span></span>              | <span data-ttu-id="800d0-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="800d0-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="800d0-291">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-291">Standard</span></span>          | [<span data-ttu-id="800d0-292">Les courbes et la génération de courbe ECC Brainpool standard</span><span class="sxs-lookup"><span data-stu-id="800d0-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="800d0-293">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-293">Key size (bits)</span></span>   | <span data-ttu-id="800d0-294">512</span><span class="sxs-lookup"><span data-stu-id="800d0-294">512</span></span>                                                                                                               |
| <span data-ttu-id="800d0-295">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-295">TLS capable</span></span>       | <span data-ttu-id="800d0-296">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-296">No</span></span>                                                                                                                |
| <span data-ttu-id="800d0-297">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-297">Object identifier</span></span> | <span data-ttu-id="800d0-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="800d0-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="800d0-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ \_ \_ EC192WAPI de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-300">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-300">Requirement</span></span> | <span data-ttu-id="800d0-301">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="800d0-302">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-302">Name</span></span>              | <span data-ttu-id="800d0-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="800d0-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="800d0-304">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-304">Standard</span></span>          | <span data-ttu-id="800d0-305">Chinois national standard pour les réseaux locaux sans fil (Go 15629.11-2003)</span><span class="sxs-lookup"><span data-stu-id="800d0-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="800d0-306">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-306">Key size (bits)</span></span>   | <span data-ttu-id="800d0-307">192</span><span class="sxs-lookup"><span data-stu-id="800d0-307">192</span></span>                                                            |
| <span data-ttu-id="800d0-308">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-308">TLS capable</span></span>       | <span data-ttu-id="800d0-309">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-309">No</span></span>                                                             |
| <span data-ttu-id="800d0-310">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-310">Object identifier</span></span> | <span data-ttu-id="800d0-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="800d0-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="800d0-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP192**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-313">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-313">Requirement</span></span> | <span data-ttu-id="800d0-314">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-315">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-315">Name</span></span>              | <span data-ttu-id="800d0-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="800d0-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="800d0-317">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-317">Standard</span></span>          | [<span data-ttu-id="800d0-318">Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral</span><span class="sxs-lookup"><span data-stu-id="800d0-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="800d0-319">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-319">Key size (bits)</span></span>   | <span data-ttu-id="800d0-320">192</span><span class="sxs-lookup"><span data-stu-id="800d0-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-321">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-321">TLS capable</span></span>       | <span data-ttu-id="800d0-322">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-323">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-323">Object identifier</span></span> | <span data-ttu-id="800d0-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="800d0-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="800d0-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-326">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-326">Requirement</span></span> | <span data-ttu-id="800d0-327">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-328">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-328">Name</span></span>              | <span data-ttu-id="800d0-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="800d0-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="800d0-330">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-330">Standard</span></span>          | [<span data-ttu-id="800d0-331">Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral</span><span class="sxs-lookup"><span data-stu-id="800d0-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="800d0-332">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-332">Key size (bits)</span></span>   | <span data-ttu-id="800d0-333">224</span><span class="sxs-lookup"><span data-stu-id="800d0-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-334">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-334">TLS capable</span></span>       | <span data-ttu-id="800d0-335">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-336">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-336">Object identifier</span></span> | <span data-ttu-id="800d0-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="800d0-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="800d0-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP256**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-339">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-339">Requirement</span></span> | <span data-ttu-id="800d0-340">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-341">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-341">Name</span></span>              | <span data-ttu-id="800d0-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="800d0-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="800d0-343">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-343">Standard</span></span>          | [<span data-ttu-id="800d0-344">Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral</span><span class="sxs-lookup"><span data-stu-id="800d0-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="800d0-345">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-345">Key size (bits)</span></span>   | <span data-ttu-id="800d0-346">256</span><span class="sxs-lookup"><span data-stu-id="800d0-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-347">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-347">TLS capable</span></span>       | <span data-ttu-id="800d0-348">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-349">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-349">Object identifier</span></span> | <span data-ttu-id="800d0-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="800d0-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="800d0-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-352">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-352">Requirement</span></span> | <span data-ttu-id="800d0-353">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-354">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-354">Name</span></span>              | <span data-ttu-id="800d0-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="800d0-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="800d0-356">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-356">Standard</span></span>          | [<span data-ttu-id="800d0-357">Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral</span><span class="sxs-lookup"><span data-stu-id="800d0-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="800d0-358">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-358">Key size (bits)</span></span>   | <span data-ttu-id="800d0-359">384</span><span class="sxs-lookup"><span data-stu-id="800d0-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-360">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-360">TLS capable</span></span>       | <span data-ttu-id="800d0-361">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-362">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-362">Object identifier</span></span> | <span data-ttu-id="800d0-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="800d0-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="800d0-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ Curve \_ NISTP521**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-365">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-365">Requirement</span></span> | <span data-ttu-id="800d0-366">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-367">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-367">Name</span></span>              | <span data-ttu-id="800d0-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="800d0-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="800d0-369">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-369">Standard</span></span>          | [<span data-ttu-id="800d0-370">Courbes elliptiques recommandées pour l’utilisation du gouvernement fédéral</span><span class="sxs-lookup"><span data-stu-id="800d0-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="800d0-371">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-371">Key size (bits)</span></span>   | <span data-ttu-id="800d0-372">521</span><span class="sxs-lookup"><span data-stu-id="800d0-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-373">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-373">TLS capable</span></span>       | <span data-ttu-id="800d0-374">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="800d0-375">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-375">Object identifier</span></span> | <span data-ttu-id="800d0-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="800d0-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="800d0-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-378">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-378">Requirement</span></span> | <span data-ttu-id="800d0-379">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-380">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-380">Name</span></span>              | <span data-ttu-id="800d0-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="800d0-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="800d0-382">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-382">Standard</span></span>          | [<span data-ttu-id="800d0-383">Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="800d0-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="800d0-384">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-384">Key size (bits)</span></span>   | <span data-ttu-id="800d0-385">256</span><span class="sxs-lookup"><span data-stu-id="800d0-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="800d0-386">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-386">TLS capable</span></span>       | <span data-ttu-id="800d0-387">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="800d0-388">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-388">Object identifier</span></span> | <span data-ttu-id="800d0-389">Aucun</span><span class="sxs-lookup"><span data-stu-id="800d0-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="800d0-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-391">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-391">Requirement</span></span> | <span data-ttu-id="800d0-392">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-393">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-393">Name</span></span>              | <span data-ttu-id="800d0-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="800d0-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="800d0-395">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-395">Standard</span></span>          | [<span data-ttu-id="800d0-396">Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="800d0-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="800d0-397">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-397">Key size (bits)</span></span>   | <span data-ttu-id="800d0-398">384</span><span class="sxs-lookup"><span data-stu-id="800d0-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="800d0-399">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-399">TLS capable</span></span>       | <span data-ttu-id="800d0-400">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="800d0-401">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-401">Object identifier</span></span> | <span data-ttu-id="800d0-402">Aucun</span><span class="sxs-lookup"><span data-stu-id="800d0-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="800d0-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ Curve \_ NUMSP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-404">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-404">Requirement</span></span> | <span data-ttu-id="800d0-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-406">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-406">Name</span></span>              | <span data-ttu-id="800d0-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="800d0-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="800d0-408">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-408">Standard</span></span>          | [<span data-ttu-id="800d0-409">Spécification de la sélection des courbes et des paramètres de courbe pris en charge dans MSR ECCLib</span><span class="sxs-lookup"><span data-stu-id="800d0-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="800d0-410">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-410">Key size (bits)</span></span>   | <span data-ttu-id="800d0-411">512</span><span class="sxs-lookup"><span data-stu-id="800d0-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="800d0-412">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-412">TLS capable</span></span>       | <span data-ttu-id="800d0-413">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="800d0-414">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-414">Object identifier</span></span> | <span data-ttu-id="800d0-415">Aucun</span><span class="sxs-lookup"><span data-stu-id="800d0-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="800d0-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-417">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-417">Requirement</span></span> | <span data-ttu-id="800d0-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-419">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-419">Name</span></span>              | <span data-ttu-id="800d0-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="800d0-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="800d0-421">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-421">Standard</span></span>          | [<span data-ttu-id="800d0-422">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-423">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-423">Key size (bits)</span></span>   | <span data-ttu-id="800d0-424">160</span><span class="sxs-lookup"><span data-stu-id="800d0-424">160</span></span>                                                                             |
| <span data-ttu-id="800d0-425">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-425">TLS capable</span></span>       | <span data-ttu-id="800d0-426">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-426">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-427">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-427">Object identifier</span></span> | <span data-ttu-id="800d0-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="800d0-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="800d0-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-430">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-430">Requirement</span></span> | <span data-ttu-id="800d0-431">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-432">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-432">Name</span></span>              | <span data-ttu-id="800d0-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="800d0-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="800d0-434">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-434">Standard</span></span>          | [<span data-ttu-id="800d0-435">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-436">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-436">Key size (bits)</span></span>   | <span data-ttu-id="800d0-437">160</span><span class="sxs-lookup"><span data-stu-id="800d0-437">160</span></span>                                                                             |
| <span data-ttu-id="800d0-438">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-438">TLS capable</span></span>       | <span data-ttu-id="800d0-439">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-439">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-440">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-440">Object identifier</span></span> | <span data-ttu-id="800d0-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="800d0-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="800d0-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-443">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-443">Requirement</span></span> | <span data-ttu-id="800d0-444">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-445">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-445">Name</span></span>              | <span data-ttu-id="800d0-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="800d0-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="800d0-447">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-447">Standard</span></span>          | [<span data-ttu-id="800d0-448">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-449">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-449">Key size (bits)</span></span>   | <span data-ttu-id="800d0-450">160</span><span class="sxs-lookup"><span data-stu-id="800d0-450">160</span></span>                                                                             |
| <span data-ttu-id="800d0-451">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-451">TLS capable</span></span>       | <span data-ttu-id="800d0-452">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-452">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-453">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-453">Object identifier</span></span> | <span data-ttu-id="800d0-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="800d0-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="800d0-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP192K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-456">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-456">Requirement</span></span> | <span data-ttu-id="800d0-457">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-458">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-458">Name</span></span>              | <span data-ttu-id="800d0-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="800d0-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="800d0-460">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-460">Standard</span></span>          | [<span data-ttu-id="800d0-461">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-462">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-462">Key size (bits)</span></span>   | <span data-ttu-id="800d0-463">192</span><span class="sxs-lookup"><span data-stu-id="800d0-463">192</span></span>                                                                             |
| <span data-ttu-id="800d0-464">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-464">TLS capable</span></span>       | <span data-ttu-id="800d0-465">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-465">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-466">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-466">Object identifier</span></span> | <span data-ttu-id="800d0-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="800d0-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="800d0-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-469">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-469">Requirement</span></span> | <span data-ttu-id="800d0-470">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-471">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-471">Name</span></span>              | <span data-ttu-id="800d0-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="800d0-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="800d0-473">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-473">Standard</span></span>          | [<span data-ttu-id="800d0-474">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-475">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-475">Key size (bits)</span></span>   | <span data-ttu-id="800d0-476">192</span><span class="sxs-lookup"><span data-stu-id="800d0-476">192</span></span>                                                                             |
| <span data-ttu-id="800d0-477">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-477">TLS capable</span></span>       | <span data-ttu-id="800d0-478">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-478">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-479">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-479">Object identifier</span></span> | <span data-ttu-id="800d0-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="800d0-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="800d0-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP224K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-482">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-482">Requirement</span></span> | <span data-ttu-id="800d0-483">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-484">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-484">Name</span></span>              | <span data-ttu-id="800d0-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="800d0-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="800d0-486">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-486">Standard</span></span>          | [<span data-ttu-id="800d0-487">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-488">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-488">Key size (bits)</span></span>   | <span data-ttu-id="800d0-489">224</span><span class="sxs-lookup"><span data-stu-id="800d0-489">224</span></span>                                                                             |
| <span data-ttu-id="800d0-490">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-490">TLS capable</span></span>       | <span data-ttu-id="800d0-491">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-491">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-492">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-492">Object identifier</span></span> | <span data-ttu-id="800d0-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="800d0-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="800d0-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-495">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-495">Requirement</span></span> | <span data-ttu-id="800d0-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-497">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-497">Name</span></span>              | <span data-ttu-id="800d0-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="800d0-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="800d0-499">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-499">Standard</span></span>          | [<span data-ttu-id="800d0-500">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-501">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-501">Key size (bits)</span></span>   | <span data-ttu-id="800d0-502">224</span><span class="sxs-lookup"><span data-stu-id="800d0-502">224</span></span>                                                                             |
| <span data-ttu-id="800d0-503">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-503">TLS capable</span></span>       | <span data-ttu-id="800d0-504">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-504">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-505">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-505">Object identifier</span></span> | <span data-ttu-id="800d0-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="800d0-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="800d0-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP256K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-508">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-508">Requirement</span></span> | <span data-ttu-id="800d0-509">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-510">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-510">Name</span></span>              | <span data-ttu-id="800d0-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="800d0-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="800d0-512">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-512">Standard</span></span>          | [<span data-ttu-id="800d0-513">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-514">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-514">Key size (bits)</span></span>   | <span data-ttu-id="800d0-515">256</span><span class="sxs-lookup"><span data-stu-id="800d0-515">256</span></span>                                                                             |
| <span data-ttu-id="800d0-516">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-516">TLS capable</span></span>       | <span data-ttu-id="800d0-517">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-517">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-518">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-518">Object identifier</span></span> | <span data-ttu-id="800d0-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="800d0-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="800d0-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-521">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-521">Requirement</span></span> | <span data-ttu-id="800d0-522">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-523">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-523">Name</span></span>              | <span data-ttu-id="800d0-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="800d0-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="800d0-525">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-525">Standard</span></span>          | [<span data-ttu-id="800d0-526">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-527">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-527">Key size (bits)</span></span>   | <span data-ttu-id="800d0-528">256</span><span class="sxs-lookup"><span data-stu-id="800d0-528">256</span></span>                                                                             |
| <span data-ttu-id="800d0-529">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-529">TLS capable</span></span>       | <span data-ttu-id="800d0-530">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-530">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-531">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-531">Object identifier</span></span> | <span data-ttu-id="800d0-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="800d0-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="800d0-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-534">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-534">Requirement</span></span> | <span data-ttu-id="800d0-535">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-536">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-536">Name</span></span>              | <span data-ttu-id="800d0-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="800d0-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="800d0-538">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-538">Standard</span></span>          | [<span data-ttu-id="800d0-539">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-540">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-540">Key size (bits)</span></span>   | <span data-ttu-id="800d0-541">384</span><span class="sxs-lookup"><span data-stu-id="800d0-541">384</span></span>                                                                             |
| <span data-ttu-id="800d0-542">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-542">TLS capable</span></span>       | <span data-ttu-id="800d0-543">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-543">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-544">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-544">Object identifier</span></span> | <span data-ttu-id="800d0-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="800d0-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="800d0-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ Curve \_ SECP521R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-547">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-547">Requirement</span></span> | <span data-ttu-id="800d0-548">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-549">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-549">Name</span></span>              | <span data-ttu-id="800d0-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="800d0-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="800d0-551">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-551">Standard</span></span>          | [<span data-ttu-id="800d0-552">Paramètres de domaine de courbe elliptique recommandés</span><span class="sxs-lookup"><span data-stu-id="800d0-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="800d0-553">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-553">Key size (bits)</span></span>   | <span data-ttu-id="800d0-554">521</span><span class="sxs-lookup"><span data-stu-id="800d0-554">521</span></span>                                                                             |
| <span data-ttu-id="800d0-555">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-555">TLS capable</span></span>       | <span data-ttu-id="800d0-556">Oui</span><span class="sxs-lookup"><span data-stu-id="800d0-556">Yes</span></span>                                                                             |
| <span data-ttu-id="800d0-557">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-557">Object identifier</span></span> | <span data-ttu-id="800d0-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="800d0-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="800d0-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ Curve \_ WTLS12**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-560">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-560">Requirement</span></span> | <span data-ttu-id="800d0-561">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="800d0-562">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-562">Name</span></span>              | <span data-ttu-id="800d0-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="800d0-563">wtls12</span></span>       |
| <span data-ttu-id="800d0-564">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-564">Standard</span></span>          | <span data-ttu-id="800d0-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="800d0-565">WTLS</span></span>         |
| <span data-ttu-id="800d0-566">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-566">Key size (bits)</span></span>   | <span data-ttu-id="800d0-567">224</span><span class="sxs-lookup"><span data-stu-id="800d0-567">224</span></span>          |
| <span data-ttu-id="800d0-568">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-568">TLS capable</span></span>       | <span data-ttu-id="800d0-569">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-569">No</span></span>           |
| <span data-ttu-id="800d0-570">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-570">Object identifier</span></span> | <span data-ttu-id="800d0-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="800d0-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="800d0-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ Curve \_ WTLS7**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-573">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-573">Requirement</span></span> | <span data-ttu-id="800d0-574">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="800d0-575">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-575">Name</span></span>              | <span data-ttu-id="800d0-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="800d0-576">wtls7</span></span>        |
| <span data-ttu-id="800d0-577">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-577">Standard</span></span>          | <span data-ttu-id="800d0-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="800d0-578">WTLS</span></span>         |
| <span data-ttu-id="800d0-579">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-579">Key size (bits)</span></span>   | <span data-ttu-id="800d0-580">160</span><span class="sxs-lookup"><span data-stu-id="800d0-580">160</span></span>          |
| <span data-ttu-id="800d0-581">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-581">TLS capable</span></span>       | <span data-ttu-id="800d0-582">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-582">No</span></span>           |
| <span data-ttu-id="800d0-583">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-583">Object identifier</span></span> | <span data-ttu-id="800d0-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="800d0-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="800d0-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-586">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-586">Requirement</span></span> | <span data-ttu-id="800d0-587">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="800d0-588">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-588">Name</span></span>              | <span data-ttu-id="800d0-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="800d0-589">wtls9</span></span>         |
| <span data-ttu-id="800d0-590">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-590">Standard</span></span>          | <span data-ttu-id="800d0-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="800d0-591">WTLS</span></span>          |
| <span data-ttu-id="800d0-592">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-592">Key size (bits)</span></span>   | <span data-ttu-id="800d0-593">160</span><span class="sxs-lookup"><span data-stu-id="800d0-593">160</span></span>           |
| <span data-ttu-id="800d0-594">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-594">TLS capable</span></span>       | <span data-ttu-id="800d0-595">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-595">No</span></span>            |
| <span data-ttu-id="800d0-596">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-596">Object identifier</span></span> | <span data-ttu-id="800d0-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="800d0-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="800d0-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ Curve \_ X962P192V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-599">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-599">Requirement</span></span> | <span data-ttu-id="800d0-600">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-601">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-601">Name</span></span>              | <span data-ttu-id="800d0-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="800d0-602">x962P192v1</span></span>          |
| <span data-ttu-id="800d0-603">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-603">Standard</span></span>          | <span data-ttu-id="800d0-604">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-605">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-605">Key size (bits)</span></span>   | <span data-ttu-id="800d0-606">192</span><span class="sxs-lookup"><span data-stu-id="800d0-606">192</span></span>                 |
| <span data-ttu-id="800d0-607">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-607">TLS capable</span></span>       | <span data-ttu-id="800d0-608">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-608">No</span></span>                  |
| <span data-ttu-id="800d0-609">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-609">Object identifier</span></span> | <span data-ttu-id="800d0-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="800d0-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="800d0-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ \_ \_ X962P192V2 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-612">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-612">Requirement</span></span> | <span data-ttu-id="800d0-613">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-614">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-614">Name</span></span>              | <span data-ttu-id="800d0-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="800d0-615">x962P192v2</span></span>          |
| <span data-ttu-id="800d0-616">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-616">Standard</span></span>          | <span data-ttu-id="800d0-617">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-618">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-618">Key size (bits)</span></span>   | <span data-ttu-id="800d0-619">192</span><span class="sxs-lookup"><span data-stu-id="800d0-619">192</span></span>                 |
| <span data-ttu-id="800d0-620">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-620">TLS capable</span></span>       | <span data-ttu-id="800d0-621">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-621">No</span></span>                  |
| <span data-ttu-id="800d0-622">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-622">Object identifier</span></span> | <span data-ttu-id="800d0-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="800d0-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="800d0-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ Curve \_ X962P192V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-625">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-625">Requirement</span></span> | <span data-ttu-id="800d0-626">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-627">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-627">Name</span></span>              | <span data-ttu-id="800d0-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="800d0-628">x962P192v3</span></span>          |
| <span data-ttu-id="800d0-629">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-629">Standard</span></span>          | <span data-ttu-id="800d0-630">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-631">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-631">Key size (bits)</span></span>   | <span data-ttu-id="800d0-632">192</span><span class="sxs-lookup"><span data-stu-id="800d0-632">192</span></span>                 |
| <span data-ttu-id="800d0-633">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-633">TLS capable</span></span>       | <span data-ttu-id="800d0-634">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-634">No</span></span>                  |
| <span data-ttu-id="800d0-635">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-635">Object identifier</span></span> | <span data-ttu-id="800d0-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="800d0-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="800d0-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ \_ \_ X962P239V1 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-638">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-638">Requirement</span></span> | <span data-ttu-id="800d0-639">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-640">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-640">Name</span></span>              | <span data-ttu-id="800d0-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="800d0-641">x962P239v1</span></span>          |
| <span data-ttu-id="800d0-642">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-642">Standard</span></span>          | <span data-ttu-id="800d0-643">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-644">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-644">Key size (bits)</span></span>   | <span data-ttu-id="800d0-645">239</span><span class="sxs-lookup"><span data-stu-id="800d0-645">239</span></span>                 |
| <span data-ttu-id="800d0-646">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-646">TLS capable</span></span>       | <span data-ttu-id="800d0-647">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-647">No</span></span>                  |
| <span data-ttu-id="800d0-648">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-648">Object identifier</span></span> | <span data-ttu-id="800d0-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="800d0-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="800d0-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ \_ \_ X962P239V2 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-651">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-651">Requirement</span></span> | <span data-ttu-id="800d0-652">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-653">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-653">Name</span></span>              | <span data-ttu-id="800d0-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="800d0-654">x962P239v2</span></span>          |
| <span data-ttu-id="800d0-655">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-655">Standard</span></span>          | <span data-ttu-id="800d0-656">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-657">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-657">Key size (bits)</span></span>   | <span data-ttu-id="800d0-658">239</span><span class="sxs-lookup"><span data-stu-id="800d0-658">239</span></span>                 |
| <span data-ttu-id="800d0-659">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-659">TLS capable</span></span>       | <span data-ttu-id="800d0-660">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-660">No</span></span>                  |
| <span data-ttu-id="800d0-661">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-661">Object identifier</span></span> | <span data-ttu-id="800d0-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="800d0-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="800d0-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ \_ \_ X962P239V3 de courbe ECC**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-664">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-664">Requirement</span></span> | <span data-ttu-id="800d0-665">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-666">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-666">Name</span></span>              | <span data-ttu-id="800d0-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="800d0-667">x962P239v3</span></span>          |
| <span data-ttu-id="800d0-668">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-668">Standard</span></span>          | <span data-ttu-id="800d0-669">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-670">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-670">Key size (bits)</span></span>   | <span data-ttu-id="800d0-671">239</span><span class="sxs-lookup"><span data-stu-id="800d0-671">239</span></span>                 |
| <span data-ttu-id="800d0-672">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-672">TLS capable</span></span>       | <span data-ttu-id="800d0-673">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-673">No</span></span>                  |
| <span data-ttu-id="800d0-674">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-674">Object identifier</span></span> | <span data-ttu-id="800d0-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="800d0-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="800d0-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ Curve \_ X962P256V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="800d0-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="800d0-677">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-677">Requirement</span></span> | <span data-ttu-id="800d0-678">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="800d0-679">Nom</span><span class="sxs-lookup"><span data-stu-id="800d0-679">Name</span></span>              | <span data-ttu-id="800d0-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="800d0-680">x962P256v1</span></span>          |
| <span data-ttu-id="800d0-681">standard</span><span class="sxs-lookup"><span data-stu-id="800d0-681">Standard</span></span>          | <span data-ttu-id="800d0-682">ANSI X 9.62</span><span class="sxs-lookup"><span data-stu-id="800d0-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="800d0-683">Taille de la clé (bits)</span><span class="sxs-lookup"><span data-stu-id="800d0-683">Key size (bits)</span></span>   | <span data-ttu-id="800d0-684">256</span><span class="sxs-lookup"><span data-stu-id="800d0-684">256</span></span>                 |
| <span data-ttu-id="800d0-685">Compatibilité TLS</span><span class="sxs-lookup"><span data-stu-id="800d0-685">TLS capable</span></span>       | <span data-ttu-id="800d0-686">Non</span><span class="sxs-lookup"><span data-stu-id="800d0-686">No</span></span>                  |
| <span data-ttu-id="800d0-687">Identificateur d'objet</span><span class="sxs-lookup"><span data-stu-id="800d0-687">Object identifier</span></span> | <span data-ttu-id="800d0-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="800d0-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="800d0-689">Notes</span><span class="sxs-lookup"><span data-stu-id="800d0-689">Remarks</span></span>

<span data-ttu-id="800d0-690">Pour utiliser une courbe nommée, appelez [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) à l’aide de l' **\_ \_ algorithme ECDSA bcrypt** ou de l' **\_ \_ algorithme ECDH bcrypt** comme ID d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="800d0-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="800d0-691">Ensuite, appelez [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) et définissez la propriété de nom de la **\_ \_ courbe \_ de BCRYPT** à l’aide de l’une des courbes ci-dessus ou de toute courbe nommée inscrite sur l’ordinateur comme indiqué par la `certutil -displayEccCurve` commande.</span><span class="sxs-lookup"><span data-stu-id="800d0-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="800d0-692">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="800d0-692">Requirements</span></span>



| <span data-ttu-id="800d0-693">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800d0-693">Requirement</span></span> | <span data-ttu-id="800d0-694">Valeur</span><span class="sxs-lookup"><span data-stu-id="800d0-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="800d0-695">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="800d0-695">Minimum supported client</span></span><br/> | <span data-ttu-id="800d0-696">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="800d0-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="800d0-697">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="800d0-697">Minimum supported server</span></span><br/> | <span data-ttu-id="800d0-698">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="800d0-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="800d0-699">En-tête</span><span class="sxs-lookup"><span data-stu-id="800d0-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="800d0-700"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="800d0-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800d0-701">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="800d0-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800d0-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="800d0-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="800d0-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="800d0-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




