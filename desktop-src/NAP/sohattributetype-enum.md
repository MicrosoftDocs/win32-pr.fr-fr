---
title: Énumération SoHAttributeType (NapProtocol. h)
description: Spécifie le type d’attribut stocké dans l’objet de type-length-value (TLV) d’attribut.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- SoHAttributeType de l’énumération NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317373"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="e4196-104">Énumération SoHAttributeType</span><span class="sxs-lookup"><span data-stu-id="e4196-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="e4196-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4196-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e4196-106">L’énumération **SoHAttributeType** spécifie le type d’attribut stocké dans l’objet de type-length-value (TLV) d’attribut.</span><span class="sxs-lookup"><span data-stu-id="e4196-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4196-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4196-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="e4196-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e4196-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e4196-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span><span class="sxs-lookup"><span data-stu-id="e4196-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-110">Spécifie le type d’attribut de l’ID d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="e4196-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="e4196-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-112">Spécifie le type d’attribut du serveur de correction IPv4.</span><span class="sxs-lookup"><span data-stu-id="e4196-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span><span class="sxs-lookup"><span data-stu-id="e4196-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-114">Spécifie le type d’attribut de code de résultat de conformité.</span><span class="sxs-lookup"><span data-stu-id="e4196-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span><span class="sxs-lookup"><span data-stu-id="e4196-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-116">Spécifie l’heure du dernier type d’attribut de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e4196-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span><span class="sxs-lookup"><span data-stu-id="e4196-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-118">Spécifie le type d’attribut de l’ID client.</span><span class="sxs-lookup"><span data-stu-id="e4196-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="e4196-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-120">Spécifie le type d’attribut spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e4196-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span><span class="sxs-lookup"><span data-stu-id="e4196-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-122">Spécifie le type d’attribut de classe d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="e4196-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="e4196-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-124">Spécifie le type d’attribut de version du logiciel.</span><span class="sxs-lookup"><span data-stu-id="e4196-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span><span class="sxs-lookup"><span data-stu-id="e4196-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-126">Spécifie le type d’attribut de nom de produit.</span><span class="sxs-lookup"><span data-stu-id="e4196-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span><span class="sxs-lookup"><span data-stu-id="e4196-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-128">Spécifie le type d’attribut d’état de la classe d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="e4196-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span><span class="sxs-lookup"><span data-stu-id="e4196-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-130">Spécifie l’heure de génération du type d’attribut d’état d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="e4196-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span><span class="sxs-lookup"><span data-stu-id="e4196-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-132">Spécifie le type d’attribut de code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e4196-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span><span class="sxs-lookup"><span data-stu-id="e4196-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-134">Spécifie le type d’attribut de catégorie d’échec.</span><span class="sxs-lookup"><span data-stu-id="e4196-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="e4196-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-136">Spécifie le type d’attribut du serveur de correction IPv6.</span><span class="sxs-lookup"><span data-stu-id="e4196-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e4196-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span><span class="sxs-lookup"><span data-stu-id="e4196-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="e4196-138">Spécifie le type d’attribut d’état d’isolement étendu.</span><span class="sxs-lookup"><span data-stu-id="e4196-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4196-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e4196-139">Remarks</span></span>

<span data-ttu-id="e4196-140">La structure [**SoHAttributeValue**](sohattributevalue-union.md) définit les valeurs d’attribut qui correspondent à chaque type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="e4196-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="e4196-141">Ces types d’attributs sont consommés par le système NAP :</span><span class="sxs-lookup"><span data-stu-id="e4196-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="e4196-142">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="e4196-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="e4196-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="e4196-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="e4196-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="e4196-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="e4196-145">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="e4196-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="e4196-146">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="e4196-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="e4196-147">Les autres types sont uniquement destinés à guider l’utilisation par les Sha et les validateurs d’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="e4196-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4196-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4196-148">Requirements</span></span>



| <span data-ttu-id="e4196-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4196-149">Requirement</span></span> | <span data-ttu-id="e4196-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4196-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4196-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4196-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e4196-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4196-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e4196-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4196-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e4196-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4196-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e4196-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4196-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4196-156"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4196-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4196-157">MIDL</span><span class="sxs-lookup"><span data-stu-id="e4196-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4196-158"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4196-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4196-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4196-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4196-160">**SoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="e4196-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="e4196-161">**SoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="e4196-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="e4196-162">**Intégrité**</span><span class="sxs-lookup"><span data-stu-id="e4196-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="e4196-163">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="e4196-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="e4196-164">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="e4196-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





