---
title: LSKeyPack, structure
description: Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la structure LSKeyPack
- Services Bureau à distance pointeur de structure LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942719"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="db380-105">LSKeyPack, structure</span><span class="sxs-lookup"><span data-stu-id="db380-105">LSKeyPack structure</span></span>

<span data-ttu-id="db380-106">Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.</span><span class="sxs-lookup"><span data-stu-id="db380-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="db380-107">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="db380-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="db380-108">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="db380-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="db380-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db380-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="db380-110">Membres</span><span class="sxs-lookup"><span data-stu-id="db380-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="db380-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="db380-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="db380-112">Version du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-113">**ucKeyPackType**</span><span class="sxs-lookup"><span data-stu-id="db380-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="db380-114">Type de jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-115">**szCompanyName**</span><span class="sxs-lookup"><span data-stu-id="db380-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="db380-116">Nom de la société qui a émis le jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-117">**szKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="db380-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="db380-118">ID du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-119">**szProductName**</span><span class="sxs-lookup"><span data-stu-id="db380-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="db380-120">Nom du produit auquel appartient ce module de clé.</span><span class="sxs-lookup"><span data-stu-id="db380-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="db380-121">**szProductId**</span><span class="sxs-lookup"><span data-stu-id="db380-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="db380-122">ID du produit auquel ce module de clé appartient.</span><span class="sxs-lookup"><span data-stu-id="db380-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="db380-123">**szProductDesc**</span><span class="sxs-lookup"><span data-stu-id="db380-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="db380-124">Description du produit auquel ce module de clé appartient.</span><span class="sxs-lookup"><span data-stu-id="db380-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="db380-125">**wMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="db380-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="db380-126">Version principale du produit auquel appartient ce module de clé.</span><span class="sxs-lookup"><span data-stu-id="db380-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="db380-127">**wMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="db380-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="db380-128">Version mineure du produit auquel appartient ce module de clé.</span><span class="sxs-lookup"><span data-stu-id="db380-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="db380-129">**dwPlatformType**</span><span class="sxs-lookup"><span data-stu-id="db380-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="db380-130">Type de plateforme.</span><span class="sxs-lookup"><span data-stu-id="db380-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="db380-131">**ucLicenseType**</span><span class="sxs-lookup"><span data-stu-id="db380-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="db380-132">Type de licences dans le jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="db380-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="db380-134">ID de langue.</span><span class="sxs-lookup"><span data-stu-id="db380-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="db380-135">**ucChannelOfPurchase**</span><span class="sxs-lookup"><span data-stu-id="db380-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="db380-136">Canal d’achat.</span><span class="sxs-lookup"><span data-stu-id="db380-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="db380-137">**szBeginSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="db380-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="db380-138">Numéro de série de la première licence.</span><span class="sxs-lookup"><span data-stu-id="db380-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="db380-139">**dwTotalLicenseInKeyPack**</span><span class="sxs-lookup"><span data-stu-id="db380-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="db380-140">Nombre total de licences dans le jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-141">**dwProductFlags**</span><span class="sxs-lookup"><span data-stu-id="db380-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="db380-142">Père.</span><span class="sxs-lookup"><span data-stu-id="db380-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="db380-143">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="db380-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="db380-144">ID du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-145">**ucKeyPackStatus**</span><span class="sxs-lookup"><span data-stu-id="db380-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="db380-146">État du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-147">**dwActivateDate**</span><span class="sxs-lookup"><span data-stu-id="db380-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="db380-148">Date d’activation du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-149">**dwExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="db380-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="db380-150">Date d’expiration du jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="db380-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="db380-151">**dwNumberOfLicenses**</span><span class="sxs-lookup"><span data-stu-id="db380-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="db380-152">Nombre de licences.</span><span class="sxs-lookup"><span data-stu-id="db380-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db380-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db380-153">Requirements</span></span>



| <span data-ttu-id="db380-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db380-154">Requirement</span></span> | <span data-ttu-id="db380-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="db380-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="db380-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db380-156">Minimum supported client</span></span><br/> | <span data-ttu-id="db380-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db380-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="db380-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db380-158">Minimum supported server</span></span><br/> | <span data-ttu-id="db380-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db380-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db380-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db380-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db380-161">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="db380-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="db380-162">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="db380-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="db380-163">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="db380-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





