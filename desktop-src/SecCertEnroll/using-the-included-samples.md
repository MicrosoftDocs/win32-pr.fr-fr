---
description: L’API d’inscription de certificats comprend plusieurs exemples conçus pour vous aider à créer des applications personnalisées. La plupart des exemples sont écrits à l’aide de C++, mais les exemples C# et Visual Basic Scripting Edition (VBScript) sont également inclus.
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Utilisation des exemples inclus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3cbf17d35e65ade52e97438d638cbd4f1489e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536541"
---
# <a name="using-the-included-samples"></a>Utilisation des exemples inclus

L’API d’inscription de certificats comprend plusieurs exemples conçus pour vous aider à créer des applications personnalisées. La plupart des exemples sont écrits à l’aide de C++, mais les exemples C# et Visual Basic Scripting Edition (VBScript) sont également inclus.

Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, les exemples suivants sont installés, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft kits de \\ \\ \\ sécurité exemples de certificats X509 de sécurité Windows v 7.0 \\ \\ \\ .



| Exemple                                                                 | Description                                                                                                                                                                                                                                                                                                                                                | Language            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Crée un objet de demande CMC à partir d’une requête PKCS 10 imbriquée interne \# .<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contient les fonctions d’assistance et les macros suivantes utilisées par les exemples inclus.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Crée une demande de certificat CMC et inscrit un ordinateur dans une hiérarchie de certificats.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Crée une demande PKCS \# 10 personnalisée, l’envoie à une [*autorité de certification*](/windows/desktop/SecGloss/c-gly) autonome (ca) et installe le certificat émis dans le [*magasin de certificats*](/windows/desktop/SecGloss/c-gly).<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Crée une demande PKCS \# 10 personnalisée et tente de l’inscrire dans une autorité de certification d’entreprise.<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Crée une demande de certificat CMC pour le compte d’un autre utilisateur et inscrit l’utilisateur dans une hiérarchie de certificats.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Initialise un objet de \# demande de certificat PKCS 10, l’encapsule dans un objet de demande CMC, soumet la demande CMC à une autorité de certification d’entreprise et enregistre le certificat retourné par l’autorité de certification dans un fichier.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Crée une demande de certificat CMC pour archiver une [*clé privée*](/windows/desktop/SecGloss/p-gly) sur une autorité de certification.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Lit une demande de certificat CMC existante à partir d’un fichier, l’encapsule dans une autre demande CMC, signe cette requête externe, la soumet à une autorité de certification et enregistre la réponse du certificat de l’autorité de certification dans un fichier.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Crée une demande [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) à partir d’un certificat existant en héritant des clés publiques et privées et du modèle de certificat. L’exemple inscrit l’utilisateur dans une hiérarchie de certificats et installe la réponse du certificat.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Crée un \# objet de requête PKCS 7 pour renouveler un certificat existant.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Inscrit un ordinateur dans une hiérarchie de certificats à l’aide d’un modèle, d’un nom d’affichage de certificat et de la description du certificat.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Inscrit un utilisateur final auprès d’une autorité de certification à l’aide d’un modèle, du nom de l’objet et de la longueur, en bits, de la clé.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Montre comment utiliser le protocole HTTP Windows 7 pour inscrire un certificat dans une autorité de certification d’entreprise.<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Installe un certificat inscrit à partir d’un fichier d’échange d’informations personnelles (PFX) dans le magasin de certificats.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API d’inscription de certificats](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

