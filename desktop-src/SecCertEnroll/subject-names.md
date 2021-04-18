---
description: Le champ objet d’une \# demande de certificat PKCS 10 contient le nom unique de l’entité demandant le certificat.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Noms de sujets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526137"
---
# <a name="subject-names"></a><span data-ttu-id="08645-103">Noms de sujets</span><span class="sxs-lookup"><span data-stu-id="08645-103">Subject Names</span></span>

<span data-ttu-id="08645-104">Le champ **objet** d’une \# demande de certificat PKCS 10 contient le nom unique de l’entité demandant le certificat.</span><span class="sxs-lookup"><span data-stu-id="08645-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="08645-105">Le nom unique est constitué d’une séquence de noms uniques relatifs (RDN).</span><span class="sxs-lookup"><span data-stu-id="08645-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="08645-106">Chaque RDN se compose d’un ensemble d’attributs, et chaque attribut se compose d’un identificateur d’objet et d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="08645-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="08645-107">Le type de données de la valeur est identifié par la structure **DirectoryString** .</span><span class="sxs-lookup"><span data-stu-id="08645-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="08645-108">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="08645-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="08645-109">Création d’un nom d’objet</span><span class="sxs-lookup"><span data-stu-id="08645-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="08645-110">Encodage d’un nom de sujet</span><span class="sxs-lookup"><span data-stu-id="08645-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="08645-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08645-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08645-112">Demandes</span><span class="sxs-lookup"><span data-stu-id="08645-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
