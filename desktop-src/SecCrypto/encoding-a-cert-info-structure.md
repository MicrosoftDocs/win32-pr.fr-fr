---
description: Le processus d’encodage est l’inverse du processus de décodage décrit dans décoder une structure d’informations de certificat \_ .
ms.assetid: 5d3311e5-a2fb-46f7-aa76-f232b39b34fd
title: Encodage d’une structure CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645a1d3054546a7b11c57d4f515dc7d3e26b5fe0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416450"
---
# <a name="encoding-a-cert_info-structure"></a>Encodage d’une structure d’informations de certificat \_

Le processus d’encodage est l’inverse du processus de décodage décrit dans [décoder une \_ structure d’informations de certificat](decoding-a-cert-info-structure.md). Par exemple, la procédure suivante ajoute un **émetteur** encodé à une structure d’informations de [**certificat \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . Consultez également l’illustration qui suit la procédure.

**Pour ajouter un émetteur encodé à une structure d’informations de certificat \_**

1.  Créez une chaîne contenant le nom de l’émetteur à utiliser.
2.  Créez un tableau de [**structures \_ \_ attr RDN de CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) , qui seront initialisées pour contenir les informations appropriées sur la chaîne de nom d’émetteur que vous venez de créer.
3.  Créez un tableau de structures de compte [**\_ RDN de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , dont l’une contient les informations sur le tableau de structures [**\_ \_ attr RDN de CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) qui vient d’être initialisé.
4.  Créez une structure d' [**\_ \_ informations de nom de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) qui a un pointeur vers le tableau de structures de nom [**\_ RDN de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) que vous venez de créer.
5.  Appelez [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) pour connaître la taille de l’objet BLOB encodé de sortie, en lui transmettant l’adresse de la structure d' [**\_ \_ informations du nom de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) que vous venez de créer.
6.  Allouez de la mémoire pour l’objet BLOB encodé de sortie.
7.  Appelez à nouveau [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , en lui transmettant les mêmes informations, mais en lui transmettant à présent l’adresse de la mémoire qui vient d’être allouée.
8.  Définissez le membre **Issuer. cbData** de la structure des [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) sur la taille retournée à l’étape 5 et le membre **émetteur. pbData** sur l’adresse obtenue à l’étape 6. L’objet blob d' **émetteur** encodé se trouve maintenant ici.

![Ajout d’un émetteur encodé à une structure d’informations de certificat \-](images/encflow.png)

Pour initialiser et encoder certaines informations d’extension de certificat, utilisez la procédure suivante. Consultez également l’illustration qui suit la procédure.

**Pour ajouter des informations d’extension encodées à une structure d’informations de certificat \_**

1.  Créer et initialiser une structure d’informations d’extension : pour cet exemple, il s’agit d’une structure d’informations de [**\_ contraintes de base \_ \_ CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) .
2.  Appelez [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject), en lui transmettant l’adresse de la structure que vous venez de créer, pour connaître la taille de l’objet BLOB encodé de sortie.
3.  Allouez de la mémoire pour l’objet BLOB encodé de sortie.
4.  Appelez à nouveau [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) , en passant les mêmes informations, à l’exception de Pass à présent dans l’adresse de la mémoire allouée.
5.  Créez un tableau de structures d' [**\_ extension de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .
6.  Initialisez une des structures [**d' \_ extension du certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) afin que **pszObjId** soit la chaîne appropriée pour les données contenues dans la **valeur**, et cette **valeur** contient l’objet blob de données chiffrées qui a été généré à partir de l’appel à [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject).
7.  Initialisez le membre **rgExtension** de la structure d' [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) pour qu’il pointe vers le tableau de structures d' [**\_ extension de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) .

![Ajout d’informations d’extension encodées à une structure d’informations de certificat \-](images/xtenflow.png)

 

 



