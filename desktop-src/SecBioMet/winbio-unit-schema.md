---
title: Structure WINBIO_UNIT_SCHEMA ( \_ types WINBIO. h)
description: Décrit les fonctionnalités d’une unité biométrique.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- API de Windows Biometric Framework de structure de WINBIO_UNIT_SCHEMA
- API du pointeur de structure PWINBIO_UNIT_SCHEMA Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942815"
---
# <a name="winbio_unit_schema-structure"></a><span data-ttu-id="887bb-105">Structure de schéma d' \_ unité WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-105">WINBIO\_UNIT\_SCHEMA structure</span></span>

<span data-ttu-id="887bb-106">La structure de **\_ \_ schéma d’unité WINBIO** décrit les fonctionnalités d’une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-106">The **WINBIO\_UNIT\_SCHEMA** structure describes the capabilities of a biometric unit.</span></span> <span data-ttu-id="887bb-107">Elle est utilisée par la fonction [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) .</span><span class="sxs-lookup"><span data-stu-id="887bb-107">It is used by the [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="887bb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="887bb-108">Syntax</span></span>


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="887bb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="887bb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="887bb-110">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="887bb-110">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-111">Valeur qui identifie l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-111">A value that identifies the biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-112">**PoolType**</span><span class="sxs-lookup"><span data-stu-id="887bb-112">**PoolType**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-113">Valeur **ULong** qui spécifie le type de l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-113">A **ULONG** value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="887bb-114">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="887bb-114">This can be one of the following values:</span></span>



| <span data-ttu-id="887bb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="887bb-115">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="887bb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="887bb-116">Meaning</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="887bb-117"><dt>**\_pool WINBIO \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="887bb-117"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="887bb-118">Le type est inconnu.</span><span class="sxs-lookup"><span data-stu-id="887bb-118">The type is unknown.</span></span><br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="887bb-119"><dt>**\_système de pool WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="887bb-119"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>    | <span data-ttu-id="887bb-120">La session se connecte à une collection partagée d’unités biométriques gérée par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="887bb-120">The session connects to a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="887bb-121"><dt>**\_pool WINBIO \_ privé**</dt></span><span class="sxs-lookup"><span data-stu-id="887bb-121"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="887bb-122">La session se connecte à une collection d’unités biométriques gérées par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="887bb-122">The session connects to a collection of biometric units that are managed by the caller.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="887bb-123">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="887bb-123">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-124">Valeur qui spécifie le type de l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-124">A value that specifies the type of the biometric unit.</span></span> <span data-ttu-id="887bb-125">Seule **une \_ \_ empreinte digitale de type WINBIO** est actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="887bb-125">Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-126">**SensorSubType**</span><span class="sxs-lookup"><span data-stu-id="887bb-126">**SensorSubType**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-127">Sous-type de capteur défini pour le type biométrique spécifié par le membre **BiometricFactor** .</span><span class="sxs-lookup"><span data-stu-id="887bb-127">A sensor subtype defined for the biometric type specified by the **BiometricFactor** member.</span></span> <span data-ttu-id="887bb-128">Seuls les types d’empreintes digitales (**\_ \_ empreintes de type WINBIO**) sont actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="887bb-128">Only fingerprint types (**WINBIO\_TYPE\_FINGERPRINT**) are currently supported.</span></span> <span data-ttu-id="887bb-129">Les sous-types suivants sont actuellement définis pour les empreintes digitales :</span><span class="sxs-lookup"><span data-stu-id="887bb-129">The following subtypes are currently defined for fingerprints:</span></span>

-   <span data-ttu-id="887bb-130">\_sous-type de capteur WINBIO \_ \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="887bb-130">WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="887bb-131">\_balayage de \_ sous-type de capteur WINBIO FP \_ \_</span><span class="sxs-lookup"><span data-stu-id="887bb-131">WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE</span></span>
-   <span data-ttu-id="887bb-132">WINBIO \_ de \_ sous-type de capteur FP \_ \_</span><span class="sxs-lookup"><span data-stu-id="887bb-132">WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH</span></span>

</dd> <dt>

<span data-ttu-id="887bb-133">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="887bb-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-134">Masque de réévaluation des fonctionnalités du capteur biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-134">A bitmask of the biometric sensor capabilities.</span></span> <span data-ttu-id="887bb-135">Il peut s’agir d’une **opération or au niveau du** bit des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="887bb-135">This can be a bitwise **OR** of the following values:</span></span>

-   <span data-ttu-id="887bb-136">\_capteur de capacité WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-136">WINBIO\_CAPABILITY\_SENSOR</span></span>
-   <span data-ttu-id="887bb-137">\_correspondance des fonctionnalités WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-137">WINBIO\_CAPABILITY\_MATCHING</span></span>
-   <span data-ttu-id="887bb-138">\_ \_ base de données de capacité WINBIO</span><span class="sxs-lookup"><span data-stu-id="887bb-138">WINBIO\_CAPABILITY\_DATABASE</span></span>
-   <span data-ttu-id="887bb-139">\_traitement des capacités WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-139">WINBIO\_CAPABILITY\_PROCESSING</span></span>
-   <span data-ttu-id="887bb-140">\_chiffrement des fonctionnalités WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-140">WINBIO\_CAPABILITY\_ENCRYPTION</span></span>
-   <span data-ttu-id="887bb-141">NAVIGATION dans les \_ fonctionnalités WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-141">WINBIO\_CAPABILITY\_NAVIGATION</span></span>
-   <span data-ttu-id="887bb-142">\_indicateur de capacité WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-142">WINBIO\_CAPABILITY\_INDICATOR</span></span>
-   <span data-ttu-id="887bb-143">\_ \_ capteur virtuel de capacité WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="887bb-143">WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR</span></span>
    > [!Note]  
    > <span data-ttu-id="887bb-144">La constante de **\_ \_ \_ capteur virtuel de capacité WINBIO** s’applique uniquement à Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="887bb-144">The **WINBIO\_CAPABILITY\_VIRTUAL\_SENSOR** constant applies only for Windows 10 and later.</span></span>

     

</dd> <dt>

<span data-ttu-id="887bb-145">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="887bb-145">**DeviceInstanceId**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-146">Valeur de chaîne qui contient l’ID d’appareil.</span><span class="sxs-lookup"><span data-stu-id="887bb-146">A string value that contains the device ID.</span></span> <span data-ttu-id="887bb-147">La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="887bb-147">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-148">**Description**</span><span class="sxs-lookup"><span data-stu-id="887bb-148">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-149">Valeur de chaîne qui contient une description de l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-149">A string value that contains a description of the biometric unit.</span></span> <span data-ttu-id="887bb-150">La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="887bb-150">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-151">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="887bb-151">**Manufacturer**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-152">Valeur de chaîne qui contient le nom du fabricant.</span><span class="sxs-lookup"><span data-stu-id="887bb-152">A string value that contains the name of the manufacturer.</span></span> <span data-ttu-id="887bb-153">La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="887bb-153">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-154">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="887bb-154">**Model**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-155">Valeur de chaîne qui contient le numéro de modèle de l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-155">A string value that contains the model number of the biometric unit.</span></span> <span data-ttu-id="887bb-156">La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="887bb-156">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-157">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="887bb-157">**SerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-158">Chaîne Unicode terminée par le caractère **null** qui contient le numéro de série de l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-158">A **NULL**-terminated Unicode string that contains the serial number of the biometric unit.</span></span> <span data-ttu-id="887bb-159">La chaîne peut contenir jusqu’à 256 caractères Unicode, y compris un caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="887bb-159">The string can contain up to 256 Unicode characters including a terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="887bb-160">**FirmwareVersion**</span><span class="sxs-lookup"><span data-stu-id="887bb-160">**FirmwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="887bb-161">Structure [**de \_ version de WINBIO**](winbio-version.md) qui contient les numéros de version principale et secondaire pour l’unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="887bb-161">A [**WINBIO\_VERSION**](winbio-version.md) structure that contains the major and minor version numbers for the biometric unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="887bb-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="887bb-162">Requirements</span></span>



| <span data-ttu-id="887bb-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="887bb-163">Requirement</span></span> | <span data-ttu-id="887bb-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="887bb-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887bb-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887bb-165">Minimum supported client</span></span><br/> | <span data-ttu-id="887bb-166">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="887bb-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="887bb-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887bb-167">Minimum supported server</span></span><br/> | <span data-ttu-id="887bb-168">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="887bb-168">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="887bb-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="887bb-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="887bb-170"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="887bb-170"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887bb-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="887bb-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887bb-172">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="887bb-172">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="887bb-173">**WinBioEnumBiometricUnits**</span><span class="sxs-lookup"><span data-stu-id="887bb-173">**WinBioEnumBiometricUnits**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





