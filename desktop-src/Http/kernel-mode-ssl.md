---
title: SSL en mode noyau
description: SSL en mode noyau
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL en mode noyau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513691"
---
# <a name="kernel-mode-ssl"></a>SSL en mode noyau

Le mode noyau SSL a été introduit dans Windows Server 2003 avec Service Pack 1 (SP1) avec prise en charge limitée. Pour les ordinateurs qui exécutent Windows Server 2003 avec SP1, une clé de registre doit être configurée pour activer le SSL de noyau. Pour les ordinateurs qui exécutent Windows Server 2008 et Windows Vista, la prise en charge du mode noyau complet pour SSL est fournie.

Les sections suivantes décrivent la prise en charge SSL en mode noyau :

-   Modes noyau SSL dans Windows Server 2003 avec SP1
-   SSL en mode noyau dans Windows Server 2008 et Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Modes noyau SSL dans Windows Server 2003 avec SP1

Dans Windows Server 2003 avec SP1, l’API du serveur HTTP offre la possibilité d’exécuter la sécurité SSL en mode noyau (le mode utilisateur est SSL par défaut). La fonctionnalité en mode noyau améliore les performances SSL en déplaçant les opérations de chiffrement et de déchiffrement vers le noyau, réduisant ainsi le nombre de transitions entre le mode noyau et le mode utilisateur.

Les fonctionnalités suivantes ne sont pas prises en charge lorsque SSL est exécuté en mode noyau :

-   Certificats clients
-   Chiffrements RC2
-   Le protocole PCT 1,0
-   Les modifications de configuration de certificat de serveur requièrent un redémarrage du service HTTP
-   Chiffrement en bloc et prise en charge du déchargement

## <a name="configuring-kernel-mode-ssl"></a>Configuration du mode noyau SSL

Le mode noyau SSL est contrôlé par la valeur de Registre **EnableKernelSSL** et est activé en définissant la valeur sur 1. L’activation du mode noyau SSL désactive le mode utilisateur SSL et nécessite le redémarrage du service HTTP pour prendre effet. La clé de Registre **EnableKernelSSL** se trouve à l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** http des services \\  de CurrentControlSet de système d’ordinateur local EnableKernelSSL

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>SSL en mode noyau dans Windows Server 2008 et Windows Vista

Pour les ordinateurs qui exécutent Windows Server 2008 et Windows Vista, l’API du serveur HTTP offre des fonctionnalités SSL améliorées.

Les nouvelles fonctionnalités suivantes sont prises en charge :

-   Prise en charge complète des certificats clients en mode noyau SSL
-   SSL en mode noyau pour toutes les transactions HTTP SSL
-   Chiffrement en bloc et prise en charge du déchargement
-   Le protocole PCT 1,0
-   Chiffrements RC2
-   Performances accrues par rapport au mode utilisateur SSL

## <a name="configuration"></a>Configuration

Le mode noyau SSL peut être configuré à l’aide de deux valeurs de Registre sous la clé des paramètres HTTP, à l’emplacement suivant :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

Un utilisateur doit disposer des privilèges administrateur/système local pour modifier les valeurs de Registre et afficher ou modifier les fichiers journaux et le dossier qui les contient.

Les informations de configuration dans les valeurs de Registre sont lues lorsque le pilote de l’API du serveur HTTP est démarré. Par conséquent, si les paramètres sont modifiés, le pilote doit être arrêté et redémarré pour lire les nouvelles valeurs. Pour ce faire, vous pouvez utiliser les commandes de console suivantes :

**net stop http**

**NET START http**

Le tableau suivant répertorie les valeurs de configuration du Registre.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur de Registre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 et Windows Vista :</strong> Cette valeur de Registre est obsolète.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Valeur <strong>DWORD</strong> qui a la valeur <strong>true</strong> pour activer Close-Notify ou <strong>false</strong> pour désactiver la spécification de fermeture-notification. Fermer-Notify est désactivé par défaut.<br/> Lorsque l’option fermer-notifier est activée, l’application cliente est requise pour envoyer un message de fermeture et de notification avant de fermer les connexions TCP. L’API du serveur HTTP envoie également une notification de fermeture avant de fermer la connexion.<br/> Lorsque l’option fermer-notifier est activée et que le client envoie un message de fermeture-notification, l’API du serveur HTTP réutilise la session SSL sur les connexions futures au client. Si le client n’envoie pas de fermeture-notification, l’API du serveur HTTP ne réutilisera pas la même session SSL sur les connexions futures. Par conséquent, une liaison SSL complète est déclenchée sur la nouvelle connexion, ce qui réduit les performances. <br/>
<blockquote>
[!Note]<br />
L’activation de la fonction de fermeture-notification permet d’atténuer les attaques par troncation contre les requêtes et les réponses HTTPs.
</blockquote>
<br/> <br/> Lorsque la fermeture-notification est désactivée, l’API du serveur HTTP réutilise la session SSL pour les connexions ultérieures.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Valeur <strong>DWORD</strong> définie sur <strong>true</strong> pour permettre à l’API du serveur http de récupérer des certificats intermédiaires à partir d’Internet ou du magasin local, ou <strong>false</strong> pour récupérer des certificats intermédiaires du magasin local uniquement. La valeur de Registre par défaut est <strong>false</strong>.<br/> Par défaut, l’API du serveur HTTP crée une chaîne de certificats client en récupérant les certificats intermédiaires dans le magasin de l’autorité de certification intermédiaire sous le compte de l’ordinateur local. Si cette valeur est définie sur <strong>true</strong> , l’API du serveur http récupère les certificats intermédiaires non seulement dans le magasin local, mais également à partir de l’autorité de certification intermédiaire sur Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





