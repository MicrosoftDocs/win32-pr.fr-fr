---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_MXType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de serveur de messagerie (MR).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MXType
- MicrosoftDNS_MXType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103852"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="9f066-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MXType</span><span class="sxs-lookup"><span data-stu-id="9f066-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="9f066-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de serveur de messagerie (Mr).</span><span class="sxs-lookup"><span data-stu-id="9f066-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f066-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f066-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9f066-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f066-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f066-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f066-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="9f066-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f066-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="9f066-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f066-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="9f066-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9f066-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="9f066-117">Class of the RR.</span></span> <span data-ttu-id="9f066-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="9f066-118">Default value is 1.</span></span> <span data-ttu-id="9f066-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="9f066-119">The following values are valid.</span></span>



| <span data-ttu-id="9f066-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f066-120">Value</span></span>                                                                                                | <span data-ttu-id="9f066-121">Signification</span><span class="sxs-lookup"><span data-stu-id="9f066-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9f066-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9f066-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9f066-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="9f066-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9f066-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9f066-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9f066-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="9f066-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="9f066-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9f066-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9f066-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="9f066-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="9f066-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9f066-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9f066-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="9f066-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="9f066-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9f066-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="9f066-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-132">*Préférence* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f066-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-133">Préférence donnée à ce RR, parmi d’autres au même propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9f066-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="9f066-134">Les valeurs les plus basses sont préférées.</span><span class="sxs-lookup"><span data-stu-id="9f066-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-135">*MailExchange* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f066-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-136">Nom de domaine complet spécifiant un ordinateur hôte prêt à agir comme échange de messagerie pour le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9f066-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="9f066-137">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="9f066-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9f066-138">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="9f066-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f066-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f066-139">Return value</span></span>

<span data-ttu-id="9f066-140">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f066-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f066-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f066-141">Requirements</span></span>



| <span data-ttu-id="9f066-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f066-142">Requirement</span></span> | <span data-ttu-id="9f066-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f066-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f066-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f066-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9f066-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f066-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9f066-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f066-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9f066-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f066-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9f066-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f066-148">Namespace</span></span><br/>                | <span data-ttu-id="9f066-149">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="9f066-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9f066-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9f066-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f066-151"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f066-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f066-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f066-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f066-153">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="9f066-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="9f066-154">**Modifier la méthode de la \_ classe MXType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="9f066-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="9f066-155">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="9f066-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





