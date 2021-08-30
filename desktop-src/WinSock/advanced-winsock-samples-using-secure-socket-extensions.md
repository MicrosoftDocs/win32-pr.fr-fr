---
description: Exemples de Winsock avancés utilisant Secure Socket extensions
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Exemples de Winsock avancés utilisant Secure Socket extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477ae91194ef09469cfd857ac36aebabbd4d0f53
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886226"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Exemples de Winsock avancés utilisant Secure Socket extensions

## <a name="secure-tcp-client-and-server-sample"></a>Exemple de serveur et de client TCP sécurisé

un exemple Winsock plus avancé qui illustre l’utilisation d’extensions ssl (secure socket extensions) est inclus dans le kit de développement logiciel (SDK) de Microsoft Windows. L’exemple comprend un client et un serveur TCP qui se connectent en toute sécurité à l’aide de Winsock et des extensions de socket sécurisé.

Par défaut, le code source de l’exemple Winsock est installé dans le répertoire suivant :

*C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ exemples \\ NetDs \\ winsock*

Un exemple se trouve dans le dossier suivant :

*securesocket*

L’exemple de code est divisé en plusieurs répertoires, comme décrit ci-dessous :

-   stcpclient : le dossier qui contient le code client TCP sécurisé.
-   stcpcommon : le dossier qui contient le code de bibliothèque commun qui est partagé entre le client et le serveur TCP sécurisés.
-   stcpserver : le dossier qui contient le code du serveur TCP sécurisé.

notez que les exemples sont censés être exécutés sur deux ordinateurs différents exécutant Windows Vista ou version ultérieure. En outre, les informations d’identification IPsec doivent être approvisionnées sur les deux ordinateurs pour que la connexion aboutisse, car l’exemple utilise IPsec pour sécuriser son trafic. Pour plus d’informations sur la configuration des informations d’identification IPsec, reportez-vous à la documentation relative à la [configuration IPSec](/windows/desktop/FWP/ipsec-configuration) .

La génération de l’exemple génère deux fichiers exécutables :

*stcpclient.exe* et *stcpserver.exe*.

Copiez *stcpclient.exe* sur l’ordinateur A et copiez *stcpserver.exe* sur l’ordinateur B. Sur l’ordinateur B, démarrez le serveur TCP en exécutant la commande suivante dans une invite de commandes :

**stcpserver.exe**

Exécutez la commande suivante pour obtenir d’autres options d’utilisation pour le serveur :

**stcpserver.exe/ ?**

Ensuite, sur l’ordinateur A, démarrez le client TCP en exécutant la commande suivante dans une invite de commandes :

**stcpclient.exe &lt; nom complet-DNS-pour-machine-B&gt;**

À ce stade, la connexion doit être établie en toute sécurité.

Pour plus d’options d’utilisation pour le client, exécutez la commande suivante :

**stcpclient.exe/ ?**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de la plateforme de filtrage Windows](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Application de la couche application (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configuration IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Fonctions IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Utilisation des extensions de socket sécurisé](using-secure-socket-extensions.md)
</dt> <dt>

[interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Plateforme de filtrage Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows Filtrage des fonctions API de la plateforme](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Extensions Winsock Secure Socket](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
