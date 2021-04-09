---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_MGType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de groupe de messagerie (MG).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MGType
- MicrosoftDNS_MGType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104734"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="a9281-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MGType</span><span class="sxs-lookup"><span data-stu-id="a9281-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="a9281-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de groupe de messagerie (mg).</span><span class="sxs-lookup"><span data-stu-id="a9281-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9281-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9281-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a9281-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9281-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9281-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9281-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a9281-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9281-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9281-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="a9281-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9281-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9281-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a9281-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="a9281-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a9281-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="a9281-117">Class of the RR.</span></span> <span data-ttu-id="a9281-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="a9281-118">Default value is 1.</span></span> <span data-ttu-id="a9281-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="a9281-119">The following values are valid.</span></span>



| <span data-ttu-id="a9281-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9281-120">Value</span></span>                                                                                                | <span data-ttu-id="a9281-121">Signification</span><span class="sxs-lookup"><span data-stu-id="a9281-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a9281-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a9281-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a9281-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="a9281-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a9281-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a9281-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a9281-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="a9281-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="a9281-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a9281-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="a9281-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="a9281-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="a9281-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="a9281-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="a9281-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="a9281-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a9281-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a9281-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="a9281-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a9281-132">*MGMailbox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9281-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-133">Nom de domaine complet spécifiant une boîte aux lettres qui est membre du groupe de messagerie spécifié par le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9281-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="a9281-134">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a9281-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a9281-135">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="a9281-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9281-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9281-136">Return value</span></span>

<span data-ttu-id="a9281-137">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9281-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9281-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9281-138">Requirements</span></span>



| <span data-ttu-id="a9281-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9281-139">Requirement</span></span> | <span data-ttu-id="a9281-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9281-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9281-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9281-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a9281-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9281-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a9281-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9281-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a9281-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9281-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a9281-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9281-145">Namespace</span></span><br/>                | <span data-ttu-id="a9281-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="a9281-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a9281-147">MOF</span><span class="sxs-lookup"><span data-stu-id="a9281-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9281-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9281-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9281-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9281-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9281-150">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="a9281-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="a9281-151">**Modifier la méthode de la \_ classe MGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="a9281-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="a9281-152">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="a9281-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





