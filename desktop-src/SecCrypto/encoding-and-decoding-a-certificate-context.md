---
description: Encodage et décodage d’un contexte de certificat à l’aide de CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Encodage et décodage d’un contexte de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201784"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Encodage et décodage d’un contexte de certificat

[*CryptoAPI*](../secgloss/c-gly.md) prend en charge l’encodage et le décodage des [*certificats*](../secgloss/c-gly.md). CryptoAPI comprend un système complet et flexible de fonctions et de structures C qui autorisent l’encodage et le décodage de différentes façons. CryptoAPI prend en charge la structure de certificat standard [*X. 509*](../secgloss/x-gly.md) et l’encodage ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ) pour assurer l’interopérabilité avec d’autres systèmes.

Pour obtenir une vue d’ensemble des données encodées, consultez [données encodées et décodées](encoded-and-decoded-data.md).

## <a name="certificate-contexts"></a>Contextes de certificat

Un [*contexte de certificat*](../secgloss/c-gly.md), un [**\_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)de certificat, est une structure C qui contient un membre encodé, un handle vers [*un magasin de certificats*](../secgloss/c-gly.md), un pointeur vers l' [*objet blob de certificat*](../secgloss/c-gly.md)encodé d’origine et un pointeur vers une structure d' [**\_ informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) de certificat C.

La structure des [**\_ informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) de certificat est le cœur du certificat. Il contient, sous forme directe et sous forme codée, toutes les informations de base du certificat. L’illustration suivante montre la structure des **\_ informations de certificat** avec tous ses membres encodés affichés comme étant ombrés.

![structure des informations de certificat \-](images/certinf2.png)

Les membres **IssuerUniqueID** et **SubjectUniqueID** font partie de l’implémentation du certificat [*X. 509*](../secgloss/x-gly.md) version 2, mais sont rarement utilisés. Les extensions de certificat dans la version 3 remplacent les fonctionnalités de ces membres.

Si les informations contenues dans l' **émetteur** et l' **objet** des membres encodés (ombrés) sont nécessaires, ces membres doivent être décodés. Utilisez [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) pour décoder ces membres. L’illustration suivante montre le processus de décodage de l’un de ces membres.

![décodage avec cryptdecodeobject](images/infoflow.png)

Dans le cas illustré, la fonction [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) crée une structure d' [**\_ \_ informations sur le nom du certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) , un tableau de structures de type [**\_ RDN**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) du certificat, un tableau correspondant de structures [**\_ \_ attr du RDN du certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) et une chaîne qui contient le nom. Les membres de la structure **\_ \_ attr** relative au RDN du certificat déterminent le contenu de la chaîne. Par exemple, si le membre **pszObjId** est 2.5.4.3, la chaîne contient un nom commun. S’il s’agit de 2.5.4.10, la chaîne contient un nom d’organisation. Pour obtenir la liste de ces [*identificateurs d’objet*](../secgloss/o-gly.md) (OID), consultez **CERT \_ RDN \_ attr**.

Le membre **dwValueType** contient des informations sur le type de chaîne. S’il s’agit \_ \_ d’une chaîne imprimable de certificat RDN imprimable \_ , le membre de valeur contient une chaîne de caractères de largeur octet, qui se termine par zéro. S’il s’agit \_ \_ d’une chaîne Unicode de certificat RDN \_ , la chaîne est une chaîne de caractères à double largeur (taille de texte).

Pour un processus détaillé d’encodage et de décodage des certificats, consultez [encodage d’une \_ structure d’informations de certificat](encoding-a-cert-info-structure.md) et [décodage d’une \_ structure d’informations de certificat](decoding-a-cert-info-structure.md).

 

 
