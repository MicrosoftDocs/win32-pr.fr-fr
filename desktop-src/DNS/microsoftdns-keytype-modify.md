---
title: Modifier la méthode de la classe MicrosoftDNS_KEYType
description: La méthode modify met à jour un enregistrement de ressource clé.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ee9182925f3f1d53fb90a4beefeb421f01c24f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106126"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a><span data-ttu-id="c2744-106">Modify, méthode de la \_ classe KeyType de MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="c2744-106">Modify method of the MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="c2744-107">La méthode **Modify** met à jour un enregistrement de ressource clé.</span><span class="sxs-lookup"><span data-stu-id="c2744-107">The **Modify** method updates a KEY Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2744-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2744-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c2744-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2744-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2744-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2744-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="c2744-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c2744-112">*Indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2744-112">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-113">Indicateurs utilisés pour spécifier le mappage, comme décrit dans la norme IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="c2744-113">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="c2744-114">*Protocole* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2744-114">*Protocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-115">Protocole pour lequel la clé spécifiée dans le RR peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c2744-115">Protocol for which the key specified in the RR can be used.</span></span> <span data-ttu-id="c2744-116">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c2744-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="c2744-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2744-117">Value</span></span>                                                                                                    | <span data-ttu-id="c2744-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c2744-118">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c2744-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-119"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="c2744-120">TLS</span><span class="sxs-lookup"><span data-stu-id="c2744-120">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="c2744-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-121"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="c2744-122">Courrier électronique</span><span class="sxs-lookup"><span data-stu-id="c2744-122">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="c2744-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-123"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="c2744-124">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="c2744-124">dnssec</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="c2744-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-125"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="c2744-126">IPsec</span><span class="sxs-lookup"><span data-stu-id="c2744-126">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="c2744-127"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-127"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="c2744-128">Tous les protocoles</span><span class="sxs-lookup"><span data-stu-id="c2744-128">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c2744-129">*Algorithme* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2744-129">*Algorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-130">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="c2744-130">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="c2744-131">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c2744-131">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="c2744-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2744-132">Value</span></span>                                                                                                | <span data-ttu-id="c2744-133">Signification</span><span class="sxs-lookup"><span data-stu-id="c2744-133">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c2744-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c2744-135">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="c2744-135">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="c2744-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c2744-137">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="c2744-137">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="c2744-138"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-138"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c2744-139">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="c2744-139">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="c2744-140"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-140"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c2744-141">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="c2744-141">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c2744-142">*PublicKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c2744-142">*PublicKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-143">Clé publique, représentée dans la base 64, comme décrit dans l’annexe A de la RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="c2744-143">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="c2744-144">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c2744-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c2744-145">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="c2744-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2744-146">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2744-146">Return value</span></span>

<span data-ttu-id="c2744-147">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c2744-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2744-148">Notes</span><span class="sxs-lookup"><span data-stu-id="c2744-148">Remarks</span></span>

<span data-ttu-id="c2744-149">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="c2744-149">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2744-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2744-150">Requirements</span></span>



| <span data-ttu-id="c2744-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2744-151">Requirement</span></span> | <span data-ttu-id="c2744-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2744-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2744-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2744-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c2744-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2744-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c2744-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2744-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c2744-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2744-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2744-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2744-157">Namespace</span></span><br/>                | <span data-ttu-id="c2744-158">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="c2744-158">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c2744-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c2744-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2744-160"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2744-160"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2744-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2744-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2744-162">**MicrosoftDNS, \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="c2744-162">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)
</dt> <dt>

[<span data-ttu-id="c2744-163">**Méthode CreateInstanceFromPropertyData de la \_ classe KeyType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="c2744-163">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="c2744-164">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="c2744-164">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





