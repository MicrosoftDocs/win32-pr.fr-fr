---
title: Modifier la méthode de la classe MicrosoftDNS_SIGType
description: La méthode modify met à jour une ressource de signature (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464526"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a><span data-ttu-id="d2dcc-106">Modifier la méthode de la \_ classe SIGType MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="d2dcc-106">Modify method of the MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="d2dcc-107">La méthode **Modify** met à jour une ressource de signature (SIG).</span><span class="sxs-lookup"><span data-stu-id="d2dcc-107">The **Modify** method updates a Signature (SIG) RR.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2dcc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2dcc-108">Syntax</span></span>


```mof
void Modify(
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



## <a name="parameters"></a><span data-ttu-id="d2dcc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2dcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2dcc-110">*TTL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-111">Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-112">*TypeCovered* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-112">*TypeCovered* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-113">Type d’enregistrement de ressource couvert par ce SIG.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-113">Type of RR covered by this SIG.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-114">*Algorithme* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-114">*Algorithm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-115">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-115">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="d2dcc-116">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-116">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="d2dcc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2dcc-117">Value</span></span>                                                                                                | <span data-ttu-id="d2dcc-118">Signification</span><span class="sxs-lookup"><span data-stu-id="d2dcc-118">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d2dcc-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d2dcc-119"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d2dcc-120">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="d2dcc-120">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="d2dcc-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d2dcc-121"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d2dcc-122">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="d2dcc-122">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="d2dcc-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d2dcc-123"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d2dcc-124">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="d2dcc-124">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="d2dcc-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d2dcc-125"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d2dcc-126">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="d2dcc-126">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2dcc-127">*Étiquettes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-127">*Labels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-128">Nombre non signé d’étiquettes dans le nom du propriétaire du RR SIG d’origine.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-128">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="d2dcc-129">Le nombre n’inclut pas l’étiquette NULL pour la racine, ni les caractères génériques initiaux.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-129">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-130">*OriginalTTL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-130">*OriginalTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-131">TTL de l’ensemble de RR signé par SIG.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-131">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-132">*SignatureExpiration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-132">*SignatureExpiration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-133">Date d’expiration de la signature, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-133">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-134">*SignatureInception* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-134">*SignatureInception* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-135">Date et heure auxquelles la signature devient valide, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-135">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-136">*KeyTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-136">*KeyTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-137">Méthode utilisée pour choisir une clé qui vérifie un SIG.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-137">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="d2dcc-138">Consultez RFC 2535, annexe C, pour connaître la méthode utilisée pour calculer un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-138">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-139">*SignerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-139">*SignerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-140">Nom de domaine du signataire qui a généré le RR SIG.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-140">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-141">*Signature* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-141">*Signature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-142">Signature, représentée dans la base 64, mise en forme comme défini dans la RFC 2535, annexe A.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-142">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="d2dcc-143">*RR* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-143">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dcc-144">Référence au nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-144">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2dcc-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2dcc-145">Return value</span></span>

<span data-ttu-id="d2dcc-146">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2dcc-147">Notes</span><span class="sxs-lookup"><span data-stu-id="d2dcc-147">Remarks</span></span>

<span data-ttu-id="d2dcc-148">Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.</span><span class="sxs-lookup"><span data-stu-id="d2dcc-148">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2dcc-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2dcc-149">Requirements</span></span>



| <span data-ttu-id="d2dcc-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2dcc-150">Requirement</span></span> | <span data-ttu-id="d2dcc-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2dcc-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2dcc-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2dcc-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d2dcc-153">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2dcc-153">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d2dcc-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2dcc-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d2dcc-155">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2dcc-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d2dcc-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d2dcc-156">Namespace</span></span><br/>                | <span data-ttu-id="d2dcc-157">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="d2dcc-157">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d2dcc-158">MOF</span><span class="sxs-lookup"><span data-stu-id="d2dcc-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2dcc-159"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2dcc-159"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2dcc-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2dcc-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2dcc-161">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="d2dcc-161">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)
</dt> <dt>

[<span data-ttu-id="d2dcc-162">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="d2dcc-162">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d2dcc-163">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="d2dcc-163">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





