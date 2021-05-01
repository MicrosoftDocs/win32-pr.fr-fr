---
description: L’horodatage Authenticode est basé sur les contre- \# signatures PKCS 7 standard. Les outils de signature de Microsoft permettent aux développeurs d’apposer des horodatages en même temps qu’ils apposeront des signatures Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Horodatage des signatures Authenticode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0232853441d2c11d331c175ac7e8dfd120b341ff
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327184"
---
# <a name="time-stamping-authenticode-signatures"></a>Horodatage des signatures Authenticode

Les signatures Microsoft Authenticode fournissent des garanties en matière d’autorisation et d’intégrité pour les données binaires. L’horodatage Authenticode est basé sur les contre- \# signatures PKCS 7 standard. Les outils de signature de Microsoft permettent aux développeurs d’apposer des horodatages en même temps qu’ils apposeront des signatures Authenticode. L’horodatage permet de vérifier la validité des signatures Authenticode même après l’expiration des certificats utilisés pour la signature.

## <a name="a-brief-introduction-to-authenticode"></a>Brève présentation d’Authenticode

[*Authenticode*](../secgloss/a-gly.md) applique la technologie de signature numérique pour garantir la création et l’intégrité des données binaires telles que les logiciels installables. Un navigateur Web client ou d’autres composants système peuvent utiliser les signatures Authenticode pour vérifier l’intégrité des données lors du téléchargement ou de l’installation du logiciel. Les signatures Authenticode peuvent être utilisées avec de nombreux formats de logiciel, notamment. cab,. exe,. ocx et. dll.

Microsoft gère une liste d' [*autorités de certification*](/security/trusted-root/participants-list) publiques (ca). Les émetteurs de certificats Authenticode incluent actuellement [SSL.com](https://www.ssl.com/), [DigiCert](https://www.digicert.com/), [Sectigo (Comodo)](https://www.sectigo.com/)et [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>À propos de l’horodatage de chiffrement

Par le passé, une variété de méthodes d’horodatage de chiffrement ont été proposées. Consultez, par exemple, Haber et Stornetta « Guide pratique pour Time-Stamp un document numérique » dans le *Journal de Cryptology* (1991) et Benaloh et de la prémare « cumuls à sens unique : une alternative décentralisée aux signatures numériques » dans *Springer Link-Verlag des notes de cours en informatique* vol. 765 (EUROCRYPT» 93). Un résumé étendu de cet article est disponible auprès de [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a). (Ces ressources peuvent ne pas être disponibles dans certaines langues et pays ou régions.) Étant donné que le temps est un physique, plutôt qu’une quantité mathématique, ces méthodes concernent généralement la façon de lier des objets afin que leur ordre de création puisse être déterminé ou comment regrouper efficacement des objets qui peuvent tous être décrits comme ayant été créés simultanément.

Les systèmes qui prétendent le temps d’authentification en tant que quantité nécessitent toujours une certaine forme de confiance. Dans un paramètre fortement conflictuelle, les protocoles complexes peuvent être utilisés pour garantir un certain degré de synchronisés. Toutefois, ces protocoles nécessitent une interaction complète entre les parties concernées. Dans la pratique, si vous avez uniquement besoin de la certification du temps d’une source approuvée, la source peut tout simplement agir comme un notaire en fournissant une instruction signée (certification) à laquelle l’objet a été présenté pour la signature à l’heure indiquée.

La méthode contre-signature d’horodatage implémentée ci-dessous permet de vérifier les signatures même après l’expiration ou la révocation du certificat de signature. L’horodatage permet au vérificateur de connaître de manière fiable l’heure à laquelle la signature a été apposée et de faire confiance à la signature si elle était valide à ce moment-là. La matrice temporelle doit avoir une source de temps fiable et protégée.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>\#Documents et contre-signatures PKCS 7 signés

PKCS \# 7 est un format standard pour les données de chiffrement, y compris les données signées, les certificats et les [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL). Le \# type d’intérêt PKCS 7 particulier dans le contexte de l’horodatage est les données signées, correspondant au \# type de contenu [**SIGNEDDATA**](signeddata.md) défini par PKCS 7.

Le \# package PKCS 7 comprend des [**SignedData**](signeddata.md) qui identifient le contenu réel et certaines informations à son sujet, ainsi que des blocs de signature signataires. Un signataires peut lui-même contenir une contre-signature, qui est, de manière récursive, un autre signataires. En principe, une séquence de ces contre-signatures peut être présente. La contre-signature est un attribut non authentifié par rapport à la signature dans le signataires ; autrement dit, il peut être apposé après la signature d’origine. Sous forme de plan :

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Version (de PKCS \# 7, en général version 1)
-   DigestAlgorithms (collection de tous les algorithmes utilisés par les blocs de signature signataires, pour un traitement optimisé)
-   ContentInfo (contentType est égal à [**SignedData**](signeddata.md), plus contenu ou référence au contenu)
-   Certificats FACULTATIFs (collection de tous les certificats utilisés)
-   Listes CRL FACULTATIVEs (regroupement de toutes les listes de révocation de certificats)
-   Signataires des blocs de signature (la signature réelle, composée d’un ou de plusieurs blocs de signature signataires)

Signataires (le bloc de signature)

-   Version (de PKCS \# 7, en général version 1)
-   Certificat (émetteur et numéro de série pour identifier de manière unique le certificat du signataire dans [**SignedData**](signeddata.md))
-   DigestAlgorithm plus le DigestEncryptionAlgorithm plus le Digest (hachage), plus le EncryptedDigest (signature réelle)
-   AuthenticatedAttributes facultatif (par exemple, signé par ce signataire)
-   UnauthenticatedAttributes facultatif (par exemple, non signé par ce signataire)

Un exemple d’attribut authentifié est le temps de signature (OID 1.2.840.113549.1.9.5), car il fait partie de ce que le service d’horodatage signe. La contre-signature (OID 1.2.840.113549.1.9.6) est un exemple d’attribut non authentifié, car elle peut être apposée après la signature. Dans ce cas, le signataires lui-même contient un signataires (la contre-signature).

> [!Note]  
> L’objet qui est signé dans la contre-signature est la signature d’origine (autrement dit, le EncryptedDigest du signataires d’origine).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool et le processus Authenticode

[SignTool](signtool.md) est disponible pour la signature Authenticode et l’horodatage des données binaires. L’outil est installé dans le \\ dossier bin du chemin d’installation du kit de développement logiciel (SDK) Microsoft Windows.

La signature et l’horodatage des données binaires sont relativement simples à l’aide de [SignTool](signtool.md). Le serveur de publication doit obtenir un certificat de signature de code d’une autorité de certification de signature de code commercial. Pour plus de commodité, Microsoft publie et met à jour une liste des autorités de certification publiques, y compris celles qui émettent des certificats Authenticode. Lorsqu’ils sont prêts à être publiés, les fichiers objets sont signés et l’horodatage est indiqué à l’aide des paramètres de ligne de commande appropriés avec l’outil SignTool. Le résultat d’une opération SignTool est toujours \# au format PKCS 7 [**SignedData**](signeddata.md).

SignTool accepte comme entrée les données binaires brutes à signer et les informations d’horodatage, ou les données binaires précédemment signées pour l’horodatage. Les données qui ont été signées précédemment peuvent être horodatées à l’aide de la commande d' **horodatage SignTool** .



| Argument             | Description                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/T** *HTTPAddress* | Indique que le fichier doit être horodaté. Une URL qui spécifie une adresse d’un serveur d’horodatage doit être fournie. **/t** peut être utilisé avec les commandes de **signature SignTool** et d' **horodatage SignTool** . |



 

Pour plus d’informations sur les outils qui peuvent être utiles dans ce contexte, consultez [outils de chiffrement](cryptography-tools.md) et [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Détails de l’implémentation et format de câble

[SignTool](signtool.md) s’appuie sur l’implémentation de Windows Authenticode pour créer des signatures d’horodatage. [*Authenticode*](../secgloss/a-gly.md) fonctionne sur les fichiers binaires, par exemple. cab,. exe,. dll ou. ocx. Authenticode crée d’abord la signature, en produisant \# un [**SignedData**](signeddata.md)PKCS 7. C’est ce **SignedData** qui doit être contresigné, comme décrit dans PKCS \# 9.

Le processus de contre-signature a lieu en quatre étapes :

1.  Copiez la signature (autrement dit, encryptedDigest) à partir du signataires du \# [**SignedData**](signeddata.md)PKCS 7.
2.  Construisez une demande d’horodatage dont le contenu est la signature d’origine. Envoyez ce code au serveur d’horodatage [*notation de syntaxe abstract One*](../secgloss/a-gly.md) (ASN. 1) encodé en tant que TimeStampRequest.
3.  Recevoir un horodatage, mis en forme en tant que \# deuxième [**SignedData**](signeddata.md)PKCS 7, retourné à partir du serveur d’horodatage.
4.  Copiez le signataires à partir de l’horodatage directement dans le \# [**SignedData**](signeddata.md)PKCS 7 d’origine, sous la forme d’une contre- \# signature PKCS 9 (autrement dit, un attribut non authentifié dans le signataires d’origine).

## <a name="time-stamp-request"></a>Demande d’horodatage

La demande d’horodatage est envoyée dans un message HTTP 1,1 postal. Dans l’en-tête HTTP, la directive CacheControl est définie sur no-cache, et la directive Content-type est définie sur application/octet-stream. Le corps du message HTTP est un encodage Base64 de [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) de la demande d’horodatage.

Bien qu’il ne soit pas actuellement utilisé, la directive Content-Length doit également être utilisée lors de la construction du message HTTP, car elle permet au serveur d’horodatage de localiser l’emplacement où la requête se trouve dans le HTTP.

D’autres en-têtes HTTP peuvent également être présents et doivent être ignorés s’ils ne sont pas compris par le demandeur ou le serveur d’horodatage.

La demande d’horodatage est un message encodé ASN. 1. Le format de la demande est le suivant.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

Le countersignatureType est l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) qui identifie cela comme une contre-signature d’horodatage et doit être le 1.3.6.1.4.1.311.3.2.1 d’OID exact.

Aucun attribut n’est actuellement inclus dans la demande d’horodatage.

Le contenu est un ContentInfo tel que défini par PKCS \# 7. Le contenu correspond aux données à signer. Pour l’horodatage de la signature, le ContentType doit être Data, et le contenu doit être le encryptedDigest (signature) à partir du signataires du \# contenu PKCS 7 pour qu’il soit horodaté.

## <a name="time-stamp-response"></a>Réponse d’horodatage

La réponse d’horodatage est également envoyée dans un message HTTP 1,1. Dans l’en-tête HTTP, la directive Content-type est également définie sur application/octet-stream. Le corps du message HTTP est un encodage Base64 de l’encodage DER de la réponse d’horodatage.

La réponse d’horodatage est un \# message signé PKCS 7 signé par l’horodateur horaire. Le fichier ContentInfo du \# message PKCS 7 est identique à la valeur ContentInfo reçue dans l’horodatage. Le \# contenu PKCS 7 contient l’attribut authentifié de l’heure de signature (défini dans PKCS \# 99, OID 1.2.840.113549.9.5).

Une fois que Authenticode a reçu l’horodatage du serveur, Authenticode incorpore l’horodatage dans le SignedData PKCS 7 d’origine comme contre- \# signature. [](signeddata.md) Pour ce faire, le ContentInfo du \# **SignedData** PKCS 7 renvoyé est ignoré, et le signataires de l’horodatage renvoyé est copié sous la forme d’une contre-signature dans le signataires du SignedData PKCS \# 7 d’origine. La chaîne de certificats de la matrice temporelle est également copiée dans les certificats de l’original PKCS \# 7 **SignedData** comme attribut non authentifié du signataire d’origine.

Pour plus d’informations sur PKCS et d’autres sujets relatifs à la sécurité, consultez la [bibliothèque de contenu du site Web RSA](https://www.rsa.com/content_library.aspx).

 

 
