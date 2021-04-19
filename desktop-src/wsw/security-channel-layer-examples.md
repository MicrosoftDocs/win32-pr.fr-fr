---
title: Exemples de couche de canal de sécurité
description: Les exemples suivants illustrent la sécurité dans la couche de canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- exemples de sécurité
- exemples de sécurité, configuration
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517962"
---
# <a name="security-channel-layer-examples"></a>Exemples de couche de canal de sécurité

Les exemples suivants illustrent la sécurité dans la [couche de canal](channel-layer-overview.md)

Sécurité de transport Windows sur TCP : client : [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), serveur : [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Sécurité de transport Windows sur les canaux nommés : client : [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), serveur : [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Sécurité de transport SSL : client : [HttpClientWithSslExample](httpclientwithsslexample.md), serveur : [HttpServerWithSslExample](httpserverwithsslexample.md).

Nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), serveur : [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nom d’utilisateur sur la sécurité SSL en mode mixte : client : [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), serveur : [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nom d’utilisateur sur la sécurité SSL en mode mixte : [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Jeton émis sur la sécurité SSL en mode mixte : [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificat x509 sur la sécurité SSL en mode mixte : [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>Configuration One-Time pour les exemples de sécurité

Pour exécuter des exemples de sécurité WWSAPI, vous devez configurer les certificats client et serveur pour SSL, ainsi qu’un compte d’utilisateur local pour l’authentification d’en-tête HTTP. Avant de commencer, vous avez besoin des outils suivants :

-   MakeCert.exe (disponible dans le kit de développement logiciel (SDK) Windows 7.)
-   CertUtil.exe ou CertMgr.exe (CertUtil.exe est disponible dans les kits de développement logiciel (SDK) Windows à partir de Windows Server 2003. CertMgr.exe est disponible dans le kit de développement logiciel (SDK) Windows 7. Vous n’avez besoin que d’un de ces outils.)
-   HttpCfg.exe : (vous en avez besoin uniquement si vous utilisez Windows 2003 ou Windows XP. Cet outil est disponible dans les outils de support de Windows XP SP2 et est également fourni avec le CD des outils du kit de ressources Windows Server 2003.)

Si vous obtenez les exemples WWSAPI en installant le kit de développement logiciel (SDK) Windows 7, vous pouvez trouver le MakeCert.exe et CertMgr.exe sous% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.

Effectuez l’installation en cinq étapes suivante à partir de l’invite de commandes (avec élévation de privilèges si vous utilisez Windows Vista et versions ultérieures) :

1.  Générer un certificat auto-signé pour être l’autorité de certification ou l’émetteur : **MakeCert.exe-SS root-SR LocalMachine-n "CN = factice-test-ca"-CY Authority-r-SK "CAKeyContainer"**
2.  Générez un certificat de serveur à l’aide du certificat précédent comme émetteur : **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Sky Exchange-est root-IR LocalMachine-in factice-test-ca-SK "ServerKeyContainer"**
3.  Recherchez l’empreinte numérique (un hachage SHA-1 de 40 caractères) du certificat de serveur en exécutant l’une des commandes suivantes et recherchez le certificat nommé localhost avec l’émetteur factice-test-CA :
    -   **CertUtil.exe-stocker mon localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Inscrire l’empreinte numérique du certificat de serveur sans espace avec HTTP.SYS :
    -   Sur Windows Vista et versions ultérieures (l’option « AppID » est un GUID arbitraire) : **Netsh.exe http add sslcert ipport = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-aabbccddeeff}** certhash =<40CharacterThumbprint>
    -   Sur Windows XP ou 2003 : **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**
5.  Créez un utilisateur local : **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**

Pour nettoyer les certificats, la liaison de certificat SSL et le compte d’utilisateur créés au cours des étapes précédentes, exécutez les commandes suivantes. Remarque s’il existe plusieurs certificats portant le même nom, CertMgr.exe aurez besoin de votre entrée avant de les supprimer.

-   **RacineCertMgr.exe-del-c-n factice-test-CA-s-r LocalMachine**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe http Delete sslcert ipport = 0.0.0.0:8443 (ou HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**
-   **Net user « TestUserForBasicAuth »/Delete**

Assurez-vous qu’il n’existe qu’un seul certificat racine nommé factice-test-CA. Si vous n’êtes pas sûr, il est toujours prudent d’essayer de nettoyer ces certificats à l’aide des commandes de nettoyage ci-dessus (et d’ignorer les erreurs) avant de commencer l’installation en cinq étapes.

 

 




