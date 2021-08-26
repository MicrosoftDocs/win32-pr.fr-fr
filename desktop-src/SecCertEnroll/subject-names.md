---
description: Le champ objet d’une \# demande de certificat PKCS 10 contient le nom unique de l’entité demandant le certificat.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Noms de sujets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101099"
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

 

 
