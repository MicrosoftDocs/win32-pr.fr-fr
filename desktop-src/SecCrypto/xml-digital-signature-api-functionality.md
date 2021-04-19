---
description: CryptXML fournit un ensemble d’API de bas niveau qui permet aux applications de créer et de vérifier des signatures enveloppes, enveloppantes et détachées. Vous pouvez utiliser CryptXML pour créer et vérifier le contenu stocké dans les éléments d’objet de signature, y compris les manifestes.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Fonctionnalité de l’API de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534292"
---
# <a name="xml-digital-signature-api-functionality"></a>Fonctionnalité de l’API de signature numérique XML

CryptXML fournit un ensemble d’API de bas niveau qui permet aux applications de créer et de vérifier des signatures enveloppes, enveloppantes et détachées. Vous pouvez utiliser CryptXML pour créer et vérifier le contenu stocké dans les éléments d’objet de signature, y compris les manifestes. Une clé publique/privée, une clé partagée ou un certificat [*X. 509*](../secgloss/x-gly.md) ou une chaîne de certificats peuvent être utilisés pour signer et vérifier la [*signature numérique*](../secgloss/d-gly.md)XML.

Les applications qui utilisent CryptXML pour vérifier les références externes (références qui ciblent un document ou un fichier externe en dehors du contexte du document) doivent résoudre les URI externes et récupérer les données à déchiffrer.

Pour plus d’informations sur les algorithmes de chiffrement pris en charge par CryptXML, consultez [algorithmes de chiffrement de signature numérique XML](xml-digital-signature-cryptographic-algorithms.md).

CryptXML fournit la prise en charge des algorithmes de canonisation avec les identificateurs suivants.



| Constante                                              | Valeur URI                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| wszURI \_ canonicalisation, \_ C14N<br/>             | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315"<br/>               |
| wszURI \_ Canonicalization \_ C14NC<br/>            | "https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"<br/> |
| wszURI \_ canonisation \_ EXSLUSIVE \_ C14N<br/>  | "https://www.w3.org/2001/10/xml-exc-c14n\#"<br/>                      |
| wszURI \_ Canonicalization \_ EXSLUSIVE \_ C14NC<br/> | "https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"<br/>          |



 

CryptXML fournit la prise en charge de la transformation de signature enveloppée.



| Constante                                       | Valeur URI                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| wszURI \_ xmlns \_ Transform \_ envelopped<br/> | "https://www.w3.org/2000/09/xmldsig\#enveloped-signature"<br/> |



 

Par défaut, CryptXML ne prend pas en charge les transformations XPath ou XSLT. Si nécessaire, les applications peuvent implémenter ces transformations par-dessus CryptXML.

 

 
