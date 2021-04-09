---
title: Classe MicrosoftDNS_ResourceRecord
description: La \_ classe MicrosoftDNS ResourceRecord représente les propriétés générales d’un RR DNS. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord de la classe DNS
- MicrosoftDNS_ResourceRecord de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe546ceabb5590ccd4907448af5efd5e2d4fe2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942282"
---
# <a name="microsoftdns_resourcerecord-class"></a><span data-ttu-id="752b7-105">MicrosoftDNS \_ ResourceRecord, classe</span><span class="sxs-lookup"><span data-stu-id="752b7-105">MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="752b7-106">La classe **MicrosoftDNS \_ ResourceRecord** représente les propriétés générales d’un RR DNS.</span><span class="sxs-lookup"><span data-stu-id="752b7-106">The **MicrosoftDNS\_ResourceRecord** class represents the general properties of a DNS RR.</span></span>

<span data-ttu-id="752b7-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="752b7-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="752b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="752b7-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a><span data-ttu-id="752b7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="752b7-109">Members</span></span>

<span data-ttu-id="752b7-110">La classe **MicrosoftDNS \_ ResourceRecord** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="752b7-110">The **MicrosoftDNS\_ResourceRecord** class has these types of members:</span></span>

-   [<span data-ttu-id="752b7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="752b7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="752b7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="752b7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="752b7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="752b7-113">Methods</span></span>

<span data-ttu-id="752b7-114">La classe **MicrosoftDNS \_ ResourceRecord** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="752b7-114">The **MicrosoftDNS\_ResourceRecord** class has these methods.</span></span>



| <span data-ttu-id="752b7-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="752b7-115">Method</span></span>                                   | <span data-ttu-id="752b7-116">Description</span><span class="sxs-lookup"><span data-stu-id="752b7-116">Description</span></span>                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="752b7-117">**CreateInstanceFromTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="752b7-117">**CreateInstanceFromTextRepresentation**</span></span> | <span data-ttu-id="752b7-118">Analyse le RR dans la chaîne TextRepresentation, et avec les noms de conteneur et de serveur DNS d’entrée, définit et instancie un objet ResourceRecord.</span><span class="sxs-lookup"><span data-stu-id="752b7-118">Parses the RR in the TextRepresentation string, and with the input DNS Server and Container Names, defines, and instantiates a ResourceRecord object.</span></span> <span data-ttu-id="752b7-119">La méthode retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="752b7-119">The method returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="752b7-120">Qualificateurs : aucun</span><span class="sxs-lookup"><span data-stu-id="752b7-120">Qualifiers: None</span></span><br/> |
| <span data-ttu-id="752b7-121">**GetObjectByTextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="752b7-121">**GetObjectByTextRepresentation**</span></span>        | <span data-ttu-id="752b7-122">Récupère une instance existante de la sous- \_ classe ResourceRecord MicrosoftDns, représentée par la chaîne TextRepresentation, ainsi que le nom du conteneur et du serveur DNS.</span><span class="sxs-lookup"><span data-stu-id="752b7-122">Retrieves an existing instance of the MicrosoftDns\_ResourceRecord subclass, represented by the TextRepresentation string along with the DNS Server and Container Name.</span></span> <br/> <span data-ttu-id="752b7-123">Qualificateurs : aucun</span><span class="sxs-lookup"><span data-stu-id="752b7-123">Qualifiers: None</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="752b7-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="752b7-124">Properties</span></span>

<span data-ttu-id="752b7-125">La classe **MicrosoftDNS \_ ResourceRecord** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="752b7-125">The **MicrosoftDNS\_ResourceRecord** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="752b7-126">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="752b7-126">**ContainerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-129">Indique le nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient le RR.</span><span class="sxs-lookup"><span data-stu-id="752b7-129">Indicates the name of the Container for the Zone, Cache, or RootHints instance that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-130">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="752b7-130">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-133">Indique le nom de domaine complet ou l’adresse IP du serveur DNS qui contient le RR.</span><span class="sxs-lookup"><span data-stu-id="752b7-133">Indicates the FQDN or IP address of the DNS Server that contains the RR.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-134">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="752b7-134">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-137">Représente le nom de domaine complet du domaine qui contient le RR.</span><span class="sxs-lookup"><span data-stu-id="752b7-137">Represents the FQDN of the Domain that contains the RR.</span></span> <span data-ttu-id="752b7-138">Cette propriété peut contenir les chaînes \\ .. Cache \\ ou \\ .. RootHints \\ si le cache interne ou RootHints contient le RR, respectivement.</span><span class="sxs-lookup"><span data-stu-id="752b7-138">This property may contain the strings \\..Cache\\ or \\..RootHints\\ if the internal cache or RootHints contain the RR, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-139">**OwnerName**</span><span class="sxs-lookup"><span data-stu-id="752b7-139">**OwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-142">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="752b7-142">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-143">**RecordClass = 1**</span><span class="sxs-lookup"><span data-stu-id="752b7-143">**RecordClass=1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="752b7-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-146">\* \* Windows Server 2003 : \* \*</span><span class="sxs-lookup"><span data-stu-id="752b7-146">\*\*Windows Server 2003:  \*\*</span></span>

<span data-ttu-id="752b7-147">Cette chaîne représente la classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="752b7-147">This string represents the class of the Resource Record.</span></span> <span data-ttu-id="752b7-148">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="752b7-148">Valid values include:</span></span>

<span data-ttu-id="752b7-149">1 : dans (Internet)</span><span class="sxs-lookup"><span data-stu-id="752b7-149">1: IN (Internet)</span></span>

<span data-ttu-id="752b7-150">2 : CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="752b7-150">2: CS (CSNET)</span></span>

<span data-ttu-id="752b7-151">3 : CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="752b7-151">3: CH (CHAOS)</span></span>

<span data-ttu-id="752b7-152">4 : HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="752b7-152">4: HS (Hesiod)</span></span>

</dd> <dt>

<span data-ttu-id="752b7-153">**RecordData**</span><span class="sxs-lookup"><span data-stu-id="752b7-153">**RecordData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-156">Données d’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="752b7-156">Resource record data.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-157">**TextRepresentation**</span><span class="sxs-lookup"><span data-stu-id="752b7-157">**TextRepresentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="752b7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-160">Représentation textuelle de l’ensemble du RR.</span><span class="sxs-lookup"><span data-stu-id="752b7-160">Text representation of the entire RR.</span></span>

</dd> <dt>

<span data-ttu-id="752b7-161">**Confirmé**</span><span class="sxs-lookup"><span data-stu-id="752b7-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="752b7-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-164">Heure de la dernière actualisation de l’enregistrement de ressource, exprimée en heures écoulées depuis le 1er janvier 1601, heure de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="752b7-164">Time at which the RR was last refreshed, expressed in elapsed hours since January 1, 1601, Greenwich Mean Time (GMT).</span></span>

</dd> <dt>

<span data-ttu-id="752b7-165">**TTL**</span><span class="sxs-lookup"><span data-stu-id="752b7-165">**TTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="752b7-166">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="752b7-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="752b7-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="752b7-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="752b7-168">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de [*résolution*](r-gly.md)DNS.</span><span class="sxs-lookup"><span data-stu-id="752b7-168">Time, in seconds, that the RR can be cached by a DNS [*resolver*](r-gly.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="752b7-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="752b7-169">Requirements</span></span>



| <span data-ttu-id="752b7-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="752b7-170">Requirement</span></span> | <span data-ttu-id="752b7-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="752b7-171">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="752b7-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="752b7-172">Minimum supported client</span></span><br/> | <span data-ttu-id="752b7-173">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="752b7-173">None supported</span></span><br/>                                                              |
| <span data-ttu-id="752b7-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="752b7-174">Minimum supported server</span></span><br/> | <span data-ttu-id="752b7-175">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="752b7-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="752b7-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="752b7-176">Namespace</span></span><br/>                | <span data-ttu-id="752b7-177">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="752b7-177">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="752b7-178">MOF</span><span class="sxs-lookup"><span data-stu-id="752b7-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="752b7-179"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="752b7-179"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="752b7-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="752b7-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752b7-181">**Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="752b7-181">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[<span data-ttu-id="752b7-182">**Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="752b7-182">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





