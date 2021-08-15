---
description: CryptXML prend en charge en mode natif les URI listés ci-dessous.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algorithmes de chiffrement de signature numérique XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290be3708565cf144b5bf23bfcb1ddfe5252b227c12bbcebbd81b68d0fc2df07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895784"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a>Algorithmes de chiffrement de signature numérique XML

CryptXML prend en charge en mode natif les URI listés ci-dessous. Si la prise en charge est requise pour les algorithmes de chiffrement et les transformations qui ne font pas partie de la prise en charge native, vous pouvez utiliser l' [API de chiffrement :](../seccng/cng-portal.md) [extensions de chiffrement de signature numérique](xml-digital-signature-cryptographic-extensions.md) nouvelle génération et XML pour prendre en charge de nouveaux algorithmes.

## <a name="supported-uris"></a>URI pris en charge

Méthodes Digest



| Constante                                 | Valeur URI                                                   |
|------------------------------------------|-------------------------------------------------------------|
| wszURI \_ xmlns \_ DIGSIG \_ SHA1<br/>   | "https://www.w3.org/2000/09/xmldsig\#sha1"<br/>        |
| wszURI \_ xmlns \_ DIGSIG \_ SHA256<br/> | "https://www.w3.org/2001/04/xmlenc\#sha256"<br/>       |
| wszURI \_ xmlns \_ DIGSIG \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#sha384"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ SHA512<br/> | "https://www.w3.org/2001/04/xmlenc\#sha512"<br/>       |



 

Méthodes de signature



| Constante                                        | Valeur URI                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| wszURI \_ xmlns \_ DIGSIG- \_ RSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#rsa-sha1"<br/>          |
| wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1<br/>     | "https://www.w3.org/2000/09/xmldsig\#dsa-sha1"<br/>          |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA384<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1<br/>   | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"<br/>   |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA384<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512<br/> | "https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"<br/> |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1<br/>    | "https://www.w3.org/2000/09/xmldsig\#hmac-sha1"<br/>         |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"<br/>  |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA384<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"<br/>  |
| wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512<br/>  | "https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"<br/>  |



 

 

 
