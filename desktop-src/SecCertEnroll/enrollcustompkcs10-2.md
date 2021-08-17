---
description: Crée une demande PKCS \# 10 personnalisée et tente de l’inscrire dans une autorité de certification d’entreprise.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780038"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

L' \_ exemple enrollCustomPKCS10 2 crée une demande PKCS \# 10 personnalisée et tente de l’inscrire auprès d’une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) d’entreprise.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) microsoft Windows, l’exemple est installé par défaut dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ enrollCustomPKCS10 \_ 2.

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

 

 
