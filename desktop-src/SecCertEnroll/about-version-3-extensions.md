---
description: Un certificat X.509 version 3 contient les champs définis dans les versions 1 et 2 et ajoute des extensions de certificat. La syntaxe ASN. 1 des extensions de certificat est présentée dans l’exemple suivant.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensions de la version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202837"
---
# <a name="version-3-extensions"></a><span data-ttu-id="006f4-104">Extensions de la version 3</span><span class="sxs-lookup"><span data-stu-id="006f4-104">Version 3 Extensions</span></span>

<span data-ttu-id="006f4-105">Un certificat X.509 version 3 contient les champs définis dans les versions 1 et 2 et ajoute des extensions de certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="006f4-106">La syntaxe ASN. 1 des extensions de certificat est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="006f4-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="006f4-107">Les extensions standard version 3 et leurs identificateurs d’objet (OID) sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="006f4-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="006f4-108">Microsoft les prend en charge et comprend des extensions personnalisées supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="006f4-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="006f4-109">Pour plus d’informations, consultez [Extensions](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="006f4-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="006f4-110">Extension</span><span class="sxs-lookup"><span data-stu-id="006f4-110">Extension</span></span>                                         | <span data-ttu-id="006f4-111">Description</span><span class="sxs-lookup"><span data-stu-id="006f4-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006f4-112">Identificateur de clé de l’autorité (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="006f4-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="006f4-113">Identifie la clé publique de l’autorité de certification qui correspond à la clé privée de l’autorité de certification utilisée pour signer le certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="006f4-114">Contraintes de base (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="006f4-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="006f4-115">Indique si l’entité peut être utilisée en tant qu’autorité de certification et, le cas échéant, le nombre d’autorités de certification secondaires pouvant exister en dessous dans la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="006f4-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="006f4-116">Stratégies de certificat (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="006f4-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="006f4-117">Indique les stratégies sous lesquelles le certificat a été émis et les fins auxquelles il peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="006f4-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="006f4-118">Points de distribution de liste de révocation de certificats (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="006f4-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="006f4-119">Contient l’URI de la [*liste de révocation de certificats*](/windows/desktop/SecGloss/c-gly) de base.</span><span class="sxs-lookup"><span data-stu-id="006f4-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="006f4-120">Utilisation améliorée de la clé (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="006f4-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="006f4-121">Indique la façon dont la clé publique contenue dans le certificat peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="006f4-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="006f4-122">Autre nom de l’émetteur (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="006f4-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="006f4-123">Indique un ou plusieurs autres noms pour l’émetteur de la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="006f4-124">Utilisation de la clé (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="006f4-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="006f4-125">Indique des restrictions sur les opérations pouvant être effectuées par la clé publique contenue dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="006f4-126">Contraintes de nom (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="006f4-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="006f4-127">Indique l’espace de noms dans lequel tous les noms de sujets d’une hiérarchie de certificats doivent se trouver.</span><span class="sxs-lookup"><span data-stu-id="006f4-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="006f4-128">L’extension n’est utilisée que dans un certificat d’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="006f4-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="006f4-129">Contraintes de stratégie (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="006f4-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="006f4-130">Contraint la validation du chemin d’accès en interdisant le mappage de stratégie ou en exigeant que tous les certificats de la hiérarchie contiennent un identificateur de stratégie acceptable.</span><span class="sxs-lookup"><span data-stu-id="006f4-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="006f4-131">L’extension n’est utilisée que dans un certificat d’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="006f4-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="006f4-132">Mappages de stratégie (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="006f4-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="006f4-133">Indique les stratégies dans une autorité de certification secondaire qui correspondent aux stratégies dans l’autorité de certification émettrice.</span><span class="sxs-lookup"><span data-stu-id="006f4-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="006f4-134">Période d’utilisation de la clé privée (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="006f4-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="006f4-135">Indique une durée de validité pour la clé privée qui est différente de celle du certificat auquel la clé privée est associée.</span><span class="sxs-lookup"><span data-stu-id="006f4-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="006f4-136">Autre nom de l’objet (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="006f4-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="006f4-137">Indique une ou plusieurs autres formes de noms pour le sujet de la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="006f4-138">Parmi les autres formes, citons : adresses de messagerie, noms DNS, adresses IP et URI.</span><span class="sxs-lookup"><span data-stu-id="006f4-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="006f4-139">Attributs du répertoire du sujet (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="006f4-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="006f4-140">Véhicule des attributs d’identification tels que la nationalité du sujet du certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="006f4-141">La valeur de l’extension est une séquence de paires OID-valeur.</span><span class="sxs-lookup"><span data-stu-id="006f4-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="006f4-142">Identificateur de la clé du sujet (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="006f4-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="006f4-143">Fait la distinction entre plusieurs clés publiques détenues par le sujet du certificat.</span><span class="sxs-lookup"><span data-stu-id="006f4-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="006f4-144">La valeur de l’extension est généralement un hachage SHA-1 de la clé.</span><span class="sxs-lookup"><span data-stu-id="006f4-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="006f4-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="006f4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="006f4-146">Champs de base</span><span class="sxs-lookup"><span data-stu-id="006f4-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="006f4-147">Champs de la version 2</span><span class="sxs-lookup"><span data-stu-id="006f4-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="006f4-148">Certificats de clé publique X. 509</span><span class="sxs-lookup"><span data-stu-id="006f4-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

