---
description: Les outils de chiffrement fournissent des outils en ligne de commande pour la signature de code, la vérification de signature et d’autres tâches de chiffrement.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Outils de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237612"
---
# <a name="cryptography-tools"></a>Outils de chiffrement

Les outils de chiffrement fournissent des outils en ligne de commande pour la signature de code, la vérification de signature et d’autres tâches de chiffrement.

## <a name="introduction-to-code-signing"></a>Présentation de la signature de code

L’industrie du logiciel doit fournir aux utilisateurs la possibilité d’approuver du code incluant du code publié sur Internet. De nombreuses pages Web contiennent uniquement des informations statiques qui peuvent être téléchargées avec peu de risques. Toutefois, certaines pages contiennent des contrôles et des applications qui doivent être téléchargés et exécutés sur l’ordinateur d’un utilisateur. Le téléchargement et l’exécution de ces fichiers exécutables peuvent être risqués.

Le logiciel empaqueté utilise des débouchés commerciaux de personnalisation pour garantir l’intégrité des utilisateurs, mais ces garanties ne sont pas disponibles lorsque le code est transmis sur Internet. En outre, Internet lui-même ne peut fournir aucune garantie quant à l’identité du créateur du logiciel. De même, il n’est pas garanti qu’aucun logiciel téléchargé n’a été modifié après sa création. Les navigateurs peuvent présenter un message d’avertissement qui explique les dangers possibles du téléchargement de données de tout type, mais les navigateurs ne peuvent pas vérifier que le code est bien ce qu’il prétend être. Une approche plus active doit être prise pour faire de l’Internet un support fiable pour la distribution de logiciels.

L’une des méthodes permettant de garantir l’authenticité et l' [*intégrité*](../secgloss/i-gly.md) des fichiers consiste à attacher des [*signatures numériques*](../secgloss/d-gly.md) à ces fichiers. Une signature numérique jointe à un fichier identifie de manière positive le serveur de distribution de ce fichier et s’assure que le contenu du fichier n’a pas été modifié après la création de la signature.

Les signatures numériques peuvent être créées et vérifiées à l’aide des API de chiffrement de Microsoft. Pour obtenir des informations générales sur le chiffrement et les fonctions [*CryptoAPI*](../secgloss/c-gly.md) , consultez la page sur la [cryptographie Essentials](cryptography-essentials.md).

Pour plus d’informations sur les [*signatures numériques*](../secgloss/d-gly.md), les [*certificats*](../secgloss/c-gly.md)et les [*magasins de certificats*](../secgloss/c-gly.md), consultez les rubriques suivantes :

-   [Hachages et signatures numériques](hashes-and-digital-signatures.md)
-   [Certificats numériques](digital-certificates.md)
-   [Gestion des certificats avec des magasins de certificats](managing-certificates-with-certificate-stores.md)
-   [Vérification de l’approbation du certificat](certificate-trust-verification.md)

Actuellement, les outils CryptoAPI prennent en charge la technologie Microsoft Authenticode en permettant aux éditeurs de logiciels de signer les types de fichiers suivants pour la vérification Authenticode.



| Extension de nom de fichier                             | Contenu                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .appx<br/>                                | fichiers du programme d’installation pour une application de l’appareil Windows Store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | Fichiers autonomes utilisés pour l’installation et la configuration de l’application. Dans un fichier CAB, plusieurs fichiers sont compressés dans un seul fichier. Ils se trouvent généralement sur les disques de distribution de logiciels de Microsoft.<br/>                        |
| .cat<br/>                                 | Fichiers qui contiennent des [*empreintes*](../secgloss/t-gly.md) numériques de plusieurs fichiers. Un fichier. CAT peut être utilisé pour garantir l’intégrité des fichiers dont il dispose.<br/> |
| .dll<br/>                                 | Fichiers qui contiennent des fonctions exécutables.<br/>                                                                                                                                                                                   |
| .exe<br/>                                 | Fichiers qui contiennent des programmes exécutables.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows des fichiers shell pour JScript ou Microsoft Visual Basic scripting Edition (VBScript).<br/>                                                                                                                                    |
| .msi<br/> .msp<br/> .mst<br/> | Windows les fichiers du programme d’installation.<br/>                                                                                                                                                                                                   |
| .ocx<br/>                                 | fichiers qui contiennent des contrôles Microsoft ActiveX.<br/>                                                                                                                                                                             |
| .ps1<br/>                                 | Fichiers qui contiennent des scripts PowerShell.<br/>                                                                                                                                                                                     |
| . STL<br/>                                 | Fichiers contenant une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL).<br/>                                                                           |
| .sys<br/>                                 | Fichiers qui contiennent des binaires de pilote.<br/>                                                                                                                                                                                        |



 

Pour plus d’informations sur la signature numérique, consultez les documents suivants :

-   CCITT, recommandation X. 509, *Directory-Authentication Framework*, Comité de consultation, téléphone international et télégraphiques, International Telecommunications Union, genève, 1989.
-   RSA Laboratories, *PKCS \# 7 : norme de syntaxe de message de chiffrement*. Version 1,5, novembre, 1993.
-   Schneier, Bruce, *chiffrement appliqué*, 2d ed. New York : John Wiley & fils, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et dans certains pays ou régions.

 

## <a name="microsoft-cryptography-tools"></a>Outils de chiffrement Microsoft

Les outils de publication et la DLL de signature sont installés dans le \\ répertoire bin de votre installation du kit de développement logiciel (SDK) Microsoft. Ils incluent les fichiers suivants.



| Nom de fichier                    | Notes                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | crée un [*certificat SPC (Software Publisher certificate*](../secgloss/s-gly.md) ) à des fins de test uniquement.<br/> |
| [CertMgr.exe](certmgr.md)   | Gère les certificats, les listes CTL et les [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL).<br/>             |
| [MakeCat.exe](makecat.md)   | Crée un fichier de catalogue non signé qui contient les hachages d’un ensemble de fichiers, ainsi que les attributs associés de chaque fichier.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Crée un certificat [*X. 509*](../secgloss/x-gly.md) à des fins de test uniquement.<br/>                                                                      |
| Pvk2pfx.exe                  | convertit un fichier de certificat de l’éditeur de logiciel (. spc) ou un fichier de clé privée (. pvk) au format de fichier PFX (Personal Information Exchange).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Définit les clés de Registre qui contrôlent la vérification du certificat.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Signe et heure horodate un fichier. Vérifie également la signature d’un fichier.<br/>                                                                                                              |



 

 

 
