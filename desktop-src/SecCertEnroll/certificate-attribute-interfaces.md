---
description: Les interfaces suivantes peuvent être utilisées pour créer des attributs de certificat.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfaces d’attribut de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543662"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="cce19-103">Interfaces d’attribut de certificat</span><span class="sxs-lookup"><span data-stu-id="cce19-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="cce19-104">Les interfaces suivantes peuvent être utilisées pour créer des attributs de certificat.</span><span class="sxs-lookup"><span data-stu-id="cce19-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="cce19-105">Interface</span><span class="sxs-lookup"><span data-stu-id="cce19-105">Interface</span></span>                                                                    | <span data-ttu-id="cce19-106">Description</span><span class="sxs-lookup"><span data-stu-id="cce19-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cce19-107">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="cce19-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="cce19-108">Représente un attribut de chiffrement dans une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="cce19-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="cce19-109">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="cce19-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="cce19-110">Gère une collection d’objets [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="cce19-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="cce19-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="cce19-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="cce19-112">Représente un attribut dans une \# demande de certificat PKCS 7, PKCS \# 10 ou CMC.</span><span class="sxs-lookup"><span data-stu-id="cce19-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="cce19-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="cce19-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="cce19-114">Représente un attribut qui peut être utilisé pour identifier le client qui a généré une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="cce19-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="cce19-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="cce19-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="cce19-116">Représente les extensions de certificat dans une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="cce19-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="cce19-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="cce19-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="cce19-118">Représente un attribut qui contient une clé privée chiffrée à archiver par une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="cce19-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="cce19-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="cce19-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="cce19-120">Représente un attribut qui contient un hachage SHA-1 de la clé privée chiffrée à archiver par une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="cce19-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="cce19-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="cce19-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="cce19-122">Représente un attribut qui identifie le fournisseur de services de chiffrement utilisé par l’entité qui demande le certificat.</span><span class="sxs-lookup"><span data-stu-id="cce19-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="cce19-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="cce19-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="cce19-124">Représente un attribut qui contient des informations de version sur le système d’exploitation client sur lequel la demande de certificat a été générée.</span><span class="sxs-lookup"><span data-stu-id="cce19-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="cce19-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="cce19-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="cce19-126">Représente un attribut qui contient le certificat en cours de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="cce19-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="cce19-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="cce19-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="cce19-128">Gère une collection d’objets [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="cce19-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="cce19-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="cce19-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="cce19-130">Représente une paire nom-valeur générique.</span><span class="sxs-lookup"><span data-stu-id="cce19-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="cce19-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="cce19-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="cce19-132">Gère une collection d’objets [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="cce19-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="cce19-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cce19-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce19-134">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="cce19-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



