---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_SIGType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource signature (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032481"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="ceef2-106">Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType</span><span class="sxs-lookup"><span data-stu-id="ceef2-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="ceef2-107">La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource signature (SIG).</span><span class="sxs-lookup"><span data-stu-id="ceef2-107">The **CreateInstanceFromPropertyData** method instantiates a Signature (SIG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceef2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ceef2-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ceef2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ceef2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceef2-110">*DnsServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-111">Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ceef2-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-112">*ContainerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-113">Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.</span><span class="sxs-lookup"><span data-stu-id="ceef2-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-114">*OwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-115">Nom du propriétaire de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ceef2-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-116">*RecordClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-117">Classe de l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ceef2-117">Class of the RR.</span></span> <span data-ttu-id="ceef2-118">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="ceef2-118">Default value is 1.</span></span> <span data-ttu-id="ceef2-119">Les valeurs suivantes sont valides.</span><span class="sxs-lookup"><span data-stu-id="ceef2-119">The following values are valid.</span></span>



| <span data-ttu-id="ceef2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceef2-120">Value</span></span>                                                                                                | <span data-ttu-id="ceef2-121">Signification</span><span class="sxs-lookup"><span data-stu-id="ceef2-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ceef2-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ceef2-123">DANS (Internet)</span><span class="sxs-lookup"><span data-stu-id="ceef2-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="ceef2-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ceef2-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="ceef2-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="ceef2-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ceef2-127">CH (CHAOS)</span><span class="sxs-lookup"><span data-stu-id="ceef2-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="ceef2-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ceef2-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="ceef2-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ceef2-130">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-131">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="ceef2-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-132">*TypeCovered* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-132">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-133">Type d’enregistrement de ressource couvert par ce SIG.</span><span class="sxs-lookup"><span data-stu-id="ceef2-133">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-134">*Algorithme* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-134">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-135">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="ceef2-135">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="ceef2-136">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ceef2-136">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="ceef2-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceef2-137">Value</span></span>                                                                                                | <span data-ttu-id="ceef2-138">Signification</span><span class="sxs-lookup"><span data-stu-id="ceef2-138">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="ceef2-139"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-139"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ceef2-140">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="ceef2-140">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="ceef2-141"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-141"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ceef2-142">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="ceef2-142">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="ceef2-143"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-143"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ceef2-144">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="ceef2-144">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="ceef2-145"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-145"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ceef2-146">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="ceef2-146">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ceef2-147">*Étiquettes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-147">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-148">Nombre non signé d’étiquettes dans le nom du propriétaire du RR SIG d’origine.</span><span class="sxs-lookup"><span data-stu-id="ceef2-148">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="ceef2-149">Le nombre n’inclut pas l’étiquette NULL pour la racine, ni les caractères génériques initiaux.</span><span class="sxs-lookup"><span data-stu-id="ceef2-149">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-150">*OriginalTTL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-150">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-151">TTL de l’ensemble de RR signé par SIG.</span><span class="sxs-lookup"><span data-stu-id="ceef2-151">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-152">*SignatureExpiration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-152">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-153">Date d’expiration de la signature, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="ceef2-153">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-154">*SignatureInception* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-154">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-155">Date et heure auxquelles la signature devient valide, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="ceef2-155">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-156">*KeyTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-156">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-157">Méthode utilisée pour choisir une clé qui vérifie un SIG.</span><span class="sxs-lookup"><span data-stu-id="ceef2-157">Method used to choose a key that verifies an SIG.</span></span> <span data-ttu-id="ceef2-158">Consultez RFC 2535, annexe C, pour connaître la méthode utilisée pour calculer un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="ceef2-158">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-159">*SignerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-159">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-160">Nom de domaine du signataire qui a généré le RR SIG.</span><span class="sxs-lookup"><span data-stu-id="ceef2-160">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-161">*Signature* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-161">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-162">Signature, représentée dans la base 64, mise en forme comme défini dans la RFC 2535, annexe A.</span><span class="sxs-lookup"><span data-stu-id="ceef2-162">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="ceef2-163">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-163">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ceef2-164">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="ceef2-164">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceef2-165">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ceef2-165">Return value</span></span>

<span data-ttu-id="ceef2-166">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ceef2-166">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceef2-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ceef2-167">Requirements</span></span>



| <span data-ttu-id="ceef2-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ceef2-168">Requirement</span></span> | <span data-ttu-id="ceef2-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceef2-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceef2-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceef2-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ceef2-171">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceef2-171">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ceef2-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ceef2-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ceef2-173">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ceef2-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ceef2-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ceef2-174">Namespace</span></span><br/>                | <span data-ttu-id="ceef2-175">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="ceef2-175">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ceef2-176">MOF</span><span class="sxs-lookup"><span data-stu-id="ceef2-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceef2-177"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceef2-177"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceef2-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ceef2-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceef2-179">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="ceef2-179">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="ceef2-180">**Modifier la méthode de la \_ classe SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="ceef2-180">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="ceef2-181">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="ceef2-181">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





