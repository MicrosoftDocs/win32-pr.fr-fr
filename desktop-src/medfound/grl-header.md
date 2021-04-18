---
description: Contient l’en-tête GRL (liste de révocation globale).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Structure GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515949"
---
# <a name="grl_header-structure"></a><span data-ttu-id="932f0-103">\_Structure d’en-tête GRL</span><span class="sxs-lookup"><span data-stu-id="932f0-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="932f0-104">Contient l’en-tête GRL (liste de révocation globale).</span><span class="sxs-lookup"><span data-stu-id="932f0-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="932f0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="932f0-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="932f0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="932f0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="932f0-107">**wszIdentifier**</span><span class="sxs-lookup"><span data-stu-id="932f0-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-108">Identificateur GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-108">The GRL identifier.</span></span> <span data-ttu-id="932f0-109">La valeur est toujours L "MSGRL".</span><span class="sxs-lookup"><span data-stu-id="932f0-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="932f0-110">**wFormatMajor**</span><span class="sxs-lookup"><span data-stu-id="932f0-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-111">Numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="932f0-111">The major version number.</span></span> <span data-ttu-id="932f0-112">Actuellement, la valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="932f0-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-113">**wFormatMinor**</span><span class="sxs-lookup"><span data-stu-id="932f0-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-114">Numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="932f0-114">The minor version number.</span></span> <span data-ttu-id="932f0-115">Actuellement, la valeur doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="932f0-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="932f0-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-117">Valeur **fileTime** qui spécifie le moment où le fichier a été créé.</span><span class="sxs-lookup"><span data-stu-id="932f0-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-118">**dwSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="932f0-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-119">Numéro de version de GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-119">The GRL version number.</span></span> <span data-ttu-id="932f0-120">Actuellement, la valeur doit être au moins égale à 3</span><span class="sxs-lookup"><span data-stu-id="932f0-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="932f0-121">**dwForceRebootVersion**</span><span class="sxs-lookup"><span data-stu-id="932f0-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="932f0-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-123">**dwForceProcessRestartVersion**</span><span class="sxs-lookup"><span data-stu-id="932f0-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-124">Réservé.</span><span class="sxs-lookup"><span data-stu-id="932f0-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-125">**cbRevocationSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="932f0-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-126">Offset, en octets, entre le début de GRL et la section principale.</span><span class="sxs-lookup"><span data-stu-id="932f0-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-127">**cRevokedKernelBinaries**</span><span class="sxs-lookup"><span data-stu-id="932f0-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-128">Nombre de binaires de noyau révoqués listés dans GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-129">**cRevokedUserBinaries**</span><span class="sxs-lookup"><span data-stu-id="932f0-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-130">Nombre de fichiers binaires en mode utilisateur révoqués listés dans GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-131">**cRevokedCertificates**</span><span class="sxs-lookup"><span data-stu-id="932f0-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-132">Nombre de certificats révoqués listés dans GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-133">**cTrustedRoots**</span><span class="sxs-lookup"><span data-stu-id="932f0-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-134">Nombre de racines de confiance listées dans GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-135">**cbExtensibleSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="932f0-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-136">Offset, en octets, entre le début de GRL et la section extensible.</span><span class="sxs-lookup"><span data-stu-id="932f0-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-137">**cExtensibleEntries**</span><span class="sxs-lookup"><span data-stu-id="932f0-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-138">Nombre d’entrées dans la section extensible.</span><span class="sxs-lookup"><span data-stu-id="932f0-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-139">**cbRenewalSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="932f0-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-140">Décalage, en octets, entre le début de GRL et la section renouvellements.</span><span class="sxs-lookup"><span data-stu-id="932f0-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-141">**cRevokedKernelBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="932f0-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-142">Nombre de renouvellements binaires de noyau listés dans le GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-143">**cRevokedUserBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="932f0-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-144">Nombre de renouvellements binaires en mode utilisateur listés dans le GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-145">**cRevokedCertificateRenewals**</span><span class="sxs-lookup"><span data-stu-id="932f0-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-146">Nombre de renouvellements de certificats listés dans le GRL.</span><span class="sxs-lookup"><span data-stu-id="932f0-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-147">**cbSignatureCoreOffset**</span><span class="sxs-lookup"><span data-stu-id="932f0-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-148">Offset, en octets, entre le début de GRL et la signature de la section principale.</span><span class="sxs-lookup"><span data-stu-id="932f0-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="932f0-149">**cbSignatureExtOffset**</span><span class="sxs-lookup"><span data-stu-id="932f0-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="932f0-150">Offset, en octets, entre le début de GRL et la signature de la section extensible.</span><span class="sxs-lookup"><span data-stu-id="932f0-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="932f0-151">Notes</span><span class="sxs-lookup"><span data-stu-id="932f0-151">Remarks</span></span>

<span data-ttu-id="932f0-152">Tous les entiers dans GRL ont un classement des octets little-endian.</span><span class="sxs-lookup"><span data-stu-id="932f0-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="932f0-153">Toutes les structures sont alignées sur des limites de 1 octet.</span><span class="sxs-lookup"><span data-stu-id="932f0-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="932f0-154">Cette structure n’est pas déclarée dans un en-tête SDK.</span><span class="sxs-lookup"><span data-stu-id="932f0-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="932f0-155">Pour utiliser cette structure, ajoutez la déclaration indiquée ici à votre code source.</span><span class="sxs-lookup"><span data-stu-id="932f0-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="932f0-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="932f0-156">Requirements</span></span>



| <span data-ttu-id="932f0-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="932f0-157">Requirement</span></span> | <span data-ttu-id="932f0-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="932f0-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="932f0-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="932f0-159">Minimum supported client</span></span><br/> | <span data-ttu-id="932f0-160">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="932f0-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="932f0-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="932f0-161">Minimum supported server</span></span><br/> | <span data-ttu-id="932f0-162">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="932f0-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="932f0-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="932f0-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932f0-164">Révocation de certificat OPM</span><span class="sxs-lookup"><span data-stu-id="932f0-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="932f0-165">Structures OPM</span><span class="sxs-lookup"><span data-stu-id="932f0-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




