---
title: SoHAttributeValue Union (NapProtocol. h)
description: Définit le contenu du membre de type dans une structure SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- SoHAttributeValue d’Union NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466458"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="515d7-104">SoHAttributeValue Union</span><span class="sxs-lookup"><span data-stu-id="515d7-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="515d7-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="515d7-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="515d7-106">L’Union **SoHAttributeValue** définit le contenu du membre de **type** dans une structure [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="515d7-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="515d7-107">La structure de l’Union **SoHAttributeValue** est déterminée par le [**SoHAttributeType**](sohattributetype-enum.md) spécifié dans le membre de **type** de la structure [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="515d7-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="515d7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="515d7-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="515d7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="515d7-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="515d7-110">**idVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-111">**cas (sohAttributeTypeSystemHealthId)**</span><span class="sxs-lookup"><span data-stu-id="515d7-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="515d7-112">[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent d’intégrité système (SHA) ou du programme de validation d’intégrité système (SHV) qui a construit ce paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="515d7-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="515d7-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-114">**cas (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="515d7-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="515d7-115">Les adresses IPv4 des serveurs de correction utilisés par le système NAP.</span><span class="sxs-lookup"><span data-stu-id="515d7-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="515d7-116">**count**</span><span class="sxs-lookup"><span data-stu-id="515d7-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-117">Nombre d’adresses IPv4 dans le membre **Addresses** dans la plage comprise entre 1 et [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="515d7-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="515d7-118">**addresses**</span><span class="sxs-lookup"><span data-stu-id="515d7-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-119">Tableau de structures [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) qui contiennent les adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="515d7-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="515d7-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-121">**cas (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="515d7-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="515d7-122">Les adresses IPv6 des serveurs de correction utilisés par le système NAP.</span><span class="sxs-lookup"><span data-stu-id="515d7-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="515d7-123">**count**</span><span class="sxs-lookup"><span data-stu-id="515d7-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-124">Nombre d’adresses IPv4 dans le membre **Addresses** dans la plage comprise entre 1 et [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="515d7-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="515d7-125">**addresses**</span><span class="sxs-lookup"><span data-stu-id="515d7-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-126">Tableau de structures [**AdresseIPv6**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) qui contiennent les adresses IPv4.</span><span class="sxs-lookup"><span data-stu-id="515d7-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="515d7-127">**codesVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-128">**case (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span><span class="sxs-lookup"><span data-stu-id="515d7-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="515d7-129">Structure [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) qui contient les codes de résultat de conformité de l’application définis pour les [**constantes d’erreur**](nap-error-constants.md)de client ou NAP.</span><span class="sxs-lookup"><span data-stu-id="515d7-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="515d7-130">Un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) doit contenir ce TLV ou le **sohAttributeTypeFailureCategory** TLV.</span><span class="sxs-lookup"><span data-stu-id="515d7-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="515d7-131">**dateTimeVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-132">**case (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span><span class="sxs-lookup"><span data-stu-id="515d7-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="515d7-133">Structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui contient l’heure de la dernière mise à jour de [**déclaration d’intégrité**](/windows/win32/api/naptypes/ns-naptypes-soh) ou la durée de génération de **déclaration d’intégrité** .</span><span class="sxs-lookup"><span data-stu-id="515d7-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="515d7-134">**vendorSpecificVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-135">**cas (sohAttributeTypeVendorSpecific)**</span><span class="sxs-lookup"><span data-stu-id="515d7-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="515d7-136">Données spécifiques à l’application définies par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="515d7-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="515d7-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="515d7-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-138">Identificateur de 4 octets qui définit l’ID de la paire SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="515d7-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="515d7-139">Les 3 premiers octets correspondent au code SMI attribué par l’IETF au fournisseur et le dernier octet identifie le composant lui-même.</span><span class="sxs-lookup"><span data-stu-id="515d7-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="515d7-140">Lors de l’implémentation d’un SHA ou d’un SHV, n’utilisez pas les valeurs d’ID attribuées aux composants d’intégrité système Microsoft internes sur les [**constantes de fournisseur NAP**](nap-vendor-constants.md).</span><span class="sxs-lookup"><span data-stu-id="515d7-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="515d7-141">**size**</span><span class="sxs-lookup"><span data-stu-id="515d7-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-142">Taille, en octets, des données de fournisseur dans la plage comprise entre 0 et ([**maxSoHAttributeSize**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="515d7-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="515d7-143">**Champ vendorspecificdata**</span><span class="sxs-lookup"><span data-stu-id="515d7-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-144">Pointeur vers les données spécifiques au fournisseur dans l’ordre des octets du réseau.</span><span class="sxs-lookup"><span data-stu-id="515d7-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="515d7-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="515d7-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-146">**case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**</span><span class="sxs-lookup"><span data-stu-id="515d7-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="515d7-147">La classe d’intégrité, la catégorie d’échec ou l’état d’isolement étendu d’un composant NAP en tant que valeur [**HealthClassValue**](healthclassvalue-enum.md) ou [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) , ou une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="515d7-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="515d7-148">**octetStringVal**</span><span class="sxs-lookup"><span data-stu-id="515d7-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-149">**default**</span><span class="sxs-lookup"><span data-stu-id="515d7-149">**default**</span></span>

<span data-ttu-id="515d7-150">Les valeurs des attributs suivants sont des chaînes d’octets :</span><span class="sxs-lookup"><span data-stu-id="515d7-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="515d7-151">sohAttributeTypeSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="515d7-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="515d7-152">sohAttributeTypeClientId</span><span class="sxs-lookup"><span data-stu-id="515d7-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="515d7-153">sohAttributeTypeProductName</span><span class="sxs-lookup"><span data-stu-id="515d7-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="515d7-154">sohAttributeTypeHealthClassStatus</span><span class="sxs-lookup"><span data-stu-id="515d7-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="515d7-155">Pour la compatibilité ascendante, tous les attributs non reconnus sont retournés en tant que chaînes d’octets.</span><span class="sxs-lookup"><span data-stu-id="515d7-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="515d7-156">les **données** doivent être dans l’ordre des octets du réseau.</span><span class="sxs-lookup"><span data-stu-id="515d7-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="515d7-157">**size**</span><span class="sxs-lookup"><span data-stu-id="515d7-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-158">Taille, en octets, des **données** dans la plage comprise entre 0 et [**maxSoHAttributeSize**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="515d7-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="515d7-159">**data**</span><span class="sxs-lookup"><span data-stu-id="515d7-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="515d7-160">Pointeur vers la valeur de chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="515d7-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="515d7-161">Disposition réelle des données</span><span class="sxs-lookup"><span data-stu-id="515d7-161">Actual data layout</span></span>

<span data-ttu-id="515d7-162">En raison de la nature de l’environnement de publication du SDK, les unions ne sont pas clairement représentées dans les blocs de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="515d7-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="515d7-163">Voici la syntaxe réelle du fichier d’en-tête NapProtocol. h.</span><span class="sxs-lookup"><span data-stu-id="515d7-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="515d7-164">Notes</span><span class="sxs-lookup"><span data-stu-id="515d7-164">Remarks</span></span>

<span data-ttu-id="515d7-165">Ces types d’attributs sont consommés par le système NAP :</span><span class="sxs-lookup"><span data-stu-id="515d7-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="515d7-166">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="515d7-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="515d7-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="515d7-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="515d7-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="515d7-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="515d7-169">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="515d7-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="515d7-170">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="515d7-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="515d7-171">Le reste du [**SoHAttributeTypes**](sohattributetype-enum.md) est conçu de manière purement normative pour une utilisation par les programmes d’intégrité des intégrité et les SHV.</span><span class="sxs-lookup"><span data-stu-id="515d7-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="515d7-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="515d7-172">Requirements</span></span>



| <span data-ttu-id="515d7-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="515d7-173">Requirement</span></span> | <span data-ttu-id="515d7-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="515d7-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="515d7-175">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="515d7-175">Minimum supported client</span></span><br/> | <span data-ttu-id="515d7-176">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="515d7-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="515d7-177">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="515d7-177">Minimum supported server</span></span><br/> | <span data-ttu-id="515d7-178">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="515d7-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="515d7-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="515d7-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="515d7-180"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="515d7-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="515d7-181">MIDL</span><span class="sxs-lookup"><span data-stu-id="515d7-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="515d7-182"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="515d7-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="515d7-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="515d7-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515d7-184">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="515d7-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="515d7-185">Structures NAP</span><span class="sxs-lookup"><span data-stu-id="515d7-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

