---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_AFSDBType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942138"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="58ba4-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType</span><span class="sxs-lookup"><span data-stu-id="58ba4-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="58ba4-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.</span><span class="sxs-lookup"><span data-stu-id="58ba4-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ba4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58ba4-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="58ba4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58ba4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ba4-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="58ba4-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="58ba4-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="58ba4-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="58ba4-117">Class of the RR.</span></span> <span data-ttu-id="58ba4-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="58ba4-118">Default value is 1.</span></span> <span data-ttu-id="58ba4-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="58ba4-119">The following values are valid.</span></span>



| <span data-ttu-id="58ba4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ba4-120">Value</span></span>                                                                                                | <span data-ttu-id="58ba4-121">Signification</span><span class="sxs-lookup"><span data-stu-id="58ba4-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="58ba4-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="58ba4-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="58ba4-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="58ba4-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="58ba4-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="58ba4-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="58ba4-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="58ba4-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="58ba4-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="58ba4-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="58ba4-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="58ba4-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="58ba4-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="58ba4-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-132">*Sous-type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-133">Sous-type du serveur AFS hôte.</span><span class="sxs-lookup"><span data-stu-id="58ba4-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="58ba4-134">Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée.</span><span class="sxs-lookup"><span data-stu-id="58ba4-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="58ba4-135">Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.</span><span class="sxs-lookup"><span data-stu-id="58ba4-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-136">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-137">Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="58ba4-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="58ba4-138">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="58ba4-139">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="58ba4-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ba4-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58ba4-140">Return value</span></span>

<span data-ttu-id="58ba4-141">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="58ba4-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ba4-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ba4-142">Requirements</span></span>



| <span data-ttu-id="58ba4-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ba4-143">Requirement</span></span> | <span data-ttu-id="58ba4-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ba4-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ba4-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ba4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="58ba4-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ba4-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="58ba4-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ba4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="58ba4-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ba4-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="58ba4-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58ba4-149">Namespace</span></span><br/>                | <span data-ttu-id="58ba4-150">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="58ba4-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="58ba4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="58ba4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58ba4-152"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58ba4-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ba4-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ba4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ba4-154">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="58ba4-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="58ba4-155">**Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="58ba4-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="58ba4-156">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="58ba4-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





