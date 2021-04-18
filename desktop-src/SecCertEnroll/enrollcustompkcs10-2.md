---
description: Crée une demande PKCS \# 10 personnalisée et tente de l’inscrire dans une autorité de certification d’entreprise.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533611"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

L' \_ exemple enrollCustomPKCS10 2 crée une demande PKCS \# 10 personnalisée et tente de l’inscrire auprès d’une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) d’entreprise.

## <a name="location"></a>Emplacement

Lorsque vous installez le kit de développement logiciel (SDK) de Microsoft Windows, l’exemple est installé par défaut dans le dossier *% ProgramFiles%* \\ Microsoft SDK Microsoft \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Discussions

Exemple enrollCustomPKCS10 \_ 2 :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir le nom d’un modèle et le nom d’un fournisseur de services de chiffrement.
2.  Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) et l’initialise à l’aide du nom du modèle spécifié sur la ligne de commande.
3.  Récupère la [*demande de certificat*](/windows/desktop/SecGloss/c-gly) à partir de l’objet d’inscription.
4.  Récupère la requête PKCS 10 la plus profonde \# de l’objet de demande de certificat obtenu à l’étape 3.
5.  Récupère une [*clé privée*](/windows/desktop/SecGloss/p-gly) à partir de la \# demande PKCS 10.
6.  Crée une collection [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) et ajoute les fournisseurs de services de chiffrement disponibles à la collection, puis récupère un objet [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) pour le fournisseur spécifié sur la ligne de commande.
7.  Définit l’objet d’État sur la clé privée.
8.  Tente d’inscrire la [*demande de certificat*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\#Demande PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 
