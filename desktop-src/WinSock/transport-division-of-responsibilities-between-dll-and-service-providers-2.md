---
description: Cette section fournit une vue d’ensemble de la répartition des responsabilités entre les \_32.dll Ws2 et les fournisseurs de services de transport.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Division de transport des responsabilités entre la DLL et les fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c256cb03bcc9e3f8746db5196c21fc2de0a8b157304a205587b275acc0bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733219"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Division de transport des responsabilités entre la DLL et les fournisseurs de services

Cette section fournit une vue d’ensemble de la répartition des responsabilités entre les \_32.dll Ws2 et les fournisseurs de services de transport.

## <a name="ws2_32dll-functionality-for-transport"></a>La \_ fonctionnalité Ws232.dll pour le transport

La principale tâche de la partie transport de données de la \_32.dll Ws2 est de servir de Traffic Manager entre les fournisseurs de services et les applications. Avec plusieurs fournisseurs de services différents qui interagissent avec la même application, chaque fournisseur de services interagit strictement avec la \_32.dll Ws2. La DLL s’occupe des éléments suivants :

-   Sélection d’un fournisseur de services approprié pour la création de sockets en fonction d’une description de protocole.
-   Transfert des appels de procédure d’application impliquant un socket au fournisseur de services approprié qui a créé ou contrôle ce Socket. Les fournisseurs de services ignorent ce qui se passe.

Ils n’ont pas besoin de se préoccuper des détails de l’interopérabilité entre eux, et même de l’existence d’autres fournisseurs de services. En faisant abstraction des fournisseurs de services dans une interface DLL cohérente et en exécutant cette fonction automatique de routage du trafic, la \_32.dll Ws2 permet aux applications d’interagir avec un grand nombre de fournisseurs sans que les applications aient besoin de connaître les divisions entre les fournisseurs, où les différents fournisseurs sont installés.

Le \_32.dll Ws2 s’appuie sur les paramètres des fonctions de création de sockets API ( [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)) pour déterminer quel fournisseur de service utiliser. Le fournisseur de services de transport sélectionné sera appelé via la fonction [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . Dans le cas de la fonction **Socket** , le \_32.dll Ws2 recherche la première entrée dans le jeu de structures [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) installées qui correspond aux valeurs fournies dans le tuple formé par les paramètres (*famille d’adresses*, type de *Socket*, *protocole*). Pour préserver la compatibilité descendante, l' \_32.dll Ws2 traite la valeur de zéro pour la *famille d’adresses* ou le type de *Socket* comme une valeur générique. La valeur zéro pour le protocole n’est pas considérée comme une valeur générique par l' \_32.dll Ws2, sauf si un tel comportement est indiqué pour un protocole particulier en faisant en sorte que le PFL \_ corresponde à l’indicateur de \_ protocole \_ Zero défini dans la structure **WSAPROTOCOL \_ info** .

Pour la fonction [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , si null est fourni pour *lpProtocolInfo*, le comportement est exactement le même que celui décrit pour [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). Toutefois, si une structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) est référencée, le \_32.dll Ws2 n’exécute aucune fonction correspondante mais relaie immédiatement la demande de création de socket au fournisseur de services de transport associé à la structure d' **\_ informations WSAPROTOCOL** indiquée. Les valeurs du tuple (*famille d’adresses,* *type de socket,*) sont fournies intactes au fournisseur de services dans la fonction [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . Les fournisseurs de services sont libres d’ignorer ou de prêter attention aux valeurs des paramètres (*famille d’adresses,* *type de socket,*) comme il convient, mais ils ne doivent pas indiquer une condition d’erreur lorsque la valeur de la *famille d’adresses* ou du type de *Socket* est égale à zéro. En outre, les fournisseurs de services ne doivent pas indiquer une condition d’erreur lorsque la constante de manifeste des \_ informations de protocole \_ est contenue dans l’un des paramètres (*famille d’adresses,* *type de socket,*). Cette valeur indique simplement que l’application souhaite utiliser les valeurs trouvées dans les paramètres correspondants de la structure **WSAPROTOCOL \_ info** : (**iAddressFamily**, **iSocketType**, **iProtocol**).

Dans le cadre de la création de sockets, un fournisseur de services informe le Ws2 \_32.dll sur l’association entre lui-même et le nouveau socket à l’aide de paramètres passés à [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) ou [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). La \_32.dll Ws2 effectue le suivi de cette association entre les descripteurs de socket et les fournisseurs de services particuliers. Chaque fois qu’une fonction d’interface d’application qui fait référence à un handle de socket est appelée, le Ws2 \_32.dll recherche l’Association et appelle la fonction d’interface du fournisseur de services correspondante du fournisseur de services approprié.

En plus de son service de routage de trafic majeur, le \_32.dll Ws2 fournit un certain nombre d’autres services, tels que l’énumération de protocole, la gestion du descripteur de socket (allocation). désallocation et Association de valeur de contexte pour les fournisseurs de services de système non-fichier, blocage de \_ la gestion des raccordements par thread, utilitaires de permutation d’octets, mise en file d’attente d’appels de procédure asynchrone (APC) pour faciliter l’appel de routines de saisie semi-automatique d’e32.dll32.dll \_

## <a name="transport-service-provider-functionality"></a>Fonctionnalités du fournisseur de services de transport

Les fournisseurs de services implémentent le protocole de transport réel, qui comprend des fonctions telles que la configuration des connexions, le transfert de données, l’exercice du contrôle de workflow et du contrôle des erreurs, etc. Le32.dll Ws2 n' \_ a aucune connaissance de la façon dont les demandes aux fournisseurs de services sont réalisées. il s’agit de l’implémentation du fournisseur de services. L’implémentation de telles fonctions peut varier d’un fournisseur à l’autre. Les fournisseurs de services masquent les détails spécifiques à l’implémentation de la façon dont les opérations réseau sont effectuées.

Les fournisseurs de services de transport peuvent être divisés en deux catégories : ceux dont les descripteurs de socket sont des handles de système de fichiers réels (et sont ci-après appelés fournisseurs IFS). les autres sont appelés fournisseurs non-IFS. l' \_32.dll Ws2 transmet toujours le descripteur de socket du fournisseur de services de transport à l’application Windows sockets, de sorte que les applications sont libres de tirer parti des descripteurs de socket qui sont des handles de système de fichiers, si c’est le cas.

Pour résumer : les fournisseurs de services implémentent les protocoles de bas niveau spécifiques au réseau. Le \_32.dll Ws2 fournit la gestion du trafic de niveau moyen qui interconnecte ces protocoles de transport avec les applications. Les applications fournissent à leur tour la stratégie quant à la façon dont ces flux de trafic et les opérations spécifiques au réseau sont utilisés pour accomplir les fonctions souhaitées par l’utilisateur.

 

 
