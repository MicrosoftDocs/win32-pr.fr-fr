---
title: Catégorisation des fournisseurs de services en couche et des applications
description: Winsock 2 prend en charge les protocoles en couches.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515453"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Catégorisation des fournisseurs de services en couche et des applications

> [!Note]  
> Les fournisseurs de services en couche sont déconseillés. À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).

 

Winsock 2 prend en charge les protocoles en couches. Un protocole en couches est un protocole qui implémente uniquement les fonctions de communication de niveau supérieur, tout en s’appuyant sur une pile de transport sous-jacente pour l’échange réel de données avec un point de terminaison distant. Un exemple d’un protocole en couches ou d’un fournisseur de services en couche est une couche de sécurité qui ajoute le protocole au processus d’établissement de la connexion afin d’effectuer l’authentification et d’établir un schéma de chiffrement convenu mutuellement. Un tel protocole de sécurité nécessite généralement les services d’un protocole de transport Reliable sous-jacent, tel que TCP ou SPX. Le terme protocole de base implémenté par le fournisseur de base fait référence à un fournisseur Winsock qui implémente un protocole tel que TCP ou SPX qui est capable d’effectuer des communications de données avec un point de terminaison distant. Le terme protocole à couches est utilisé pour décrire un protocole qui ne peut pas être autonome. Ces protocoles superposés sont installés en tant que fournisseurs de services en couche (LSP) Winsock.

Un exemple d’un LSP est le fournisseur de services du client de pare-feu Microsoft installé dans le cadre de l’Internet Secutity et du serveur d’authentification (ISA) sur les clients. Le fournisseur de services du client de pare-feu Microsoft s’installe sur les fournisseurs de base Winsock pour TCP et UDP. Une bibliothèque de liens dynamiques (DLL) dans le logiciel client de pare-feu ISA devient un fournisseur de services en couche Winsock que toutes les applications Winsock utilisent en toute transparence. De cette façon, le client de pare-feu ISA LSP peut intercepter les appels de fonction Winsock à partir des applications clientes, puis acheminer une demande vers le fournisseur de services de base sous-jacent d’origine si la destination est locale ou vers le service de pare-feu sur un ordinateur ISA Server si la destination est distante. Un LSP similaire est installé dans le cadre du service pare-feu Microsoft Forefront et du client Threat Management Gateway (TMG) sur les clients.

Pendant l’initialisation de LSP, le LSP doit fournir des pointeurs vers plusieurs fonctions de l’interface de fournisseur de services (SPI) Winsock. Ces fonctions sont appelées au cours d’un traitement normal par la couche située juste au-dessus du LSP (soit un autre32.DLL LSP ou Ws2 \_ ).

Il est possible de définir des catégories LSP basées sur le sous-ensemble de fonctions SPI qu’un LSP met en œuvre et la nature du traitement supplémentaire effectué pour chacune de ces fonctions. En classant les LSP, ainsi que la classification des applications qui utilisent des sockets Winsock, il devient possible de déterminer de manière sélective si un LSP doit être impliqué dans un processus donné au moment de l’exécution.

Sur Windows Vista et versions ultérieures, une nouvelle méthode est fournie pour classer les applications et les fournisseurs de services en couche Winsock afin que seuls certains LSP soient chargés. Il existe plusieurs raisons pour ajouter ces fonctionnalités.

L’une des principales raisons est que certains processus système critiques, tels que Winlogon et LSASS, créent des sockets, mais ces processus n’utilisent pas ces Sockets pour envoyer du trafic sur le réseau. La plupart des LSP ne doivent donc pas être chargés dans ces processus. Un certain nombre de cas ont également été documentés dans lesquels des LSP de bogue peuvent provoquer le blocage de *lsass.exe* . En cas de blocage de LSASS, le système force un arrêt. L’effet secondaire de ces processus système qui chargent les LSP est que ces processus ne se ferment jamais. par conséquent, lorsqu’un LSP est installé ou supprimé, un redémarrage est nécessaire.

Une raison secondaire est que dans certains cas, il se peut que les applications ne souhaitent pas charger certains LSP. Par exemple, certaines applications peuvent ne pas vouloir charger des LSP de chiffrement qui pourraient empêcher l’application de communiquer avec d’autres systèmes sur lesquels le LSP cyptographic n’est pas installé.

Enfin, les catégories LSP peuvent être utilisées par d’autres LSP pour déterminer où elles doivent s’installer dans la chaîne de protocole Winsock. Pendant des années, divers développeurs LSP ont voulu savoir comment se comportera un LSP. Par exemple, un LSP qui inspecte le flux de données doit se trouver au-dessus d’un LSP qui chiffre les données. Bien entendu, cette méthode de catégorisation LSP n’est pas trompeur, car elle s’appuie sur les LSP tiers pour les classer de manière appropriée.

La catégorisation LSP et d’autres améliorations de sécurité dans Windows Vista et les versions ultérieures sont conçues pour empêcher les utilisateurs d’installer involontairement des LSP malveillants.

## <a name="lsp-categories"></a>Catégories LSP

Sur Windows Vista et versions ultérieures, un LSP peut être classé en fonction de la façon dont il interagit avec les données et les appels Windows Sockets. Une catégorie LSP est un groupe identifiable de comportements sur un sous-ensemble de fonctions Winsock SPI. Par exemple, un filtre de contenu HTTP est classé en tant qu’inspecteur de données (catégorie de l' \_ inspecteur LSP). La \_ catégorie de l’inspecteur LSP inspecte (mais ne modifie pas) les paramètres des fonctions SPI de transfert de données. Une application peut interroger la catégorie d’un LSP et choisir de ne pas charger le LSP en fonction de la catégorie LSP et de l’ensemble des catégories LSP autorisées de l’application.

Le tableau suivant répertorie les catégories dans lesquelles un LSP peut être classé.

| Catégorie LSP              | Description                                                     |
|---------------------------|-----------------------------------------------------------------|
| **\_compression de chiffrement LSP \_** | Le LSP est un fournisseur de chiffrement ou de compression de données.         |
| **\_pare-feu LSP**         | Le LSP est un fournisseur de pare-feu.                                 |
| **\_cache local \_ LSP**     | Le LSP est un fournisseur de cache local.                              |
| **\_modification entrante de LSP \_**  | Le LSP modifie les données entrantes.                                  |
| **\_inspecteur LSP**        | Le LSP inspecte ou filtre les données.                               |
| **\_modification sortante \_ LSP** | Le LSP modifie les données sortantes.                                 |
| **\_proxy LSP**            | Le LSP agit comme un proxy et redirige les paquets.                  |
| **redirecteur LSP \_**       | Le LSP est un redirecteur réseau.                                |
| **\_système LSP**           | Le LSP est acceptable pour une utilisation dans les services et les processus système. |



 

Un LSP peut appartenir à plusieurs catégories. Par exemple, un LSP de pare-feu/sécurité peut appartenir à la fois aux catégories Inspector (**\_ inspecteur LSP**) et pare-feu (**\_ pare-feu LSP**).

Si un LSP n’a pas de catégorie définie, il est considéré comme étant dans la catégorie toute autre. Cette catégorie LSP ne sera pas chargée dans les services ou les processus système (par exemple, LSASS, Winlogon et de nombreux processus Svchost).

## <a name="categorizing-lsps"></a>Catégorisation des LSP

Plusieurs nouvelles fonctions sont disponibles sur Windows Vista et versions ultérieures pour classer un LSP :

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Pour classer un LSP, la fonction [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) ou [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) est appelée avec un GUID pour identifier l’entrée masquée LSP, la classe d’informations à définir pour cette entrée de protocole LSP et un ensemble d’indicateurs utilisés pour modifier le comportement de la fonction.

La fonction [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) ou [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) est utilisée de la même façon pour récupérer les données associées à une classe d’informations pour un LSP.

## <a name="categorizing-applications"></a>Catégorisation des applications

Plusieurs nouvelles fonctions sont disponibles sur Windows Vista et versions ultérieures pour la catégorisation d’une application :

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Pour classer une application, la fonction [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) est appelée avec le chemin de chargement vers l’image exécutable pour identifier l’application, les arguments de ligne de commande utilisés lors du démarrage de l’application et les catégories LSP autorisées pour toutes les instances de cette application.

La fonction [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) est utilisée de la même façon pour récupérer les catégories du fournisseur de services en couche (LSP) associées à une application.

## <a name="determining-which-lsps-get-loaded"></a>Détermination des LSP chargés

La dernière partie de la catégorisation LSP consiste à déterminer les LSP qui seront chargés dans les processus. Lorsqu’un processus charge Winsock, les comparaisons suivantes sont effectuées à partir de la catégorie application et des catégories LSP pour tous les LSP installés :

-   Si l’application n’est pas catégorisée, autorisez le chargement de tous les LSP dans le processus.
-   Si l’application et le LSP ont tous deux affecté des catégories, les conditions suivantes doivent être remplies : <dl> Au moins l’une des catégories LSP est présente dans les catégories spécifiées de l’application.  
    Seules les catégories spécifiées dans les catégories spécifiées de l’application sont spécifiées dans les catégories LSP. Par exemple, si l’application spécifie une catégorie, elle doit figurer dans la catégorie LSP.  
    Si la \_ catégorie du système LSP est présente dans la catégorie de l’application, elle doit être présente dans les catégories du LSP.  
    </dl>

> [!Note]  
> Si un LSP n’est pas catégorisé, sa catégorie est effectivement égale à zéro. Pour qu’une correspondance se produise, toutes les catégories spécifiées dans le LSP doivent être présentes dans les catégories de l’application (les catégories de l’application doivent être un sur-ensemble des catégories du LSP). en outre, si le \_ système LSP est présent dans la catégorie de l’application, il doit également être présent dans la catégorie LSP.

 

Prenons l’exemple suivant :

L’application *Foo.exe* est catégorisée comme \_ système LSP + \_ pare-feu LSP + LSP \_ crypto \_ . Le *Bar.exe* de l’application est catégorisé comme \_ pare-feu LSP + \_ compression de chiffrement LSP \_ . Quatre LSP sont installés sur le système :

-   LSP1 a défini une catégorie de \_ système LSP.
-   LSP2 n’est pas défini sur les catégories. sa catégorie est donc égale à zéro.
-   LSP3 a défini une catégorie de \_ pare-feu LSP.
-   LSP4 a défini des catégories de \_ système LSP + \_ pare-feu LSP + LSP \_ crypto \_ compression + LSP \_ Inspector

Dans cet exemple, l’application *Foo.exe* chargera uniquement lsp1, tandis que l’application *Bar.exe* chargera LSP3.

## <a name="determining-winsock-providers-installed"></a>Détermination des fournisseurs Winsock installés

Le kit de développement logiciel (SDK) Microsoft Windows comprend un exemple de programme Winsock qui peut être utilisé pour déterminer les fournisseurs de transport Winsock installés sur un ordinateur local. Par défaut, le code source de cet exemple Winsock est installé dans le répertoire suivant du SDK Windows pour Windows 7 :

*C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ NetDs \\ Winsock \\ LSP*

Cet exemple est un utilitaire pour l’installation et le test des fournisseurs de services en couche. Toutefois, il peut également être utilisé pour collecter des informations détaillées du catalogue Winsock sur un ordinateur local par programmation. Pour répertorier tous les fournisseurs Winsock actuels, y compris les fournisseurs de base et les fournisseurs de services de couche, générez cet exemple Winsock et exécutez la commande de console suivante :

**instlsp-p**

La sortie sera une liste des fournisseurs Winsock installés sur l’ordinateur local, y compris les fournisseurs de services en couche. La sortie répertorie l’ID de catalogue et le nom de chaîne pour le fournisseur Winsock.

Pour collecter des informations plus détaillées sur tous les fournisseurs Winsock, exécutez la commande de console suivante :

**instlsp-p-v**

La sortie sera une liste de structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) prises en charge sur l’ordinateur local.

Pour obtenir la liste des seuls fournisseurs de services en couche installés sur l’ordinateur local, exécutez la commande de console suivante :

**instlsp-l**

Pour mapper la structure LSP, exécutez la commande de console suivante :

**instlsp-m**

> [!Note]  
> La fonctionnalité TDI est déconseillée et sera supprimée dans les prochaines versions de Microsoft Windows. Selon la façon dont vous utilisez TDI, utilisez le noyau Winsock (WSK) ou la plateforme de filtrage Windows (WFP). Pour plus d’informations sur WFP et WSK, consultez [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md) et [noyau Winsock](/windows-hardware/drivers/ddi/_netvista/). Pour une entrée de blog sur la mise en réseau de base Windows sur WSK et TDI, consultez [Introduction to Winsock kernel (WSK) (en anglais)](/archive/blogs/wndp/).

 

 

 
