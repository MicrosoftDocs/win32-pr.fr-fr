---
description: le système d’exploitation Windows fournit des mécanismes pour faciliter les communications et le partage de données entre les applications. Collectivement, les activités activées par ces mécanismes sont appelées communications interprocessus (IPC).
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Communications interprocessus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5632443187ba9e50ed6c7f1adb31e8a02a280735c99dd8ee5455d2f067ef263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756318"
---
# <a name="interprocess-communications"></a>Communications interprocessus

le système d’exploitation Windows fournit des mécanismes pour faciliter les communications et le partage de données entre les applications. Collectivement, les activités activées par ces mécanismes sont appelées *communications interprocessus* (IPC). Certaines formes d’IPC facilitent la Division du travail entre plusieurs processus spécialisés. D’autres formes d’IPC facilitent la Division du travail entre les ordinateurs d’un réseau.

En règle générale, les applications peuvent utiliser IPC catégorisé comme clients ou serveurs. Un *client* est une application ou un processus qui demande un service à partir d’une autre application ou d’un autre processus. Un *serveur* est une application ou un processus qui répond à une demande du client. De nombreuses applications agissent à la fois comme un client et un serveur, en fonction de la situation. Par exemple, une application de traitement de texte peut agir en tant que client pour demander un tableau récapitulatif des coûts de fabrication d’une application de feuille de calcul agissant comme un serveur. L’application de tableur, à son tour, peut agir en tant que client lors de la demande des niveaux de stock les plus récents à partir d’une application de contrôle d’inventaire automatisée.

Une fois que vous avez décidé que votre application pourrait tirer parti d’IPC, vous devez décider de la méthode IPC disponible à utiliser. Il est probable qu’une application utilise plusieurs mécanismes IPC. Les réponses à ces questions déterminent si une application peut tirer parti de l’utilisation d’un ou de plusieurs mécanismes IPC.

-   L’application doit-elle pouvoir communiquer avec d’autres applications exécutées sur d’autres ordinateurs sur un réseau, ou est-il suffisant pour que l’application communique uniquement avec les applications sur l’ordinateur local ?
-   l’application doit-elle être en mesure de communiquer avec des applications exécutées sur d’autres ordinateurs qui peuvent s’exécuter sous des systèmes d’exploitation différents (par exemple, 16 bits Windows ou UNIX) ?
-   L’utilisateur de l’application doit-il choisir les autres applications avec lesquelles l’application communique, ou l’application peut-elle trouver implicitement ses partenaires coopérants ?
-   L’application doit-elle communiquer avec de nombreuses applications de manière générale, par exemple pour autoriser les opérations couper-coller avec une autre application, ou si ses exigences en matière de communication doivent être limitées à un ensemble restreint d’interactions avec d’autres applications spécifiques ?
-   Les performances sont-elles un aspect critique de l’application ? Tous les mécanismes IPC incluent une quantité de surcharge.
-   L’application doit-elle être une application GUI ou une application console ? Certains mécanismes IPC nécessitent une application GUI.

Les mécanismes IPC suivants sont pris en charge par les Windows :

-   [Presse-papiers](#using-the-clipboard-for-ipc)
-   [COM](#using-com-for-ipc)
-   [Copie de données](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Mappage de fichiers](#using-a-file-mapping-for-ipc)
-   [Boîtes](#using-a-mailslot-for-ipc)
-   [Canaux](#using-pipes-for-ipc)
-   [RPC](#using-rpc-for-ipc)
-   [Windows Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Utilisation du presse-papiers pour IPC

Le presse-papiers fait office de dépositaire central pour le partage de données entre les applications. Lorsqu’un utilisateur effectue une opération couper ou copier dans une application, l’application place les données sélectionnées dans le presse-papiers dans un ou plusieurs formats standard ou définis par l’application. Toute autre application peut ensuite récupérer les données du presse-papiers, en choisissant parmi les formats disponibles qu’elle comprend. Le presse-papiers est un support Exchange très faiblement couplé, où les applications doivent uniquement s’accorder sur le format de données. Les applications peuvent résider sur le même ordinateur ou sur des ordinateurs différents sur un réseau.

**Point clé :** Toutes les applications doivent prendre en charge le presse-papiers pour les formats de données qu’ils comprennent. Par exemple, un éditeur de texte ou un traitement de texte doit pouvoir produire et accepter les données du presse-papiers dans un format de texte pur. Pour plus d’informations, consultez [presse-papiers](../dataxchg/clipboard.md).

## <a name="using-com-for-ipc"></a>Utilisation de COM pour IPC

Les applications qui utilisent OLE gèrent les *documents composés*, c’est-à-dire les documents constitués de données provenant de diverses applications différentes. OLE fournit des services qui facilitent l’appel des applications sur d’autres applications pour la modification des données. Par exemple, un traitement de texte qui utilise OLE peut incorporer un graphique dans une feuille de calcul. L’utilisateur peut démarrer la feuille de calcul automatiquement à partir du traitement de texte en choisissant le graphique incorporé pour la modification. OLE s’occupe du démarrage de la feuille de calcul et de la présentation du graphique pour la modification. Lorsque l’utilisateur quitte la feuille de calcul, le graphique est mis à jour dans le document de traitement de texte d’origine. La feuille de calcul semble être une extension du traitement de texte.

La base d’OLE est le modèle COM (Component Object Model). Un composant logiciel qui utilise COM peut communiquer avec un large éventail d’autres composants, y compris ceux qui n’ont pas encore été écrits. Les composants interagissent en tant qu’objets et clients. COM distribué étend le modèle de programmation COM pour qu’il fonctionne sur un réseau.

**Point clé :** OLE prend en charge les documents composés et permet à une application d’inclure des données incorporées ou liées qui, lorsqu’elles sont sélectionnées, démarrent automatiquement une autre application pour la modification des données. Cela permet à l’application d’être étendue par toute autre application qui utilise OLE. Les objets COM fournissent l’accès aux données d’un objet par le biais d’un ou plusieurs ensembles de fonctions associées, appelées *interfaces*. pour plus d’informations, consultez COM et ActiveX Object Services.

## <a name="using-data-copy-for-ipc"></a>Utilisation de la copie de données pour IPC

La copie de données permet à une application d’envoyer des informations à une autre application à l’aide du message [**WM \_ COPYDATA**](../dataxchg/wm-copydata.md) . Cette méthode nécessite une collaboration entre l’application émettrice et l’application réceptrice. L’application réceptrice doit connaître le format des informations et être en mesure d’identifier l’expéditeur. L’application émettrice ne peut pas modifier la mémoire référencée par les pointeurs.

**Point clé :** la copie de données peut être utilisée pour envoyer rapidement des informations à une autre application à l’aide de la messagerie Windows. Pour plus d’informations, consultez [copie de données](../dataxchg/data-copy.md).

## <a name="using-dde-for-ipc"></a>Utilisation de DDE pour IPC

DDE est un protocole qui permet aux applications d’échanger des données dans différents formats. Les applications peuvent utiliser DDE pour les échanges de données à usage unique ou pour les échanges en cours dans lesquels les applications se mettent à jour à mesure que de nouvelles données deviennent disponibles.

Les formats de données utilisés par DDE sont les mêmes que ceux utilisés par le presse-papiers. DDE peut être considéré comme une extension du mécanisme de presse-papiers. Le presse-papiers est presque toujours utilisé pour une réponse ponctuelle à une commande utilisateur, comme le choix de la commande coller dans un menu. DDE est également généralement initié par une commande utilisateur, mais continue à fonctionner sans intervention supplémentaire de l’utilisateur. Vous pouvez également définir des formats de données DDE personnalisés pour IPC à usage spécifique entre des applications avec des exigences de communication plus étroitement couplées.

Les échanges DDE peuvent se produire entre des applications qui s’exécutent sur le même ordinateur ou sur des ordinateurs différents sur un réseau.

**Point clé :** DDE n’est pas aussi efficace que les nouvelles technologies. Toutefois, vous pouvez toujours utiliser DDE si d’autres mécanismes IPC ne sont pas appropriés ou si vous devez interagir avec une application existante qui prend uniquement en charge DDE. pour plus d’informations, consultez [échange dynamique de données](../dataxchg/dynamic-data-exchange.md) et [échange dynamique de données bibliothèque de gestion](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Utilisation d’un mappage de fichiers pour IPC

Le *mappage de fichiers* permet à un processus de traiter le contenu d’un fichier comme s’il s’agissait d’un bloc de mémoire dans l’espace d’adressage du processus. Le processus peut utiliser des opérations de pointeur simples pour examiner et modifier le contenu du fichier. Quand deux ou plusieurs processus accèdent au même mappage de fichier, chaque processus reçoit un pointeur vers la mémoire dans son propre espace d’adressage qu’il peut utiliser pour lire ou modifier le contenu du fichier. Les processus doivent utiliser un objet de synchronisation, tel qu’un sémaphore, pour empêcher l’endommagement des données dans un environnement multitâche.

Vous pouvez utiliser un cas particulier de mappage de fichiers pour fournir une *mémoire partagée nommée* entre les processus. Si vous spécifiez le fichier de permutation du système lors de la création d’un objet de mappage de fichiers, l’objet de mappage de fichiers est traité comme un bloc de mémoire partagée. D’autres processus peuvent accéder au même bloc de mémoire en ouvrant le même objet de mappage de fichier.

Le mappage de fichiers est très efficace et fournit également des attributs de sécurité pris en charge par le système d’exploitation qui peuvent contribuer à empêcher l’endommagement des données non autorisées. Le mappage de fichier peut être utilisé uniquement entre des processus sur un ordinateur local ; elle ne peut pas être utilisée sur un réseau.

**Point clé :** Le mappage de fichiers est un moyen efficace pour deux ou plusieurs processus sur le même ordinateur de partager des données, mais vous devez assurer la synchronisation entre les processus. Pour plus d’informations, consultez mappage et [synchronisation](/windows/desktop/Sync/synchronization)de [fichiers](/windows/desktop/Memory/file-mapping) .

## <a name="using-a-mailslot-for-ipc"></a>Utilisation d’un mailslot pour IPC

Les mailslots fournissent une communication unidirectionnelle. Tout processus qui crée un mailslot est un *serveur mailslot*. D’autres processus, appelés *clients mailslot*, envoient des messages au serveur mailslot en écrivant un message sur son mailslot. Les messages entrants sont toujours ajoutés au mailslot. La mailslot enregistre les messages jusqu’à ce que le serveur mailslot les ait lus. Un processus peut être à la fois un serveur mailslot et un client mailslot, de sorte que la communication bidirectionnelle est possible à l’aide de plusieurs mailslots.

Un client mailslot peut envoyer un message à une messagerie mailslot sur son ordinateur local, à un mailslot sur un autre ordinateur ou à toutes les mailslots portant le même nom sur tous les ordinateurs d’un domaine réseau spécifié. Les messages diffusés à toutes les mailslots d’un domaine ne peuvent pas dépasser 400 octets, tandis que les messages envoyés à une seule mailslot sont limités par la taille de message maximale spécifiée par le serveur mailslot lors de la création du mailslot.

**Point clé :** Les mailslots offrent aux applications un moyen simple d’envoyer et de recevoir des messages courts. Ils offrent également la possibilité de diffuser des messages sur tous les ordinateurs d’un domaine réseau. Pour plus d’informations, consultez les [mailslots](mailslots.md).

## <a name="using-pipes-for-ipc"></a>Utilisation de canaux pour IPC

Il existe deux types de canaux pour la communication bidirectionnelle : les canaux anonymes et les canaux nommés. Les *canaux anonymes* permettent aux processus associés de transférer des informations entre eux. En règle générale, un canal anonyme est utilisé pour rediriger l’entrée ou la sortie standard d’un processus enfant afin qu’il puisse échanger des données avec son processus parent. Pour échanger des données dans les deux sens (opération duplex), vous devez créer deux canaux anonymes. Le processus parent écrit des données sur un canal à l’aide de son handle d’écriture, tandis que le processus enfant lit les données de ce canal à l’aide de son handle de lecture. De même, le processus enfant écrit des données dans l’autre canal et le processus parent les lit. Les canaux anonymes ne peuvent pas être utilisés sur un réseau et ne peuvent pas être utilisés entre des processus non liés.

Les *canaux nommés* sont utilisés pour transférer des données entre des processus qui ne sont pas liés à des processus et entre des processus sur des ordinateurs différents. En règle générale, un processus serveur de canal nommé crée un canal nommé avec un nom connu ou un nom qui doit être communiqué à ses clients. Un processus client de canal nommé qui connaît le nom du canal peut ouvrir son autre extrémité, sous réserve des restrictions d’accès spécifiées par le processus serveur de canal nommé. Une fois que le serveur et le client sont connectés au canal, ils peuvent échanger des données en effectuant des opérations de lecture et d’écriture sur le canal.

**Point clé :** Les canaux anonymes offrent un moyen efficace de rediriger l’entrée ou la sortie standard vers des processus enfants sur le même ordinateur. Les canaux nommés fournissent une interface de programmation simple pour transférer des données entre deux processus, qu’ils résident sur le même ordinateur ou sur un réseau. Pour plus d’informations, consultez [canaux](pipes.md).

## <a name="using-rpc-for-ipc"></a>Utilisation de RPC pour IPC

RPC permet aux applications d’appeler des fonctions à distance. Par conséquent, RPC rend IPC aussi simple que l’appel d’une fonction. RPC fonctionne entre les processus sur un seul ordinateur ou sur différents ordinateurs sur un réseau.

le RPC fourni par Windows est conforme à l’environnement de calcul distribué OSF (Open Software Foundation). Cela signifie que les applications qui utilisent RPC sont en mesure de communiquer avec les applications exécutées avec d’autres systèmes d’exploitation qui prennent en charge DCE. RPC prend automatiquement en charge la conversion des données pour prendre en compte les différentes architectures matérielles et l’ordre des octets entre les environnements dissemblables.

Les clients et les serveurs RPC sont étroitement couplés, tout en continuant à assurer des performances élevées. Le système utilise largement RPC pour faciliter une relation client/serveur entre les différentes parties du système d’exploitation.

**Point clé :** RPC est une interface de niveau fonction, avec prise en charge de la conversion de données automatique et pour les communications avec d’autres systèmes d’exploitation. À l’aide de RPC, vous pouvez créer des applications distribuées hautement performantes et étroitement couplées. Pour plus d’informations, consultez [composants Microsoft RPC](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>utilisation de Windows sockets pour IPC

Windows Sockets est une interface indépendante du protocole. Elle tire parti des fonctionnalités de communication des protocoles sous-jacents. dans Windows sockets 2, un handle de socket peut éventuellement être utilisé comme handle de fichier avec les fonctions d’e/s de fichier standard.

Windows Les sockets sont basés sur les sockets d’abord répandus par Berkeley Software Distribution (BSD). une application qui utilise Windows sockets peut communiquer avec d’autres implémentations de socket sur d’autres types de systèmes. Toutefois, tous les fournisseurs de services de transport ne prennent pas en charge toutes les options disponibles.

**Point clé :** Windows sockets est une interface indépendante du protocole qui prend en charge les fonctionnalités de mise en réseau actuelles et émergentes. pour plus d’informations, consultez [Windows sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
