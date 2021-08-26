---
description: Crée une demande de certificat CMC pour archiver une clé privée sur une autorité de certification.
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e2e9856309560e982e7e1dda7ba724fefd0759e6fa10196b321eb66947cf64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882949"
---
# <a name="enrollkeyarchivalcmc"></a>enrollKeyArchivalCMC

L’exemple enrollKeyArchivalCMC crée une demande de certificat CMC pour archiver une clé privée sur une autorité de certification. Pour plus d’informations, consultez [demande d’archivage de clé CMC](cmc-key-archival-request.md).

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollKeyArchivalCMC VC.

## <a name="discussion"></a>Discussions

Exemple enrollKeyArchivalCMC :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom du modèle de certificat à utiliser pour l’inscription.
2.  Crée un objet de demande de certificat [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise pour un contexte d’utilisateur final en utilisant le nom du modèle.
3.  Définit la propriété [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) sur la demande CMC.
4.  Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.
5.  Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise pour récupérer le certificat Exchange pour l’autorité de certification.
6.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de la demande CMC, crée une chaîne encodée en base64 qui contient la demande d’archivage de clé et l’envoie à l’autorité de certification.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Demande d’archivage de clé CMC](cmc-key-archival-request.md)
</dt> <dt>

[Demande CMC](cmc-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
