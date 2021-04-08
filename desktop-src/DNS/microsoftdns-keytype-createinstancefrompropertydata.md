---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_KEYType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource clé.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16dc8f3f591ba3aaf5ac9883cdd3a15c85146d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033227"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="69d4e-106">Méthode CreateInstanceFromPropertyData de la \_ classe KeyType de MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="69d4e-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="69d4e-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource clé.</span><span class="sxs-lookup"><span data-stu-id="69d4e-107">The **CreateInstanceFromPropertyData** method instantiates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d4e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69d4e-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="69d4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69d4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d4e-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="69d4e-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="69d4e-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="69d4e-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="69d4e-117">Class of the RR.</span></span> <span data-ttu-id="69d4e-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="69d4e-118">Default value is 1.</span></span> <span data-ttu-id="69d4e-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="69d4e-119">The following values are valid.</span></span>



| <span data-ttu-id="69d4e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="69d4e-120">Value</span></span>                                                                                                | <span data-ttu-id="69d4e-121">Signification</span><span class="sxs-lookup"><span data-stu-id="69d4e-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="69d4e-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="69d4e-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="69d4e-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="69d4e-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="69d4e-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="69d4e-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="69d4e-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="69d4e-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="69d4e-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="69d4e-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="69d4e-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="69d4e-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="69d4e-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="69d4e-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-132">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-132">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-133">Indicateurs utilisés pour spécifier le mappage, comme décrit dans la norme IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="69d4e-133">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-134">*Protocole* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-134">*Protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-135">Protocole pour lequel la clé spécifiée dans l’enregistrement de ressource peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="69d4e-135">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="69d4e-136">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69d4e-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="69d4e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="69d4e-137">Value</span></span>                                                                                                    | <span data-ttu-id="69d4e-138">Signification</span><span class="sxs-lookup"><span data-stu-id="69d4e-138">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="69d4e-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-139"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="69d4e-140">TLS</span><span class="sxs-lookup"><span data-stu-id="69d4e-140">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="69d4e-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-141"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="69d4e-142">Courrier électronique</span><span class="sxs-lookup"><span data-stu-id="69d4e-142">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="69d4e-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-143"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="69d4e-144">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="69d4e-144">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="69d4e-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-145"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="69d4e-146">IPsec</span><span class="sxs-lookup"><span data-stu-id="69d4e-146">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="69d4e-147"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-147"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="69d4e-148">Tous les protocoles</span><span class="sxs-lookup"><span data-stu-id="69d4e-148">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="69d4e-149">*Algorithme* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-149">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-150">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="69d4e-150">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="69d4e-151">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69d4e-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="69d4e-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="69d4e-152">Value</span></span>                                                                                                | <span data-ttu-id="69d4e-153">Signification</span><span class="sxs-lookup"><span data-stu-id="69d4e-153">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="69d4e-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-154"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="69d4e-155">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="69d4e-155">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="69d4e-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-156"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="69d4e-157">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="69d4e-157">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="69d4e-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-158"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="69d4e-159">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="69d4e-159">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="69d4e-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-160"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="69d4e-161">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="69d4e-161">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="69d4e-162">*PublicKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-162">*PublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-163">Clé publique, représentée dans la base 64, comme décrit dans l’annexe A de la RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="69d4e-163">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="69d4e-164">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-164">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-165">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="69d4e-165">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d4e-166">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69d4e-166">Return value</span></span>

<span data-ttu-id="69d4e-167">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="69d4e-167">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d4e-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69d4e-168">Requirements</span></span>



| <span data-ttu-id="69d4e-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69d4e-169">Requirement</span></span> | <span data-ttu-id="69d4e-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="69d4e-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69d4e-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69d4e-171">Minimum supported client</span></span><br/> | <span data-ttu-id="69d4e-172">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="69d4e-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="69d4e-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69d4e-173">Minimum supported server</span></span><br/> | <span data-ttu-id="69d4e-174">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69d4e-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69d4e-175">Namespace</span></span><br/>                | <span data-ttu-id="69d4e-176">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="69d4e-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="69d4e-177">MOF</span><span class="sxs-lookup"><span data-stu-id="69d4e-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69d4e-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d4e-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69d4e-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d4e-180">**MicrosoftDNS, \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="69d4e-180">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="69d4e-181">**Modify, méthode de la \_ classe KeyType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="69d4e-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="69d4e-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="69d4e-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





