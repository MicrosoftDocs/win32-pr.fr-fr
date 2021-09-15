---
description: installe un certificat inscrit à partir d’un fichier de Exchange d’informations personnelles (PFX) dans le magasin de certificats.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: installResponseFromPFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311309"
---
# <a name="installresponsefrompfx"></a>installResponseFromPFX

l’exemple installResponseFromPFX installe un certificat inscrit à partir d’un fichier de Exchange d’informations personnelles (PFX) dans le magasin de certificats.

## <a name="location"></a>Emplacement

lorsque vous installez le kit de développement logiciel (SDK) de microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security \\ X509 certificate \\ \\ installResponseFromPFX VC.

## <a name="discussion"></a>Discussion

Exemple installResponseFromPFX :

1.  Traite les arguments de ligne de commande. La ligne de commande doit contenir :
    -   Nom de l’exemple.
    -   Nom du fichier PFX qui contient le certificat inscrit.
    -   Mot de passe associé au fichier PFX.
2.  Lit le fichier PFX, en commençant par le format Base64 et le format binaire si base64 échoue. La fonction DecodeFileW () est définie dans enrollCommon. cpp.
3.  Convertit le certificat inscrit en **BSTR** et l’utilise pour initialiser un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . La fonction convertWszToBstr est définie dans enrollCommon. cpp.
4.  Installe le certificat dans le magasin de certificats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[enrollEOBOCMC](enrolleobocmc.md)
</dt> <dt>

[Utilisation des exemples inclus](using-the-included-samples.md)
</dt> </dl>

 

 



