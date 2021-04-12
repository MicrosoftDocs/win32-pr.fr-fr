---
description: Crée un objet de demande CMC à partir d’une requête PKCS 10 imbriquée interne \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318069"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

L’exemple createCNGCustomCMC crée un objet de demande CMC à partir d’une requête PKCS 10 imbriquée interne \# . La requête interne est créée à l’aide d’une [*clé privée*](/windows/desktop/SecGloss/p-gly)asymétrique. La clé privée est créée à l’aide du fournisseur de services de chiffrement Cryptography API : Next Generation (CNG) et de l’algorithme spécifié sur la ligne de commande. Les options personnalisées, telles que la stratégie d’exportation et le niveau de protection de clé, sont également définies sur la clé privée.

## <a name="location"></a>Emplacement

Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ createCNGCustomCMC VC.

## <a name="discussion"></a>Discussions

Exemple createCNGCustomCMC :

1.  Traite les arguments de ligne de commande suivants :
    -   Nom d’un fournisseur de [*services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) CNG.
    -   Nom de l’algorithme utilisé pour générer une clé privée asymétrique.
    -   Nom de l’algorithme utilisé pour [*hacher*](/windows/desktop/SecGloss/h-gly) la [*demande de certificat*](/windows/desktop/SecGloss/c-gly).
    -   Fichier de sortie dans lequel enregistrer la demande de certificat.
    -   Chaîne facultative (AlternateSignature) qui, si elle est présente, spécifie qu’un algorithme discret plutôt qu’un algorithme de signature combiné doit être utilisé. Pour plus d’informations, consultez la propriété [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .
2.  Crée un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) et définit les propriétés suivantes :
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algorithme**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**Keyprotection**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Crée une clé privée asymétrique.
4.  Crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide de la clé privée.
5.  Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide de l' \# objet de requête PKCS 10 créé à l’étape 4.
6.  Définit l’indicateur de l’algorithme de signature alternatif sur **Variant \_ true** ou **\_ false variant** selon qu’une autre chaîne de signature est spécifiée sur la ligne de commande. Pour plus d’informations, consultez [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).
7.  Crée un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID) d' [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) à partir du nom de l’algorithme spécifié sur la ligne de commande et définit l’OID sur l’objet de demande CMC.
8.  Signe la demande de certificat et l’encode à l’aide d' [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
9.  Récupère une chaîne qui contient la demande de certificat CMC encodée et l’enregistre dans un fichier. La fonction EncodeToFileW est définie dans EnrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
