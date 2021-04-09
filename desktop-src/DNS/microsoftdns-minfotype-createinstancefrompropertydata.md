---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_MINFOType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource d’informations de messagerie (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032388"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="c173a-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MINFOType</span><span class="sxs-lookup"><span data-stu-id="c173a-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="c173a-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource d’informations de messagerie (mInfo).</span><span class="sxs-lookup"><span data-stu-id="c173a-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c173a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c173a-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c173a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c173a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c173a-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c173a-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c173a-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c173a-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="c173a-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c173a-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c173a-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c173a-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c173a-117">Class of the RR.</span></span> <span data-ttu-id="c173a-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="c173a-118">Default value is 1.</span></span> <span data-ttu-id="c173a-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="c173a-119">The following values are valid.</span></span>



| <span data-ttu-id="c173a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c173a-120">Value</span></span>                                                                                                | <span data-ttu-id="c173a-121">Signification</span><span class="sxs-lookup"><span data-stu-id="c173a-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c173a-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c173a-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c173a-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="c173a-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c173a-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c173a-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c173a-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c173a-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c173a-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c173a-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c173a-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="c173a-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c173a-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c173a-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c173a-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c173a-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c173a-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c173a-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c173a-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-132">*ResponsibleMailbox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c173a-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-133">Nom de domaine complet spécifiant une boîte aux lettres responsable de la liste de distribution ou de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c173a-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-134">*ErrorMailbox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c173a-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-135">Nom de domaine complet spécifiant une boîte aux lettres pour recevoir des messages d’erreur liés à la liste de diffusion ou à la boîte aux lettres spécifiée par le nom de propriétaire de l’enregistrement MINFO.</span><span class="sxs-lookup"><span data-stu-id="c173a-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="c173a-136">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c173a-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c173a-137">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c173a-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c173a-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c173a-138">Return value</span></span>

<span data-ttu-id="c173a-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c173a-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c173a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c173a-140">Requirements</span></span>



| <span data-ttu-id="c173a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c173a-141">Requirement</span></span> | <span data-ttu-id="c173a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="c173a-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c173a-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c173a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c173a-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c173a-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c173a-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c173a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c173a-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c173a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c173a-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c173a-147">Namespace</span></span><br/>                | <span data-ttu-id="c173a-148">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c173a-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c173a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c173a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c173a-150"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c173a-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c173a-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c173a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c173a-152">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="c173a-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="c173a-153">**Modifier la méthode de la \_ classe MINFOType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c173a-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="c173a-154">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c173a-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





