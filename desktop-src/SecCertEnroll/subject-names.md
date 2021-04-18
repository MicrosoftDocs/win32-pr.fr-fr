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
# <a name="subject-names"></a>Noms de sujets

Le champ **objet** d’une \# demande de certificat PKCS 10 contient le nom unique de l’entité demandant le certificat.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

Le nom unique est constitué d’une séquence de noms uniques relatifs (RDN). Chaque RDN se compose d’un ensemble d’attributs, et chaque attribut se compose d’un identificateur d’objet et d’une valeur. Le type de données de la valeur est identifié par la structure **DirectoryString** .

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

Pour plus d'informations, voir les rubriques suivantes :

-   [Création d’un nom d’objet](creating-a-subject-name.md)
-   [Encodage d’un nom de sujet](encoding-a-subject-name.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demandes](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
