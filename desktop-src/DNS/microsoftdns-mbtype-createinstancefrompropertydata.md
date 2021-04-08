---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_MBType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de boîte aux lettres (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MBType
- MicrosoftDNS_MBType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843773"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="ec2f6-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MBType</span><span class="sxs-lookup"><span data-stu-id="ec2f6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="ec2f6-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de boîte aux lettres (MB).</span><span class="sxs-lookup"><span data-stu-id="ec2f6-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2f6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec2f6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ec2f6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec2f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2f6-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f6-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f6-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f6-116">*RecordClass* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-117">Optional.</span></span> <span data-ttu-id="ec2f6-118">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-118">Class of the RR.</span></span> <span data-ttu-id="ec2f6-119">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-119">Default value is 1.</span></span> <span data-ttu-id="ec2f6-120">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-120">The following values are valid.</span></span>



| <span data-ttu-id="ec2f6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f6-121">Value</span></span>                                                                                                | <span data-ttu-id="ec2f6-122">Signification</span><span class="sxs-lookup"><span data-stu-id="ec2f6-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ec2f6-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ec2f6-124">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="ec2f6-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ec2f6-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ec2f6-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ec2f6-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ec2f6-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ec2f6-128">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="ec2f6-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ec2f6-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ec2f6-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ec2f6-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ec2f6-131">*TTL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-132">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-132">Optional.</span></span> <span data-ttu-id="ec2f6-133">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f6-134">*MBHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-135">Nom d’hôte de la boîte aux lettres pour le RR.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ec2f6-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ec2f6-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2f6-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec2f6-138">Return value</span></span>

<span data-ttu-id="ec2f6-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2f6-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec2f6-140">Requirements</span></span>



| <span data-ttu-id="ec2f6-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec2f6-141">Requirement</span></span> | <span data-ttu-id="ec2f6-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec2f6-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f6-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec2f6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2f6-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec2f6-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ec2f6-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec2f6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2f6-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec2f6-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec2f6-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec2f6-147">Namespace</span></span><br/>                | <span data-ttu-id="ec2f6-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ec2f6-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ec2f6-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ec2f6-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec2f6-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec2f6-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec2f6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2f6-152">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="ec2f6-153">**Modifier la méthode de la \_ classe MBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ec2f6-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





