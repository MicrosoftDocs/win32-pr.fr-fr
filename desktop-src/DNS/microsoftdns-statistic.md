---
title: Classe MicrosoftDNS_Statistic
description: La \_ classe statistique MicrosoftDNS représente une statistique de serveur DNS unique.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic de la classe DNS
- MicrosoftDNS_Statistic de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033136"
---
# <a name="microsoftdns_statistic-class"></a><span data-ttu-id="5f45c-105">\_Classe de statistiques MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="5f45c-105">MicrosoftDNS\_Statistic class</span></span>

<span data-ttu-id="5f45c-106">La **classe \_ statistique MicrosoftDNS** représente une statistique de serveur DNS unique.</span><span class="sxs-lookup"><span data-stu-id="5f45c-106">The **MicrosoftDNS\_Statistic** class represents a single DNS Server statistic.</span></span>

<span data-ttu-id="5f45c-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="5f45c-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f45c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f45c-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a><span data-ttu-id="5f45c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5f45c-109">Members</span></span>

<span data-ttu-id="5f45c-110">La **classe \_ statistique MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5f45c-110">The **MicrosoftDNS\_Statistic** class has these types of members:</span></span>

-   [<span data-ttu-id="5f45c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f45c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f45c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f45c-112">Properties</span></span>

<span data-ttu-id="5f45c-113">La **classe \_ statistique MicrosoftDNS** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5f45c-113">The **MicrosoftDNS\_Statistic** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f45c-114">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="5f45c-114">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f45c-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-117">Représentation numérique de **CollectionName**.</span><span class="sxs-lookup"><span data-stu-id="5f45c-117">Numeric representation of **CollectionName**.</span></span>

</dd> <dt>

<span data-ttu-id="5f45c-118">**CollectionName**</span><span class="sxs-lookup"><span data-stu-id="5f45c-118">**CollectionName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f45c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-121">Nom de la collection à laquelle la statistique appartient.</span><span class="sxs-lookup"><span data-stu-id="5f45c-121">Name of the collection to which the statistic belongs.</span></span>

</dd> <dt>

<span data-ttu-id="5f45c-122">**DnsServerName**</span><span class="sxs-lookup"><span data-stu-id="5f45c-122">**DnsServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f45c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-125">Indique le nom de domaine complet ou l’adresse IP du serveur DNS qui contient la statistique.</span><span class="sxs-lookup"><span data-stu-id="5f45c-125">Indicates the FQDN or IP address of the DNS Server that contains the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="5f45c-126">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5f45c-126">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f45c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-129">Nom de la statistique.</span><span class="sxs-lookup"><span data-stu-id="5f45c-129">Name of the statistic.</span></span>

</dd> <dt>

<span data-ttu-id="5f45c-130">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="5f45c-130">**StringValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5f45c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-133">Valeur de chaîne de la statistique, utilisée uniquement lorsque la valeur de statistique n’est pas représentée comme une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="5f45c-133">String value of the statistic, used only when the statistic value is not represented as a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="5f45c-134">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5f45c-134">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f45c-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f45c-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f45c-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5f45c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f45c-137">Valeur numérique de la statistique, représentée sous la forme d’un DWORD.</span><span class="sxs-lookup"><span data-stu-id="5f45c-137">Numeric value of the statistic, represented as a DWORD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f45c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f45c-138">Requirements</span></span>



| <span data-ttu-id="5f45c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f45c-139">Requirement</span></span> | <span data-ttu-id="5f45c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f45c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f45c-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f45c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5f45c-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f45c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5f45c-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f45c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5f45c-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f45c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5f45c-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f45c-145">Namespace</span></span><br/>                | <span data-ttu-id="5f45c-146">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="5f45c-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5f45c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="5f45c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f45c-148"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f45c-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f45c-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f45c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f45c-150">MicrosoftDNS \_ StatisticCollection</span><span class="sxs-lookup"><span data-stu-id="5f45c-150">MicrosoftDNS\_StatisticCollection</span></span>](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





