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
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529602"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="350de-103">D3DADAPTER \_ IDENTIFIER9, structure</span><span class="sxs-lookup"><span data-stu-id="350de-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="350de-104">Contient des informations identifiant l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="350de-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="350de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="350de-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="350de-106">Membres</span><span class="sxs-lookup"><span data-stu-id="350de-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="350de-107">**Driver**</span><span class="sxs-lookup"><span data-stu-id="350de-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="350de-108">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="350de-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="350de-109">Utilisé pour la présentation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="350de-109">Used for presentation to the user.</span></span> <span data-ttu-id="350de-110">Cela ne doit pas être utilisé pour identifier des pilotes particuliers, car de nombreuses chaînes différentes peuvent être associées au même appareil et au même pilote de différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="350de-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="350de-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="350de-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="350de-112">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="350de-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="350de-113">Utilisé pour la présentation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="350de-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="350de-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="350de-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="350de-115">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="350de-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="350de-116">Nom de l’appareil pour GDI.</span><span class="sxs-lookup"><span data-stu-id="350de-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="350de-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="350de-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="350de-118">Type : **[ **\_ entier long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="350de-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-119">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="350de-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="350de-120">Il est possible d’effectuer des comparaisons inférieur à et supérieur à sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="350de-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="350de-121">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="350de-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="350de-122">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="350de-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="350de-123">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="350de-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="350de-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="350de-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="350de-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-126">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="350de-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="350de-127">Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="350de-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="350de-128">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="350de-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="350de-129">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="350de-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="350de-130">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="350de-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="350de-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="350de-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="350de-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-133">Identifiez la version du pilote Direct3D.</span><span class="sxs-lookup"><span data-stu-id="350de-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="350de-134">Il est possible d’effectuer des comparaisons < et > sur la valeur de l’entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="350de-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="350de-135">Toutefois, soyez prudent si vous utilisez cet élément pour identifier les pilotes problématiques.</span><span class="sxs-lookup"><span data-stu-id="350de-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="350de-136">Au lieu de cela, vous devez utiliser DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="350de-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="350de-137">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="350de-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="350de-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="350de-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="350de-139">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-140">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="350de-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="350de-141">Interrogez ce membre pour identifier le fabricant.</span><span class="sxs-lookup"><span data-stu-id="350de-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="350de-142">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="350de-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="350de-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="350de-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="350de-144">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-145">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="350de-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="350de-146">Interrogez ce membre pour identifier le type de processeur.</span><span class="sxs-lookup"><span data-stu-id="350de-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="350de-147">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="350de-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="350de-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="350de-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="350de-149">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-150">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="350de-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="350de-151">Interrogez ce membre pour identifier le sous-système, généralement le tableau particulier.</span><span class="sxs-lookup"><span data-stu-id="350de-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="350de-152">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="350de-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="350de-153">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="350de-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="350de-154">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-155">Peut être utilisé pour aider à identifier un jeu de processeurs particulier.</span><span class="sxs-lookup"><span data-stu-id="350de-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="350de-156">Interrogez ce membre pour identifier le niveau de révision du jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="350de-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="350de-157">La valeur peut être zéro si inconnu.</span><span class="sxs-lookup"><span data-stu-id="350de-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="350de-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="350de-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="350de-159">Type : **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-160">Peut être interrogé pour vérifier les modifications apportées au pilote et au jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="350de-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="350de-161">Ce GUID est un identificateur unique pour le couple du pilote et du jeu de processeurs.</span><span class="sxs-lookup"><span data-stu-id="350de-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="350de-162">Interrogez ce membre pour effectuer le suivi des modifications apportées au pilote et au jeu de processeurs afin de générer un nouveau profil pour le sous-système graphique.</span><span class="sxs-lookup"><span data-stu-id="350de-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="350de-163">DeviceIdentifier peut également être utilisé pour identifier des pilotes problématiques particuliers.</span><span class="sxs-lookup"><span data-stu-id="350de-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="350de-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="350de-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="350de-165">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="350de-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="350de-166">Utilisé pour déterminer le niveau de validation WHQL (Windows Hardware Quality Labs) pour ce pilote et cette paire d’appareils.</span><span class="sxs-lookup"><span data-stu-id="350de-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="350de-167">La valeur DWORD est une structure de date compressée qui définit la date de publication du test WHQL le plus récent passé par le pilote.</span><span class="sxs-lookup"><span data-stu-id="350de-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="350de-168">Il est légal d’effectuer des opérations de < et de > sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="350de-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="350de-169">L’exemple suivant illustre le format de date.</span><span class="sxs-lookup"><span data-stu-id="350de-169">The following illustrates the date format.</span></span>



|       |                                               |
|-------|-----------------------------------------------|
| <span data-ttu-id="350de-170">Bits</span><span class="sxs-lookup"><span data-stu-id="350de-170">Bits</span></span>  |                                               |
| <span data-ttu-id="350de-171">31-16</span><span class="sxs-lookup"><span data-stu-id="350de-171">31-16</span></span> | <span data-ttu-id="350de-172">Année, un nombre décimal compris entre 1999 et plus.</span><span class="sxs-lookup"><span data-stu-id="350de-172">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="350de-173">15-8</span><span class="sxs-lookup"><span data-stu-id="350de-173">15-8</span></span>  | <span data-ttu-id="350de-174">Le mois, un nombre décimal compris entre 1 et 12.</span><span class="sxs-lookup"><span data-stu-id="350de-174">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="350de-175">7-0</span><span class="sxs-lookup"><span data-stu-id="350de-175">7-0</span></span>   | <span data-ttu-id="350de-176">Le jour, un nombre décimal compris entre 1 et 31.</span><span class="sxs-lookup"><span data-stu-id="350de-176">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="350de-177">Les valeurs suivantes sont également utilisées.</span><span class="sxs-lookup"><span data-stu-id="350de-177">The following values are also used.</span></span>



|     |                                                       |
|-----|-------------------------------------------------------|
| <span data-ttu-id="350de-178">0</span><span class="sxs-lookup"><span data-stu-id="350de-178">0</span></span>   | <span data-ttu-id="350de-179">Non certifié.</span><span class="sxs-lookup"><span data-stu-id="350de-179">Not certified.</span></span>                                        |
| <span data-ttu-id="350de-180">1</span><span class="sxs-lookup"><span data-stu-id="350de-180">1</span></span>   | <span data-ttu-id="350de-181">WHQL validée, mais aucune information de date n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="350de-181">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="350de-182">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="350de-182">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="350de-183">Pour les Direct3D9Ex s’exécutant sur Windows Vista, Windows Server 2008, Windows 7 et Windows Server 2008 R2 (ou plus le système d’exploitation actuel), [**IDirect3D9 :: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) retourne 1 pour le niveau WHQL sans vérifier l’état du pilote.</span><span class="sxs-lookup"><span data-stu-id="350de-183">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="350de-184">Notes</span><span class="sxs-lookup"><span data-stu-id="350de-184">Remarks</span></span>

<span data-ttu-id="350de-185">L’exemple de pseudo-code suivant illustre le format de version encodé dans les membres DriverVersion, DriverVersionLowPart et DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="350de-185">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="350de-186">Consultez le kit de développement Platform SDK pour plus d’informations sur la macro HIWORD, la macro LOWORD et la grande \_ structure d’entiers.</span><span class="sxs-lookup"><span data-stu-id="350de-186">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="350de-187">\_ \_ La chaîne d’identificateur de périphérique Max \_ est une constante avec la définition suivante.</span><span class="sxs-lookup"><span data-stu-id="350de-187">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="350de-188">Les membres ID de périphérique, DeviceId, SubSysId et Revision peuvent être utilisés en tandem pour identifier des jeux de puces particuliers.</span><span class="sxs-lookup"><span data-stu-id="350de-188">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="350de-189">Toutefois, utilisez ces membres avec précaution.</span><span class="sxs-lookup"><span data-stu-id="350de-189">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="350de-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="350de-190">Requirements</span></span>



| <span data-ttu-id="350de-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="350de-191">Requirement</span></span> | <span data-ttu-id="350de-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="350de-192">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="350de-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="350de-193">Header</span></span><br/> | <dl> <span data-ttu-id="350de-194"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="350de-194"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="350de-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="350de-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="350de-196">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="350de-196">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
