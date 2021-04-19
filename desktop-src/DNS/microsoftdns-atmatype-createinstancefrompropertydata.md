---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_ATMAType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’adresse ATM (ATMA).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513781"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a><span data-ttu-id="97c82-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ATMAType</span><span class="sxs-lookup"><span data-stu-id="97c82-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ATMAType class</span></span>

<span data-ttu-id="97c82-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’adresse ATM (ATMA).</span><span class="sxs-lookup"><span data-stu-id="97c82-107">The **CreateInstanceFromPropertyData** method instantiates an ATM Address to Name (ATMA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c82-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97c82-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="97c82-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97c82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c82-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c82-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="97c82-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c82-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="97c82-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c82-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="97c82-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="97c82-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="97c82-117">Class of the RR.</span></span> <span data-ttu-id="97c82-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="97c82-118">Default value is 1.</span></span> <span data-ttu-id="97c82-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="97c82-119">The following values are valid.</span></span>



| <span data-ttu-id="97c82-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="97c82-120">Value</span></span>                                                                                                | <span data-ttu-id="97c82-121">Signification</span><span class="sxs-lookup"><span data-stu-id="97c82-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="97c82-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="97c82-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="97c82-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="97c82-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="97c82-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="97c82-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="97c82-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="97c82-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="97c82-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="97c82-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="97c82-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="97c82-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="97c82-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="97c82-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="97c82-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="97c82-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="97c82-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="97c82-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="97c82-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-132">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c82-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-133">Format d’adresse ATM.</span><span class="sxs-lookup"><span data-stu-id="97c82-133">ATM address format.</span></span> <span data-ttu-id="97c82-134">Deux valeurs possibles pour FORMAT sont : 0 indiquant le format AESA (ATM End System Address) et 1 indiquant le format E. 164.</span><span class="sxs-lookup"><span data-stu-id="97c82-134">Two possible values for FORMAT are: 0 indicating ATM End System Address (AESA) format and 1 indicating E.164 format.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-135">*ATMAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97c82-135">*ATMAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-136">Chaîne de longueur variable d’octets contenant l’adresse ATM du nœud/propriétaire auquel appartient ce RR.</span><span class="sxs-lookup"><span data-stu-id="97c82-136">Variable length string of octets containing the ATM address of the node/owner to which this RR pertains.</span></span> <span data-ttu-id="97c82-137">Les quatre premiers octets du tableau sont utilisés pour stocker la taille de la chaîne d’octets.</span><span class="sxs-lookup"><span data-stu-id="97c82-137">The first four bytes of the array are used to store the size of the octet string.</span></span> <span data-ttu-id="97c82-138">L’octet le plus significatif est stocké à l’octet 0.</span><span class="sxs-lookup"><span data-stu-id="97c82-138">The most significant byte is stored in byte 0.</span></span>

</dd> <dt>

<span data-ttu-id="97c82-139">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="97c82-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="97c82-140">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="97c82-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c82-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97c82-141">Return value</span></span>

<span data-ttu-id="97c82-142">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="97c82-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c82-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97c82-143">Requirements</span></span>



| <span data-ttu-id="97c82-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97c82-144">Requirement</span></span> | <span data-ttu-id="97c82-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="97c82-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c82-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97c82-146">Minimum supported client</span></span><br/> | <span data-ttu-id="97c82-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97c82-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="97c82-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97c82-148">Minimum supported server</span></span><br/> | <span data-ttu-id="97c82-149">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97c82-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="97c82-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97c82-150">Namespace</span></span><br/>                | <span data-ttu-id="97c82-151">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="97c82-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="97c82-152">MOF</span><span class="sxs-lookup"><span data-stu-id="97c82-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97c82-153"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97c82-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c82-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97c82-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c82-155">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="97c82-155">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)
</dt> <dt>

[<span data-ttu-id="97c82-156">**Modifier la méthode de la \_ classe ATMAType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="97c82-156">**Modify Method of the MicrosoftDNS\_ATMAType Class**</span></span>](microsoftdns-atmatype-modify.md)
</dt> <dt>

[<span data-ttu-id="97c82-157">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="97c82-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





