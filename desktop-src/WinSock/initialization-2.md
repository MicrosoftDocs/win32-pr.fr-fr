---
description: le \_32.dll Ws2 charge la DLL d’interface du fournisseur de services dans le système à l’aide des mécanismes de chargement de bibliothèque dynamique Microsoft Windows standard et l’initialise en appelant WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76570fe401fb064047581a60a4340daf71b5a583034baf67b8e9b830ccae0dc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097869"
---
# <a name="initialization"></a>Initialisation

le *\_32.dllWs2* charge la DLL d’interface du fournisseur de services dans le système à l’aide des mécanismes de chargement de bibliothèque dynamique Microsoft Windows standard et l’initialise en appelant [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Cette valeur est généralement déclenchée par une application qui appelle [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) pour créer un socket à associer à un fournisseur de services dont la dll d’interface n’est pas actuellement chargée en mémoire. Le chemin d’accès à chaque DLL d’interface du fournisseur de services est stocké par le *\_32.dllWs2* au moment de l’installation du fournisseur de services. Pour plus d’informations, consultez [fonctions d’installation et de configuration](installation-and-configuration-functions-2.md) .

Au fil du temps, différentes versions peuvent exister pour les dll, les applications et les fournisseurs de services Winsock. Les nouvelles versions peuvent définir de nouvelles fonctionnalités et de nouveaux paramètres pour les structures de données et les paramètres de bits, etc. Les numéros de version indiquent donc comment interpréter diverses structures de données.

Pour permettre un mixage optimal et une correspondance avec les différentes versions d’applications, les versions de l' \_32.dll Ws2 et les versions des fournisseurs de services par différents fournisseurs, le SPI fournit un mécanisme de négociation de version pour une utilisation entre le *\_32.dllWs2* et les fournisseurs de services. Cette négociation de version est gérée par [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). En fait, le *Ws2 \_32.dll* transmet au fournisseur de service les numéros de version les plus élevés avec lesquels il est compatible. Le fournisseur de services compare ce avec sa propre plage de numéros de version prise en charge. Si ces plages se chevauchent, le fournisseur de services retourne une valeur dans la partie chevauchante de la plage en tant que résultat de la négociation. En règle générale, il doit s’agir de la valeur la plus élevée possible. Si les plages ne se chevauchent pas, les deux parties sont incompatibles et la fonction retourne une erreur.

[**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) doit être appelé au moins une fois par chaque processus client et peut être appelé plusieurs fois par Ws2 \_32.dll ou d’autres entités. Un [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) correspondant doit être appelé pour chaque appel **WSPStartup** réussi. Le fournisseur de services doit conserver un décompte de références pour chaque processus. À chaque appel de **WSPStartup** , l’appelant peut spécifier n’importe quel numéro de version pris en charge par la dll SP.

Un fournisseur de services doit stocker le pointeur vers la table de distribution des appels de client qui est reçue en tant que paramètre [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) pour chaque processus. Si un processus donné appelle plusieurs fois **WSPStartup** , le fournisseur de services doit utiliser uniquement le pointeur de table de dispatch fourni le plus récemment.

Dans le cadre du processus d’initialisation du fournisseur de services, le \_32.dll Ws2 récupère la table de dispatch du fournisseur de services via le paramètre *lpProcTable* afin d’obtenir des points d’entrée pour le reste des fonctions SPI spécifiées dans ce document.

L’utilisation d’une table de dispatch (par opposition aux mécanismes de DLL habituels pour l’accès aux points d’entrée) remplit deux fonctions :

-   Il est plus pratique pour la32.dll Ws2, \_ car un seul appel peut être fait pour découvrir l’ensemble des points d’entrée.
-   Elle permet aux fournisseurs de services en couche formés dans des chaînes de protocole de fonctionner plus efficacement.

## <a name="initializing-protocol-chains"></a>Initialisation des chaînes de protocole

Au moment où la structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour une chaîne de protocole est installée, le chemin d’accès au premier fournisseur superposé dans la chaîne est également spécifié. Quand une chaîne de protocole est initialisée, le \_32.dll Ws2 utilise ce chemin pour charger la dll du fournisseur, puis appelle [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Étant donné que **WSPStartup** contient un pointeur vers la structure **WSAPROTOCOL \_ info** de la chaîne comme l’un de ses paramètres, les fournisseurs superposés peuvent déterminer le type de chaîne dans lequel ils sont initialisés et l’identité de la couche inférieure suivante dans la chaîne. Un fournisseur superposé chargera ensuite le fournisseur de protocole suivant dans la chaîne et l’initialise avec un appel à **WSPStartup**, et ainsi de suite. Chaque fois que la couche inférieure suivante est un autre fournisseur superposé, la structure d' **\_ informations WSAPROTOCOL** de la chaîne doit être référencée dans l’appel **WSPStartup** . Lorsque la couche inférieure suivante est un protocole de base (signifiant la fin de la chaîne), la structure d' **\_ informations WSAPROTOCOL** de la chaîne n’est plus propagée vers le bas. Au lieu de cela, la couche actuelle doit faire référence à une structure **WSAPROTOCOL \_ info** qui correspond au protocole que le fournisseur de base doit utiliser. Ainsi, le fournisseur de base n’a aucune notion de impliqué dans une chaîne de protocole.

La table de dispatch fournie par un fournisseur superposé donné, dans de nombreux cas, duplique les points d’entrée d’un fournisseur sous-jacent. Le fournisseur superposé insère uniquement ses propres points d’entrée pour les fonctions dont il devait être directement impliqué. Notez, cependant, qu’il est impératif qu’un fournisseur en couches ne modifie pas le contenu de la table de l’appel qu’il a reçue lors de l’appel de [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) sur la couche inférieure suivante dans une chaîne de protocole. ces appels doivent être effectués directement sur la DLL Windows sockets 2.

 

 
