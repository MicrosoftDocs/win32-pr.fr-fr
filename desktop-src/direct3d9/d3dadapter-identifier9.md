---
description: Contient des informations identifiant l’adaptateur.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Structure D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129968"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="15fa9-103">D3DADAPTER \_ IDENTIFIER9, structure</span><span class="sxs-lookup"><span data-stu-id="15fa9-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="15fa9-104">Contient des informations identifiant l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="15fa9-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fa9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15fa9-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="15fa9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="15fa9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15fa9-107">**Driver**</span><span class="sxs-lookup"><span data-stu-id="15fa9-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-108">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="15fa9-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-109">Utilisé pour la présentation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15fa9-109">Used for presentation to the user.</span></span> <span data-ttu-id="15fa9-110">Cela ne doit pas être utilisé pour identifier des pilotes particuliers, car de nombreuses chaînes différentes peuvent être associées au même appareil et au même pilote de différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="15fa9-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="15fa9-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-112">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="15fa9-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-113">Utilisé pour la présentation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15fa9-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="15fa9-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-115">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="15fa9-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-116">Nom de l’appareil pour GDI.</span><span class="sxs-lookup"><span data-stu-id="15fa9-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="15fa9-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-118">Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-119">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="15fa9-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="15fa9-120">Il est possible d’effectuer des comparaisons inférieur à et supérieur à sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="15fa9-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="15fa9-121">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="15fa9-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="15fa9-122">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="15fa9-123">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="15fa9-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="15fa9-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-126">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="15fa9-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="15fa9-127">Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="15fa9-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="15fa9-128">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="15fa9-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="15fa9-129">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="15fa9-130">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="15fa9-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="15fa9-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-133">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="15fa9-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="15fa9-134">Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="15fa9-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="15fa9-135">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="15fa9-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="15fa9-136">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="15fa9-137">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="15fa9-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="15fa9-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-139">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-140">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="15fa9-141">Interrogez ce membre pour identifier le fabricant.</span><span class="sxs-lookup"><span data-stu-id="15fa9-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="15fa9-142">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="15fa9-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="15fa9-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-144">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-145">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="15fa9-146">Interrogez ce membre pour identifier le type de processeur.</span><span class="sxs-lookup"><span data-stu-id="15fa9-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="15fa9-147">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="15fa9-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="15fa9-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-149">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-150">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="15fa9-151">Interrogez ce membre pour identifier le sous-système, généralement le tableau particulier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="15fa9-152">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="15fa9-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-153">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="15fa9-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-154">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-155">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="15fa9-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="15fa9-156">Interrogez ce membre pour identifier le niveau de révision du jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="15fa9-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="15fa9-157">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="15fa9-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="15fa9-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-159">Type : **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-160">Peut être interrogé pour vérifier les modifications apportées au pilote et au jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="15fa9-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="15fa9-161">Ce GUID est un identificateur unique pour le couple du pilote et du jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="15fa9-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="15fa9-162">Interrogez ce membre pour effectuer le suivi des modifications apportées au pilote et au jeu de processeurs afin de générer un nouveau profil pour le sous-système graphique.</span><span class="sxs-lookup"><span data-stu-id="15fa9-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="15fa9-163">DeviceIdentifier peut également être utilisé pour identifier des pilotes problématiques particuliers.</span><span class="sxs-lookup"><span data-stu-id="15fa9-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="15fa9-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="15fa9-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="15fa9-165">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fa9-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="15fa9-166">Utilisé pour déterminer le niveau de validation WHQL (Windows Hardware Quality Labs) pour ce pilote et cette paire d’appareils.</span><span class="sxs-lookup"><span data-stu-id="15fa9-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="15fa9-167">La valeur DWORD est une structure de date compressée qui définit la date de publication du test WHQL le plus récent passé par le pilote.</span><span class="sxs-lookup"><span data-stu-id="15fa9-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="15fa9-168">Il est légal d’effectuer des opérations de < et de > sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="15fa9-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="15fa9-169">L’exemple suivant illustre le format de date.</span><span class="sxs-lookup"><span data-stu-id="15fa9-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="15fa9-170">Bits</span><span class="sxs-lookup"><span data-stu-id="15fa9-170">Bits</span></span>  |  <span data-ttu-id="15fa9-171">Description</span><span class="sxs-lookup"><span data-stu-id="15fa9-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="15fa9-172">31-16</span><span class="sxs-lookup"><span data-stu-id="15fa9-172">31-16</span></span> | <span data-ttu-id="15fa9-173">Année, un nombre décimal compris entre 1999 et plus.</span><span class="sxs-lookup"><span data-stu-id="15fa9-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="15fa9-174">15-8</span><span class="sxs-lookup"><span data-stu-id="15fa9-174">15-8</span></span>  | <span data-ttu-id="15fa9-175">Le mois, un nombre décimal compris entre 1 et 12.</span><span class="sxs-lookup"><span data-stu-id="15fa9-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="15fa9-176">7-0</span><span class="sxs-lookup"><span data-stu-id="15fa9-176">7-0</span></span>   | <span data-ttu-id="15fa9-177">Le jour, un nombre décimal compris entre 1 et 31.</span><span class="sxs-lookup"><span data-stu-id="15fa9-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="15fa9-178">Les valeurs suivantes sont également utilisées.</span><span class="sxs-lookup"><span data-stu-id="15fa9-178">The following values are also used.</span></span>



| <span data-ttu-id="15fa9-179">Value</span><span class="sxs-lookup"><span data-stu-id="15fa9-179">Value</span></span>    |  <span data-ttu-id="15fa9-180">Description</span><span class="sxs-lookup"><span data-stu-id="15fa9-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="15fa9-181">0</span><span class="sxs-lookup"><span data-stu-id="15fa9-181">0</span></span>   | <span data-ttu-id="15fa9-182">Non certifié.</span><span class="sxs-lookup"><span data-stu-id="15fa9-182">Not certified.</span></span>                                        |
| <span data-ttu-id="15fa9-183">1</span><span class="sxs-lookup"><span data-stu-id="15fa9-183">1</span></span>   | <span data-ttu-id="15fa9-184">WHQL validée, mais aucune information de date n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="15fa9-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="15fa9-185">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="15fa9-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="15fa9-186">Pour les Direct3D9Ex s’exécutant sur Windows Vista, Windows Server 2008, Windows 7 et Windows Server 2008 R2 (ou plus le système d’exploitation actuel), [**IDirect3D9 :: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) retourne 1 pour le niveau WHQL sans vérifier l’état du pilote.</span><span class="sxs-lookup"><span data-stu-id="15fa9-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15fa9-187">Remarques</span><span class="sxs-lookup"><span data-stu-id="15fa9-187">Remarks</span></span>

<span data-ttu-id="15fa9-188">L’exemple de pseudo-code suivant illustre le format de version encodé dans les membres DriverVersion, DriverVersionLowPart et DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="15fa9-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="15fa9-189">Consultez le kit de développement Platform SDK pour plus d’informations sur la macro HIWORD, la macro LOWORD et la grande \_ structure d’entiers.</span><span class="sxs-lookup"><span data-stu-id="15fa9-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="15fa9-190">\_ \_ La chaîne d’identificateur de périphérique Max \_ est une constante avec la définition suivante.</span><span class="sxs-lookup"><span data-stu-id="15fa9-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="15fa9-191">Les membres ID de périphérique, DeviceId, SubSysId et Revision peuvent être utilisés en tandem pour identifier des jeux de puces particuliers.</span><span class="sxs-lookup"><span data-stu-id="15fa9-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="15fa9-192">Toutefois, utilisez ces membres avec précaution.</span><span class="sxs-lookup"><span data-stu-id="15fa9-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fa9-193">Spécifications</span><span class="sxs-lookup"><span data-stu-id="15fa9-193">Requirements</span></span>



| <span data-ttu-id="15fa9-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15fa9-194">Requirement</span></span> | <span data-ttu-id="15fa9-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="15fa9-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15fa9-196">En-tête</span><span class="sxs-lookup"><span data-stu-id="15fa9-196">Header</span></span><br/> | <dl> <span data-ttu-id="15fa9-197"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="15fa9-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fa9-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15fa9-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fa9-199">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="15fa9-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
