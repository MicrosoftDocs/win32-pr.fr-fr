---
description: Implémente les interfaces IX509PrivateKey et IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Fonctions de clés privées et publiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c1d8ec481c87337e7d7e56cffee47f1f483b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520588"
---
# <a name="private-and-public-key-functions"></a>Fonctions de clés privées et publiques

CertEnroll.dll implémente les interfaces [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) et [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) . Vous pouvez, par exemple, utiliser l’interface [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) pour effectuer les actions suivantes sur une [*clé privée*](/windows/desktop/SecGloss/p-gly):

-   Créer, ouvrir, fermer, importer, exporter et supprimer la clé.
-   Spécifiez ou récupérez l' [*algorithme de clé publique*](/windows/desktop/SecGloss/p-gly).
-   Spécifiez ou récupérez des informations sur le [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) disponible qui prend en charge l’algorithme de clé publique.
-   Spécifiez ou récupérez le [*certificat*](/windows/desktop/SecGloss/c-gly) associé à la [*clé privée*](/windows/desktop/SecGloss/p-gly).
-   Spécifiez ou récupérez le nom du [*conteneur de clé*](/windows/desktop/SecGloss/k-gly).
-   Spécifiez ou récupérez une description de et un nom d’affichage pour la clé.
-   Spécifiez ou récupérez les contraintes d’exportation sur une clé privée.
-   Spécifiez ou récupérez une valeur booléenne qui indique si la clé existe.
-   Spécifiez ou récupérez une valeur qui indique comment la clé est protégée avant son utilisation.
-   Spécifiez ou récupérez une valeur qui indique si la clé peut être utilisée pour la signature, le chiffrement, ou les deux.
-   Spécifiez ou récupérez une valeur qui identifie l’objectif spécifique pour lequel la clé peut être utilisée.
-   Spécifiez ou récupérez la longueur de la clé.
-   Spécifiez ou récupérez une valeur qui indique si la clé est utilisée ou enregistrée dans le contexte d’un ordinateur ou d’un utilisateur.
-   Récupérez une valeur booléenne qui spécifie si la clé a été ouverte.
-   Spécifiez un numéro d’identification personnel pour accéder à une clé privée sur une [*carte à puce*](/windows/desktop/SecGloss/s-gly).
-   Spécifiez ou récupérez le nom du fournisseur de services de chiffrement associé à la clé.
-   Spécifiez ou récupérez le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) pour la clé.

Chacune des sections suivantes identifie une fonction exportée par Xenroll.dll qui peut être utilisée pour gérer une [*clé de chiffrement*](/windows/desktop/SecGloss/c-gly). Chaque rubrique explique également comment utiliser CertEnroll.dll pour remplacer la fonction ou indique qu’il n’existe aucun mappage entre les deux bibliothèques :

-   [ContainerNameWStr](#containernamewstr)
-   [GenKeyFlags](#genkeyflags)
-   [GetKeyLen](#getkeylenex)
-   [GetKeyLenEx](#getkeylenex)
-   [GetSupportedKeySpec](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [LimitExchangeKeyToEncipherment](#limitexchangekeytoencipherment)
-   [PVKFileNameWStr](#pvkfilenamewstr)
-   [ReuseHardwareKeyIfUnableToGenNew](#reusehardwarekeyifunabletogennew)
-   [UseExistingKeySet](#useexistingkeyset)
-   [Rubriques connexes](#related-topics)

## <a name="containernamewstr"></a>ContainerNameWStr

La fonction [**ContainerNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) dans Xenroll.dll spécifie ou récupère le nom du [*conteneur de clé*](/windows/desktop/SecGloss/k-gly).

Lorsque vous utilisez CertEnroll.dll, vous pouvez effectuer les actions suivantes pour récupérer le nom d’un conteneur de clé :

1.  Appelez la propriété [**Request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) sur un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) existant.
2.  Appelez la méthode [**GetInnerRequest**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) sur la requête retournée à l’étape 1 pour récupérer la requête la plus profonde.
3.  Appelez **QueryInterface** sur l’objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) retourné à l’étape 2 pour effectuer un cast en un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Appelez la propriété [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) sur la \# demande PKCS 10.
5.  Appelez la propriété [**containerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) sur l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) récupéré à partir de l’étape 4.

## <a name="genkeyflags"></a>GenKeyFlags

La fonction [**GenKeyFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) définie dans Xenroll.dll spécifie ou récupère les indicateurs utilisés pour générer une clé privée ou une [*paire de clés publique/privée*](/windows/desktop/SecGloss/p-gly).

Lorsque vous utilisez CertEnroll.dll, vous pouvez spécifier un certain nombre de propriétés différentes qui détermineront la façon dont une clé privée sera créée. Pour plus d’informations, consultez [**créer**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>GetKeyLen

La fonction [**GetKeyLen**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) définie dans Xenroll.dll récupère la taille de clé maximale ou minimale d’une clé de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez appeler la propriété [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) sur un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) pour récupérer la taille de la clé, en bits.

## <a name="getkeylenex"></a>GetKeyLenEx

La fonction [**GetKeyLenEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) définie dans Xenroll.dll récupère la taille de clé maximale ou minimale ou la longueur d’incrément d’une clé de chiffrement.

Lorsque vous utilisez CertEnroll.dll, vous pouvez appeler la propriété [**Length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) sur un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) pour récupérer la taille de la clé, en bits. Si un algorithme prend en charge des longueurs de clé incrémentielles, vous pouvez appeler la propriété [**IncrementLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) sur l’objet [**ICspAlgorithm**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) pour récupérer la valeur d’incrémentation. Vous pouvez également appeler les propriétés [**minLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) et [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) pour récupérer les tailles de clé minimale et maximale.

## <a name="getsupportedkeyspec"></a>GetSupportedKeySpec

La fonction [**GetSupportedKeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) définie dans Xenroll.dll récupère une valeur qui indique si un fournisseur de services de chiffrement prend en charge les clés d’échange, les clés de signature ou les deux.

Lorsque vous utilisez CertEnroll.dll, vous pouvez appeler la propriété [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) sur les objets [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) ou [**ICspInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) pour récupérer les opérations prises en charge par la clé.

## <a name="keyspec"></a>KeySpec

La fonction [**KeySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) définie dans Xenroll.dll spécifie ou récupère le type de clé.

Lorsque vous utilisez CertEnroll.dll, vous pouvez appeler la propriété [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) sur un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) pour récupérer les opérations prises en charge par la clé.

## <a name="limitexchangekeytoencipherment"></a>LimitExchangeKeyToEncipherment

La fonction [**LimitExchangeKeyToEncipherment**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) définie dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique si une clé de chiffrement peut être utilisée uniquement pour les données ou le chiffrement de clé.

CertEnroll.dll ne contient pas d’équivalent direct pour cette fonction. Toutefois, vous pouvez obtenir un résultat quasiment équivalent en spécifiant un objet [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) et en l’ajoutant à la demande de certificat.

## <a name="pvkfilenamewstr"></a>PVKFileNameWStr

La fonction [**PVKFileNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) définie dans Xenroll.dll spécifie ou récupère le nom d’un fichier qui contient des clés exportées.

Quand vous utilisez CertEnroll.dll, vous pouvez appeler la méthode [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) sur un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) pour exporter une clé vers un **BSTR**. Vous pouvez appeler la méthode [**ExportPublicKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) pour exporter la partie [*clé publique*](/windows/desktop/SecGloss/p-gly) d’une paire de clés asymétriques.

## <a name="reusehardwarekeyifunabletogennew"></a>ReuseHardwareKeyIfUnableToGenNew

La fonction [**ReuseHardwareKeyIfUnableToGenNew**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) définie dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique si une clé existante est réutilisée lorsqu’une erreur se produit lors de la génération d’une nouvelle clé.

Quand vous utilisez CertEnroll.dll, vous pouvez appeler la méthode [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) sur un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et spécifier une valeur du type d’énumération [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) pour réutiliser une clé privée existante.

## <a name="useexistingkeyset"></a>UseExistingKeySet

La fonction [**UseExistingKeySet**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) définie dans Xenroll.dll spécifie ou récupère une valeur booléenne qui indique s’il faut utiliser des clés existantes.

Lorsque vous utilisez CertEnroll.dll, vous pouvez appeler la méthode [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) sur un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et spécifier une valeur du type d’énumération [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) pour réutiliser les clés privées et publiques existantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
