---
description: Validation de la chaîne de certificats
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Validation de la chaîne de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70a1dd3a09e46199cb537c1ac4b17cb96ed0edc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240588"
---
# <a name="validating-the-certificate-chain"></a>Validation de la chaîne de certificats

Cette rubrique explique comment valider la chaîne de certificats du pilote lors de l’utilisation du protocole COPP (Certified Output Protection Protocol).

La chaîne de certificats du pilote graphique est un document XML. La chaîne de certificats contient trois certificats. Le premier certificat est appelé le *certificat feuille*, et est le certificat Copp du pilote. Le certificat suivant est le certificat de signature du fournisseur de matériel indépendant (IHV). Le dernier certificat est le certificat de signature de Microsoft. Pour vous assurer que le pilote Graphics est un appareil COPP légitime, l’application doit valider les trois certificats. Un programme malveillant peut empêcher COPP de fonctionner si une application ne valide pas correctement les certificats dans la chaîne.

Les chaînes de certificats COPP utilisent le jeu de caractères UTF-8. Les données binaires dans les certificats, telles que la clé publique RSA, sont encodées en base64 et stockées dans l’ordre de primauté des octets de poids fort (Big endian). (*Big-endian* signifie que l’octet le plus significatif est stocké dans l’emplacement de mémoire avec l’adresse la plus basse.)

Certains éléments d’un certificat contiennent des valeurs booléennes pour indiquer qu’il existe une fonctionnalité du certificat. Si la fonctionnalité existe, la valeur de l’élément enfant correspondant est définie sur 1. Si une fonctionnalité n’est pas présente, cet élément enfant n’est pas présent dans le certificat.

### <a name="xml-element-definitions"></a>Définitions d’éléments XML

Voici les définitions des éléments du schéma de certificat :

-   **CertificateCollection**. Élément racine du document XML. Il contient des éléments de certificat, un pour chaque certificat de la chaîne.
-   **Certificat**. Contient un seul certificat. Cet élément contient des données et des éléments de signature.
-   **Data**. Contient des informations sur le certificat. En particulier, il contient la clé et le type publics du certificat. L’élément de données contient les éléments enfants suivants :
    -   **PublicKey**. Contient la clé publique RSA du certificat. L’élément PublicKey contient un élément KeyValue, qui contient un élément RSAKeyValue. L’élément RSAKeyValue possède deux éléments enfants, le modulo et l’exposant, et ceux-ci définissent la clé publique. Les éléments modulo et Exponent sont encodés en base64 et stockés dans l’ordre Big-endian.
    -   **Utilisation de KeyUsage**. Si le certificat est le certificat COPP du pilote, cet élément doit contenir un élément enfant appelé EncryptKey. Si le certificat est le certificat de signature du IHV ou le certificat de signature de Microsoft, il doit contenir un élément enfant appelé SignCertificate. Ces deux éléments enfants contiennent des valeurs booléennes.
    -   **SecurityLevel**. Cet élément doit être ignoré.
    -   **ManufacturerData**. Spécifie le fabricant et le modèle de l’appareil graphique. Cet élément est informatif uniquement.
    -   **Features**. Contient des éléments enfants qui spécifient l’utilisation du certificat. Le seul élément pertinent pour COPP est l’élément COPPCertificate. D’autres éléments enfants peuvent être présents ; dans ce cas, ils doivent être ignorés. Si l’élément COPPCertificate existe, le certificat est un certificat COPP. Cet élément doit être présent dans le nœud terminal d’un certificat COPP valide. Cet élément contient une valeur booléenne.
-   **Signature**. Contient la signature pour ce certificat. Il contient les éléments enfants suivants :
    -   **SignedInfo**. Contient des informations sur la signature. L’élément enfant important de cet élément est l’élément DigestValue, qui contient la valeur encodée en base64 du hachage SHA-1 sur l’élément de données. La valeur Digest est utilisée lors de la vérification du certificat par rapport à la liste de révocation de certificats (CRL).
    -   **SignatureValue**. Cette valeur est calculée à partir de l’élément de données et est calculée selon le schéma de signature numérique RSASSA-PSS défini dans Public-Key Cryptography Standards (PKCS) \# 1 (version 2,1). Pour plus d’informations sur PKCS \# 1, visitez [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Contient la clé publique RSA du certificat suivant dans la chaîne. Cet élément est utilisé pour vérifier que les données de l’élément de données n’ont pas été falsifiées. Cet élément a le même format que l’élément PublicKey.

### <a name="certificate-validation"></a>Validation de certificat

L’application doit effectuer les étapes suivantes pour valider correctement la chaîne de certificats. Si une étape échoue, ou si un élément référencé dans ces procédures n’existe pas, la validation échoue.

### <a name="validate-certificate-collection-procedure"></a>Procédure valider la collecte des certificats

Pour valider la chaîne de certificats, procédez comme suit :

1.  Vérifiez que le code XML CertificateCollection est bien formé.
2.  Vérifiez que CertificateCollection est encodé au format UTF-8.
3.  Vérifiez que l’attribut version de l’élément CertificateCollection est 2,0 ou une version ultérieure.
4.  Vérifiez que la chaîne de certificats contient exactement trois éléments de certificat.
5.  Parcourez chaque élément de certificat de la chaîne de certificats et exécutez la procédure valider le certificat, décrite ci-dessous, sur chacun d’eux.

### <a name="validate-certificate-procedure"></a>Procédure valider le certificat

Pour valider un certificat dans la chaîne, procédez comme suit :

1.  Vérifiez qu’aucun des éléments enfants de l’élément de données n’est dupliqué. Par exemple, il ne doit y avoir qu’un seul élément PublicKey.
2.  Assurez-vous que l’élément Data/PublicKey/KeyValue/RSAKeyValue/modulo existe. La valeur décodée en base64 doit avoir une longueur de 256 octets pour tous les certificats, à l’exception de la racine. Dans le certificat racine, cet élément doit avoir une longueur de 128 octets.
3.  Assurez-vous que l’élément Data/PublicKey/KeyValue/RSAKeyValue/Exponent existe. La valeur décodée en base64 ne doit pas être supérieure à 4 octets.
4.  Si ce certificat est le certificat feuille, vérifiez les éléments suivants :
    -   L’élément KeyUsage contient un élément EncryptKey avec la valeur 1.
    -   L’élément features contient un élément COPPCertificate avec la valeur 1.
5.  Si ce certificat n’est pas le certificat feuille, vérifiez les éléments suivants :
    -   Le modulo et l’exposant de l’élément Data/PublicKey correspondent exactement au modulo et à l’exposant de l’élément signature/KeyInfo du certificat précédent.
    -   L’élément KeyUsage contient un élément SignCertificate, avec la valeur 1.
6.  Utilisez l’algorithme de hachage SHA-1 pour hacher chaque octet dans l’élément de données du certificat. Chaque octet du premier caractère de la &lt; &gt; balise de données jusqu’au dernier caractère de la &lt; balise de fermeture/Data &gt; doit être haché. La valeur de hachage est utilisée pour vérifier le certificat par rapport à la liste de révocation de certificats, comme décrit dans [listes de révocation de certificats](certificate-revocation-lists.md) .
7.  Comparez la valeur de hachage de l’étape 6 à la valeur décodée en base64 de l’élément signature/SignedInfo/Reference/DigestValue. Ces valeurs doivent correspondre.
8.  Effectuez la procédure de vérification de la signature, décrite ci-dessous.
9.  Si ce certificat n’est pas le certificat final dans la chaîne, enregistrez la valeur de signature/KeyInfo/KeyValue/RSAKeyValue pour la prochaine itération de la boucle.
10. Si ce certificat est le certificat final dans la chaîne, assurez-vous que la valeur de signature/KeyInfo/KeyValue/RSAKeyValue correspond à la clé publique de Microsoft. La clé publique Microsoft a les valeurs encodées en base64 suivantes :
    -   Young

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Positifs `AQAB`

### <a name="verify-signature-procedure"></a>Vérifier la procédure de signature

La valeur de l’élément SignatureValue est calculée sur l’élément de données en fonction du schéma de signature numérique RSASSA-PSS défini dans la \# version 2,1 de PKCS 1 (ci-après, appelée PKCS). Pour vérifier cette signature, procédez comme suit :

1.  Décodez les valeurs du modulo et de l’exposant dans l’élément signature/KeyInfo/KeyValue/RSAKeyValue. Ces valeurs définissent la clé publique RSA du certificat de signature.
2.  Décodez l’élément signature/SignatureValue.
3.  Calculez l’opération RSASSA-PSS-Verify, définie dans la section 8.1.2 de PKCS.

Pour l’opération RSASSA-PSS-Verify, utilisez les entrées suivantes :

-   (*n*,*e*) est la clé publique de l’étape 1.
-   *M* correspond à tous les octets de l’élément de données, y compris les &lt; &gt; balises de données et de &lt; /Data &gt; qui encadrent l’élément.
-   *S* est la valeur de signature décodée de l’étape 2.

L’opération RSASSA-PSS-Verify utilise l’opération EMSA-PSS-ENCODE, définie dans la section 9.1.1. de PKCS. Pour cette opération, COPP utilise les options suivantes :

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (fonction de génération de masque) = MGF1
-   *sLen* = 0

La fonction de génération de masque MGF1 est définie dans l’annexe B. 2 de PKCS. Pour cette fonction, COPP utilise les options suivantes :

-   Hash = SHA-1
-   *hLen* = 20

La sortie de l’opération RSASSA-PSS-Verify indique si la signature est valide ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



