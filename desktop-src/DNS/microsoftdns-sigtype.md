---
title: Classe MicrosoftDNS_SIGType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de signature (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType de la classe DNS
- MicrosoftDNS_SIGType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740261"
---
# <a name="microsoftdns_sigtype-class"></a><span data-ttu-id="17113-105">MicrosoftDNS \_ SIGType, classe</span><span class="sxs-lookup"><span data-stu-id="17113-105">MicrosoftDNS\_SIGType class</span></span>

<span data-ttu-id="17113-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de signature (SIG).</span><span class="sxs-lookup"><span data-stu-id="17113-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a Signature (SIG) Resource Record.</span></span>

<span data-ttu-id="17113-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="17113-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="17113-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17113-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a><span data-ttu-id="17113-109">Membres</span><span class="sxs-lookup"><span data-stu-id="17113-109">Members</span></span>

<span data-ttu-id="17113-110">La classe **MicrosoftDNS \_ SIGType** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17113-110">The **MicrosoftDNS\_SIGType** class has these types of members:</span></span>

-   [<span data-ttu-id="17113-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17113-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="17113-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17113-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17113-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17113-113">Methods</span></span>

<span data-ttu-id="17113-114">La classe **MicrosoftDNS \_ SIGType** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="17113-114">The **MicrosoftDNS\_SIGType** class has these methods.</span></span>



| <span data-ttu-id="17113-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="17113-115">Method</span></span>                             | <span data-ttu-id="17113-116">Description</span><span class="sxs-lookup"><span data-stu-id="17113-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17113-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="17113-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="17113-118">Instancie un RR SIG basé sur les données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai de recherche inverse, le délai d’expiration du cache WINS et le nom de domaine à ajouter</span><span class="sxs-lookup"><span data-stu-id="17113-118">Instantiates an SIG RR based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="17113-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="17113-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="17113-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="17113-120">Qualifiers: Implemented, static</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="17113-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="17113-121">**Modify**</span></span>                         | <span data-ttu-id="17113-122">Met à jour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et le domaine de résultat sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="17113-122">Updates the TTL, Mapping Flag, Look-up Time out, Cache Time out and Result Domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="17113-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="17113-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="17113-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="17113-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="17113-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="17113-125">Qualifiers: Implemented</span></span><br/> <span data-ttu-id="17113-126">**Windows Server 2003 :** Cette méthode met également à jour l’TypeCovered, l’algorithme, les étiquettes, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName et la signature avec les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="17113-126">**Windows Server 2003:** This method also updates the TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName and Signature to the values specified as the input parameters of this method.</span></span><br/> <br/> |



 

### <a name="properties"></a><span data-ttu-id="17113-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17113-127">Properties</span></span>

<span data-ttu-id="17113-128">La classe **MicrosoftDNS \_ SIGType** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="17113-128">The **MicrosoftDNS\_SIGType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17113-129">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="17113-129">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17113-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17113-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-132">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="17113-132">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="17113-133">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="17113-133">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="17113-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="17113-134">Value</span></span>                                                                                                | <span data-ttu-id="17113-135">Signification</span><span class="sxs-lookup"><span data-stu-id="17113-135">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="17113-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="17113-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="17113-137">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="17113-137">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="17113-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="17113-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="17113-139">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="17113-139">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="17113-140"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="17113-140"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="17113-141">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="17113-141">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="17113-142"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="17113-142"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="17113-143">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="17113-143">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="17113-144">**KeyTag**</span><span class="sxs-lookup"><span data-stu-id="17113-144">**KeyTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17113-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17113-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-147">Méthode utilisée pour choisir une clé qui vérifie un SIG.</span><span class="sxs-lookup"><span data-stu-id="17113-147">Method used to choose a key that verifies a SIG.</span></span> <span data-ttu-id="17113-148">Consultez RFC 2535, annexe C, pour connaître la méthode utilisée pour calculer un KeyTag.</span><span class="sxs-lookup"><span data-stu-id="17113-148">See RFC 2535, Appendix C for the method used to calculate a KeyTag.</span></span>

</dd> <dt>

<span data-ttu-id="17113-149">**Étiquettes**</span><span class="sxs-lookup"><span data-stu-id="17113-149">**Labels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17113-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17113-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-152">Nombre non signé d’étiquettes dans le nom du propriétaire du RR SIG d’origine.</span><span class="sxs-lookup"><span data-stu-id="17113-152">Unsigned count of labels in the original SIG RR owner name.</span></span> <span data-ttu-id="17113-153">Le nombre n’inclut pas l’étiquette NULL pour la racine, ni les caractères génériques initiaux.</span><span class="sxs-lookup"><span data-stu-id="17113-153">The count does not include the NULL label for the root, nor any initial wildcards.</span></span>

</dd> <dt>

<span data-ttu-id="17113-154">**OriginalTTL**</span><span class="sxs-lookup"><span data-stu-id="17113-154">**OriginalTTL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17113-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17113-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-157">TTL de l’ensemble de RR signé par SIG.</span><span class="sxs-lookup"><span data-stu-id="17113-157">TTL of the RR set signed by the SIG.</span></span>

</dd> <dt>

<span data-ttu-id="17113-158">**Signature**</span><span class="sxs-lookup"><span data-stu-id="17113-158">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17113-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17113-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-161">Signature, représentée dans la base 64, mise en forme comme défini dans la RFC 2535, annexe A.</span><span class="sxs-lookup"><span data-stu-id="17113-161">Signature, represented in base 64, formatted as defined in RFC 2535, Appendix A.</span></span>

</dd> <dt>

<span data-ttu-id="17113-162">**SignatureExpiration**</span><span class="sxs-lookup"><span data-stu-id="17113-162">**SignatureExpiration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17113-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17113-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-165">Date d’expiration de la signature, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="17113-165">Signature expiration date, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="17113-166">**SignatureInception**</span><span class="sxs-lookup"><span data-stu-id="17113-166">**SignatureInception**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17113-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17113-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-169">Date et heure auxquelles la signature devient valide, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.</span><span class="sxs-lookup"><span data-stu-id="17113-169">Date and time at which the Signature becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.</span></span>

</dd> <dt>

<span data-ttu-id="17113-170">**SignerName**</span><span class="sxs-lookup"><span data-stu-id="17113-170">**SignerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="17113-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17113-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-173">Nom de domaine du signataire qui a généré le RR SIG.</span><span class="sxs-lookup"><span data-stu-id="17113-173">Domain name of the signer that generated the SIG RR.</span></span>

</dd> <dt>

<span data-ttu-id="17113-174">**TypeCovered**</span><span class="sxs-lookup"><span data-stu-id="17113-174">**TypeCovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17113-175">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17113-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17113-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17113-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17113-177">Type d’enregistrement de ressource couvert par ce SIG.</span><span class="sxs-lookup"><span data-stu-id="17113-177">Type of RR covered by this SIG.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17113-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17113-178">Requirements</span></span>



| <span data-ttu-id="17113-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17113-179">Requirement</span></span> | <span data-ttu-id="17113-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="17113-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17113-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17113-181">Minimum supported client</span></span><br/> | <span data-ttu-id="17113-182">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="17113-182">None supported</span></span><br/>                                                              |
| <span data-ttu-id="17113-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17113-183">Minimum supported server</span></span><br/> | <span data-ttu-id="17113-184">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17113-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="17113-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="17113-185">Namespace</span></span><br/>                | <span data-ttu-id="17113-186">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="17113-186">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="17113-187">MOF</span><span class="sxs-lookup"><span data-stu-id="17113-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17113-188"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17113-188"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17113-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17113-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17113-190">**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType**</span><span class="sxs-lookup"><span data-stu-id="17113-190">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="17113-191">**Modifier la méthode de la \_ classe SIGType MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="17113-191">**Modify Method of the MicrosoftDNS\_SIGType Class**</span></span>](microsoftdns-sigtype-modify.md)
</dt> <dt>

[<span data-ttu-id="17113-192">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="17113-192">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





