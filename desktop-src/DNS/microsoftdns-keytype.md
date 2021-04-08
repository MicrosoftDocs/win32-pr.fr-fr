---
title: Classe MicrosoftDNS_KEYType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de clé.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- MicrosoftDNS_KEYType de la classe DNS
- MicrosoftDNS_KEYType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1e814af1d22820f1722e5812dd314dd1c7f6e0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843774"
---
# <a name="microsoftdns_keytype-class"></a><span data-ttu-id="1c0b6-105">\_Classe KeyType de MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="1c0b6-105">MicrosoftDNS\_KEYType class</span></span>

<span data-ttu-id="1c0b6-106">Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de clé.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-106">The subclass of [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) that represents a KEY Resource Record.</span></span>

<span data-ttu-id="1c0b6-107">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c0b6-108">Syntax</span></span>

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a><span data-ttu-id="1c0b6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1c0b6-109">Members</span></span>

<span data-ttu-id="1c0b6-110">La classe de **\_ KeyType de MicrosoftDNS** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c0b6-110">The **MicrosoftDNS\_KEYType** class has these types of members:</span></span>

-   [<span data-ttu-id="1c0b6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1c0b6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c0b6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c0b6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c0b6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1c0b6-113">Methods</span></span>

<span data-ttu-id="1c0b6-114">La classe de **\_ KeyType de MicrosoftDNS** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-114">The **MicrosoftDNS\_KEYType** class has these methods.</span></span>



| <span data-ttu-id="1c0b6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="1c0b6-115">Method</span></span>                             | <span data-ttu-id="1c0b6-116">Description</span><span class="sxs-lookup"><span data-stu-id="1c0b6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0b6-117">**CreateInstanceFromPropertyData**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-117">**CreateInstanceFromPropertyData**</span></span> | <span data-ttu-id="1c0b6-118">Instancie un enregistrement de ressource clé en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai d’attente de la recherche inversée, le délai d’expiration du cache WINS et le nom de</span><span class="sxs-lookup"><span data-stu-id="1c0b6-118">Instantiates a KEY Resource Record based on the data in the method's input parameters: the record's DNS Server Name, Container Name, Owner Name, class (default = IN), time-to-live value, and WINS mapping flag, reverse look-up time out, WINS cache time out and domain name to append.</span></span> <span data-ttu-id="1c0b6-119">Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-119">It returns a reference to the new object as an output parameter.</span></span> <br/> <span data-ttu-id="1c0b6-120">Qualificateurs : implémentés, statiques</span><span class="sxs-lookup"><span data-stu-id="1c0b6-120">Qualifiers: Implemented, static</span></span><br/> |
| <span data-ttu-id="1c0b6-121">**Modify**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-121">**Modify**</span></span>                         | <span data-ttu-id="1c0b6-122">Met à jour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et le domaine de résultat sur les valeurs spécifiées comme paramètres d’entrée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-122">Updates the TTL, mapping flag, look-up time out, cache time out, and result domain to the values specified as the input parameters of this method.</span></span> <span data-ttu-id="1c0b6-123">Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-123">If a new value for a parameter is not specified, then the current value for the parameter is not changed.</span></span> <span data-ttu-id="1c0b6-124">La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-124">The method returns a reference to the modified object as an output parameter.</span></span> <br/> <span data-ttu-id="1c0b6-125">Qualificateurs : implémentés</span><span class="sxs-lookup"><span data-stu-id="1c0b6-125">Qualifiers: Implemented</span></span><br/>                          |



 

### <a name="properties"></a><span data-ttu-id="1c0b6-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1c0b6-126">Properties</span></span>

<span data-ttu-id="1c0b6-127">La classe de **\_ KeyType de MicrosoftDNS** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-127">The **MicrosoftDNS\_KEYType** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c0b6-128">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-128">**Algorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0b6-129">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0b6-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c0b6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0b6-131">Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-131">Algorithm used with the key specified in the resource record.</span></span> <span data-ttu-id="1c0b6-132">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-132">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="1c0b6-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0b6-133">Value</span></span>                                                                                                | <span data-ttu-id="1c0b6-134">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0b6-134">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1c0b6-135"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-135"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1c0b6-136">RSA/MD5 (RFC 2537)</span><span class="sxs-lookup"><span data-stu-id="1c0b6-136">RSA/MD5 (RFC 2537)</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="1c0b6-137"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-137"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1c0b6-138">Diffie-Hellman (RFC 2539)</span><span class="sxs-lookup"><span data-stu-id="1c0b6-138">Diffie-Hellman (RFC 2539)</span></span><br/>   |
| <span id="3"></span><dl> <span data-ttu-id="1c0b6-139"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-139"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1c0b6-140">DSA (RFC 2536)</span><span class="sxs-lookup"><span data-stu-id="1c0b6-140">DSA (RFC 2536)</span></span><br/>              |
| <span id="4"></span><dl> <span data-ttu-id="1c0b6-141"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-141"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1c0b6-142">Chiffrement à courbe elliptique</span><span class="sxs-lookup"><span data-stu-id="1c0b6-142">Elliptic curve cryptography</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1c0b6-143">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-143">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0b6-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0b6-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c0b6-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0b6-146">Indicateurs utilisés pour spécifier le mappage, comme décrit dans la norme IETF RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-146">Flags used to specify mapping, as described in IETF RFC 2535.</span></span>

</dd> <dt>

<span data-ttu-id="1c0b6-147">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-147">**Protocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0b6-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c0b6-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c0b6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0b6-150">Protocole pour lequel la clé spécifiée dans l’enregistrement de ressource peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-150">Protocol for which the key specified in the resource record can be used.</span></span> <span data-ttu-id="1c0b6-151">Les valeurs affectées sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-151">The assigned values are shown in the following table.</span></span>



| <span data-ttu-id="1c0b6-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0b6-152">Value</span></span>                                                                                                    | <span data-ttu-id="1c0b6-153">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0b6-153">Meaning</span></span>                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="1c0b6-154"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-154"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="1c0b6-155">TLS</span><span class="sxs-lookup"><span data-stu-id="1c0b6-155">TLS</span></span><br/>           |
| <span id="2"></span><dl> <span data-ttu-id="1c0b6-156"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-156"><dt>**2**</dt></span></span> </dl>     | <span data-ttu-id="1c0b6-157">Courrier électronique</span><span class="sxs-lookup"><span data-stu-id="1c0b6-157">E-Mail</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="1c0b6-158"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-158"><dt>**3**</dt></span></span> </dl>     | <span data-ttu-id="1c0b6-159">DNSSEC</span><span class="sxs-lookup"><span data-stu-id="1c0b6-159">DNSSEC</span></span><br/>        |
| <span id="4"></span><dl> <span data-ttu-id="1c0b6-160"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-160"><dt>**4**</dt></span></span> </dl>     | <span data-ttu-id="1c0b6-161">IPsec</span><span class="sxs-lookup"><span data-stu-id="1c0b6-161">IPsec</span></span><br/>         |
| <span id="255"></span><dl> <span data-ttu-id="1c0b6-162"><dt>**255**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-162"><dt>**255**</dt></span></span> </dl> | <span data-ttu-id="1c0b6-163">Tous les protocoles</span><span class="sxs-lookup"><span data-stu-id="1c0b6-163">All protocols</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1c0b6-164">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-164">**PublicKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c0b6-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c0b6-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1c0b6-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c0b6-167">Clé publique, représentée dans la base 64, comme décrit dans l’annexe A de la RFC 2535.</span><span class="sxs-lookup"><span data-stu-id="1c0b6-167">Public key, represented in base 64 as described in Appendix A of RFC 2535.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c0b6-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c0b6-168">Requirements</span></span>



| <span data-ttu-id="1c0b6-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c0b6-169">Requirement</span></span> | <span data-ttu-id="1c0b6-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0b6-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0b6-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0b6-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0b6-172">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0b6-172">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1c0b6-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0b6-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0b6-174">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c0b6-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c0b6-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1c0b6-175">Namespace</span></span><br/>                | <span data-ttu-id="1c0b6-176">\\MicrosoftDNS racine</span><span class="sxs-lookup"><span data-stu-id="1c0b6-176">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="1c0b6-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1c0b6-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c0b6-178"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c0b6-178"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0b6-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c0b6-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c0b6-180">**Méthode CreateInstanceFromPropertyData de la \_ classe KeyType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-180">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="1c0b6-181">**Modify, méthode de la \_ classe KeyType de MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-181">**Modify Method of the MicrosoftDNS\_KEYType Class**</span></span>](microsoftdns-keytype-modify.md)
</dt> <dt>

[<span data-ttu-id="1c0b6-182">**MicrosoftDNS \_ ResourceRecord**</span><span class="sxs-lookup"><span data-stu-id="1c0b6-182">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





