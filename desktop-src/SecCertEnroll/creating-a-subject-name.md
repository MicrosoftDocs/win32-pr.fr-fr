---
description: Vous pouvez utiliser l’interface IX500DistinguishedName pour créer un nom d’objet à partir d’une chaîne de nom unique.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Création d’un nom d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525096"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="a8ac6-103">Création d’un nom d’objet</span><span class="sxs-lookup"><span data-stu-id="a8ac6-103">Creating a Subject Name</span></span>

<span data-ttu-id="a8ac6-104">Vous pouvez utiliser l’interface [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) pour créer un nom d’objet à partir d’une chaîne de nom unique.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="a8ac6-105">La chaîne se compose de noms uniques relatifs concaténés (RDN).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="a8ac6-106">Les clés RDN suivantes sont prises en charge par l’API d’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="a8ac6-107">Clé</span><span class="sxs-lookup"><span data-stu-id="a8ac6-107">Key</span></span>                               | <span data-ttu-id="a8ac6-108">OID</span><span class="sxs-lookup"><span data-stu-id="a8ac6-108">OID</span></span>                                             | <span data-ttu-id="a8ac6-109">Description</span><span class="sxs-lookup"><span data-stu-id="a8ac6-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ac6-110">C</span><span class="sxs-lookup"><span data-stu-id="a8ac6-110">C</span></span><br/>                      | <span data-ttu-id="a8ac6-111">nom du pays de l' \_ OID XCN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="a8ac6-112">Contient un code de pays ou de région ISO 3166 à deux lettres.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="a8ac6-113">CN</span><span class="sxs-lookup"><span data-stu-id="a8ac6-113">CN</span></span><br/>                     | <span data-ttu-id="a8ac6-114">\_ \_ nom commun de l’OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="a8ac6-115">Contient un nom commun.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="a8ac6-116">E</span><span class="sxs-lookup"><span data-stu-id="a8ac6-116">E</span></span><br/> <span data-ttu-id="a8ac6-117">Messagerie</span><span class="sxs-lookup"><span data-stu-id="a8ac6-117">EMAIL</span></span><br/>     | <span data-ttu-id="a8ac6-118">XCN \_ OID \_ RSA \_ emailaddr</span><span class="sxs-lookup"><span data-stu-id="a8ac6-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="a8ac6-119">Contient une adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="a8ac6-120">DC</span><span class="sxs-lookup"><span data-stu-id="a8ac6-120">DC</span></span><br/>                     | <span data-ttu-id="a8ac6-121">\_composant de \_ domaine XCN OID \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="a8ac6-122">Contient une partie d’un nom DNS (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="a8ac6-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="a8ac6-123">G</span><span class="sxs-lookup"><span data-stu-id="a8ac6-123">G</span></span><br/> <span data-ttu-id="a8ac6-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="a8ac6-124">GivenName</span></span><br/> | <span data-ttu-id="a8ac6-125">nom d’XCN \_ OID \_ donné \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="a8ac6-126">Contient la partie du nom d’une personne qui n’est pas un nom de famille.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="a8ac6-127">I</span><span class="sxs-lookup"><span data-stu-id="a8ac6-127">I</span></span><br/>                      | <span data-ttu-id="a8ac6-128">\_initiales OID \_ XCN</span><span class="sxs-lookup"><span data-stu-id="a8ac6-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="a8ac6-129">Contient les initiales d’une personne.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="a8ac6-130">L</span><span class="sxs-lookup"><span data-stu-id="a8ac6-130">L</span></span><br/>                      | <span data-ttu-id="a8ac6-131">nom de la localité de l' \_ OID XCN \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="a8ac6-132">Contient le nom de la localité qui identifie une ville, un pays ou une autre région géographique.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="a8ac6-133">O</span><span class="sxs-lookup"><span data-stu-id="a8ac6-133">O</span></span><br/>                      | <span data-ttu-id="a8ac6-134">nom de l' \_ organisation XCN OID \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="a8ac6-135">Contient le nom d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="a8ac6-136">OU</span><span class="sxs-lookup"><span data-stu-id="a8ac6-136">OU</span></span><br/>                     | <span data-ttu-id="a8ac6-137">nom de l' \_ \_ unité d’organisation XCN OID \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="a8ac6-138">Contient le nom d’une sous-division d’unité au sein d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="a8ac6-139">S</span><span class="sxs-lookup"><span data-stu-id="a8ac6-139">S</span></span><br/> <span data-ttu-id="a8ac6-140">ST</span><span class="sxs-lookup"><span data-stu-id="a8ac6-140">ST</span></span><br/>        | <span data-ttu-id="a8ac6-141">\_ \_ état \_ ou nom de la \_ province \_ XCN OID</span><span class="sxs-lookup"><span data-stu-id="a8ac6-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="a8ac6-142">Contient le nom complet d’un État ou d’une province.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="a8ac6-143">STREET</span><span class="sxs-lookup"><span data-stu-id="a8ac6-143">STREET</span></span><br/>                 | <span data-ttu-id="a8ac6-144">\_ \_ adresse postale de l’OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="a8ac6-145">Contient l’adresse physique.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="a8ac6-146">SN</span><span class="sxs-lookup"><span data-stu-id="a8ac6-146">SN</span></span><br/>                     | <span data-ttu-id="a8ac6-147">XCN \_ OID sur le \_ \_ nom</span><span class="sxs-lookup"><span data-stu-id="a8ac6-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="a8ac6-148">Contient le nom de famille d’une personne.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="a8ac6-149">T</span><span class="sxs-lookup"><span data-stu-id="a8ac6-149">T</span></span><br/> <span data-ttu-id="a8ac6-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="a8ac6-150">TITLE</span></span><br/>     | <span data-ttu-id="a8ac6-151">titre de l' \_ OID XCN \_</span><span class="sxs-lookup"><span data-stu-id="a8ac6-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="a8ac6-152">Contient le titre d’une personne de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="a8ac6-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="a8ac6-153">Lorsque vous initialisez un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , vous pouvez identifier le format du nom unique en spécifiant une valeur à partir du type d’énumération [**l x500nameflags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) .</span><span class="sxs-lookup"><span data-stu-id="a8ac6-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="a8ac6-154">Par exemple, supposons que le nom unique du sujet se compose des noms de RDN suivants :</span><span class="sxs-lookup"><span data-stu-id="a8ac6-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="a8ac6-155">CN = administrateur</span><span class="sxs-lookup"><span data-stu-id="a8ac6-155">CN=Administrator</span></span>  
<span data-ttu-id="a8ac6-156">CN = utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a8ac6-156">CN=Users</span></span>  
<span data-ttu-id="a8ac6-157">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="a8ac6-157">DC=jdomcsc</span></span>  
<span data-ttu-id="a8ac6-158">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="a8ac6-158">DC=nttest</span></span>  
<span data-ttu-id="a8ac6-159">DC = Microsoft</span><span class="sxs-lookup"><span data-stu-id="a8ac6-159">DC=microsoft</span></span>  
<span data-ttu-id="a8ac6-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="a8ac6-160">DC=com</span></span>  
</dl>

<span data-ttu-id="a8ac6-161">Si vous concaténez ces RDN dans la chaîne de nom unique délimitée par des virgules suivante, vous pouvez spécifier la valeur de l’indicateur de la **virgule de nom de \_ certificat XCN \_ \_ Str \_ \_** lors de l’initialisation d’un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .</span><span class="sxs-lookup"><span data-stu-id="a8ac6-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="a8ac6-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8ac6-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ac6-163">Encodage d’un nom de sujet</span><span class="sxs-lookup"><span data-stu-id="a8ac6-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="a8ac6-164">Noms de sujets</span><span class="sxs-lookup"><span data-stu-id="a8ac6-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




