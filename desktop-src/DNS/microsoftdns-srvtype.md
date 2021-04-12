---
title: Classe MicrosoftDNS_SRVType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de service (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType de la classe DNS
- MicrosoftDNS_SRVType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465674"
---
# <a name="microsoftdns_srvtype-class"></a><span data-ttu-id="6202c-105">MicrosoftDNS \_ SRVType, classe</span><span class="sxs-lookup"><span data-stu-id="6202c-105">MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="6202c-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de service (SRV).</span><span class="sxs-lookup"><span data-stu-id="6202c-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Service (SRV) record.</span></span>

<span data-ttu-id="6202c-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="6202c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6202c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6202c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a><span data-ttu-id="6202c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6202c-109">Members</span></span>

<span data-ttu-id="6202c-110">La classe **MicrosoftDNS \_ SRVType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6202c-110">The **MicrosoftDNS\_SRVType** class has these types of members:</span></span>

-   [<span data-ttu-id="6202c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6202c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6202c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6202c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6202c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6202c-113">Methods</span></span>

<span data-ttu-id="6202c-114">La classe **MicrosoftDNS \_ SRVType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6202c-114">The **MicrosoftDNS\_SRVType** class has these methods.</span></span>



| <span data-ttu-id="6202c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="6202c-115">Method</span></span>                             | <span data-ttu-id="6202c-116">Description</span><span class="sxs-lookup"><span data-stu-id="6202c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6202c-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6202c-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="6202c-118">Instancie un type SRV de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le propriétaire/nom de la cible, la classe (valeur par défaut = IN), la valeur de durée de vie et la priorité, le poids, le port et le nom de domaine de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="6202c-118">Instantiates an SRV Type of RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner/target Name, class (default = IN), time-to-live value, and target host's priority, weight, port, and domain name.</span></span> <span data-ttu-id="6202c-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="6202c-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="6202c-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="6202c-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="6202c-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="6202c-121">**Modify**</span></span>                         | <span data-ttu-id="6202c-122">Met à jour la durée de vie, la priorité, le poids, le port et le nom de domaine selon les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6202c-122">Updates the TTL, Priority, Weight, Port, and Domain Name to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="6202c-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="6202c-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="6202c-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="6202c-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="6202c-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="6202c-125">Qualifiers: Implemented</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="6202c-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6202c-126">Properties</span></span>

<span data-ttu-id="6202c-127">La classe **MicrosoftDNS \_ SRVType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6202c-127">The **MicrosoftDNS\_SRVType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6202c-128">**Port**</span><span class="sxs-lookup"><span data-stu-id="6202c-128">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202c-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6202c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6202c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6202c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6202c-131">Port utilisé sur l’hôte cible d’un service de protocole.</span><span class="sxs-lookup"><span data-stu-id="6202c-131">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="6202c-132">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6202c-132">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202c-133">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6202c-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6202c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6202c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6202c-135">Priorité de l’hôte cible spécifiée dans le nom du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="6202c-135">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="6202c-136">Les nombres inférieurs impliquent des priorités plus élevées.</span><span class="sxs-lookup"><span data-stu-id="6202c-136">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="6202c-137">**SRVDomainName**</span><span class="sxs-lookup"><span data-stu-id="6202c-137">**SRVDomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202c-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6202c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6202c-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6202c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6202c-140">Nom de domaine complet de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="6202c-140">FQDN of the target host.</span></span> <span data-ttu-id="6202c-141">Une cible de \\ . \\ signifie que le service n’est pas disponible dans ce domaine.</span><span class="sxs-lookup"><span data-stu-id="6202c-141">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="6202c-142">**Poids**</span><span class="sxs-lookup"><span data-stu-id="6202c-142">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6202c-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6202c-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6202c-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6202c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6202c-145">Poids de l’hôte cible.</span><span class="sxs-lookup"><span data-stu-id="6202c-145">Weight of the target host.</span></span> <span data-ttu-id="6202c-146">Cela est utile lorsque vous sélectionnez parmi les hôtes qui ont la même priorité.</span><span class="sxs-lookup"><span data-stu-id="6202c-146">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="6202c-147">La probabilité d’utiliser cet hôte doit être proportionnelle à son poids.</span><span class="sxs-lookup"><span data-stu-id="6202c-147">The chances of using this host should be proportional to its weight.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6202c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6202c-148">Requirements</span></span>



| <span data-ttu-id="6202c-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6202c-149">Requirement</span></span> | <span data-ttu-id="6202c-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="6202c-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6202c-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6202c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6202c-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6202c-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6202c-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6202c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6202c-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6202c-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6202c-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6202c-155">Namespace</span></span><br/>                | <span data-ttu-id="6202c-156">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="6202c-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="6202c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="6202c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6202c-158"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6202c-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6202c-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6202c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6202c-160">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SRVType**</span><span class="sxs-lookup"><span data-stu-id="6202c-160">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="6202c-161">**Modifier la méthode de la \_ classe SRVType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="6202c-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="6202c-162">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="6202c-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





