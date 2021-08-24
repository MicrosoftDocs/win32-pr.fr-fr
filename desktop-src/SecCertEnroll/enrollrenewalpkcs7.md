---
description: Crée un \# objet de requête PKCS 7 pour renouveler un certificat existant. L’objet de requête utilise une nouvelle paire de clés, mais conserve le fournisseur de services de chiffrement associé au certificat en cours de renouvellement.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3da14719cc2a9e6bdf4c16cad57d24b9ee4ec0c2ee955cc8b7c20643b2b6f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740429"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

L’exemple enrollRenewalPKCS7 crée un \# objet de demande PKCS 7 pour renouveler un certificat existant. L’objet de requête utilise une nouvelle paire de clés, mais conserve le fournisseur de services de chiffrement associé au certificat en cours de renouvellement.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollRenewalPKCS7 VC.

## <a name="discussion"></a>Discussions

Exemple enrollRenewalPKCS7 :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom du modèle utilisé pour créer la demande de certificat.
2.  Récupère un certificat existant en utilisant le nom du modèle spécifié sur la ligne de commande ou, si un certificat est introuvable, tente d’en inscrire un à l’aide du modèle. Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.
3.  Vérifie la chaîne de certificats et convertit le certificat en **BSTR**.
4.  Crée un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) et l’initialise à l’aide du certificat existant. Étant donné que le paramètre *inheritOptions* est défini sur InheritDefault, une nouvelle paire de clés est créée pour la demande, mais le fournisseur de services de chiffrement dans le certificat existant est utilisé. Pour plus d’informations, consultez la méthode [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .
5.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l' \# objet de requête PKCS 7, tente de l’inscrire auprès de l’autorité de certification et surveille l’état du processus d’inscription. La fonction checkEnrollStatus est définie dans enrollCommon. cpp.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[\#Demande de renouvellement PKCS 7](pkcs--7--renewal-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



