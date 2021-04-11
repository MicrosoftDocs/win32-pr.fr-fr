---
description: Les opérations de canal, y compris les clients de canal et les serveurs, peuvent appeler l’une des fonctions suivantes, en plus de CallNamedPipe, pour lire et écrire dans un canal nommé.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Opérations de canal nommé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703189a129fc44b956ab65c2f70bbf88bfd22700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112023"
---
# <a name="named-pipe-operations"></a>Opérations de canal nommé

La première fois que le serveur de canal appelle la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) , il utilise le paramètre *nMaxInstances* pour spécifier le nombre maximal d’instances du canal qui peuvent exister simultanément. Le serveur peut appeler **CreateNamedPipe** à plusieurs reprises pour créer des instances supplémentaires du canal, à condition qu’il ne dépasse pas le nombre maximal d’instances. Si la fonction est réussie, chaque appel retourne un handle vers l’extrémité serveur d’une instance de canal nommé.

Dès que le serveur de canal crée une instance de canal, un client de canal peut s’y connecter en appelant la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Si une instance de canal est disponible, **CreateFile** retourne un handle à l’extrémité cliente de l’instance de canal. Si aucune instance du canal n’est disponible, un client de canal peut utiliser la fonction [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) pour attendre qu’un canal soit disponible.

Un serveur de canaux peut déterminer quand un client de canal est connecté à une instance de canal en appelant la fonction [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Si le handle de canal est en mode d’attente de blocage, **ConnectNamedPipe** ne retourne pas tant qu’un client n’est pas connecté.

Les clients et les serveurs de canal peuvent appeler l’une des fonctions suivantes, en plus de [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) , pour lire et écrire dans un canal nommé. Le comportement de ces fonctions dépend du type de canal et des modes en vigueur pour le handle de canal spécifié, comme suit :

-   Les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) peuvent être utilisées avec des canaux de type octet ou de type message.
-   Les fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) peuvent être utilisées avec des canaux de type octet ou de type de message si le handle de canal a été ouvert pour des opérations avec chevauchement.
-   La fonction [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) peut être utilisée pour lire sans supprimer le contenu d’un canal de type octet ou d’un canal de type message. **PeekNamedPipe** peut également retourner des informations supplémentaires sur l’instance de canal.
-   La fonction [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) peut être utilisée avec des canaux duplex de type message si le descripteur de canal vers le processus appelant est défini en mode de lecture de message. La fonction écrit un message de demande et lit un message de réponse en une seule opération, ce qui améliore les performances du réseau.

Le serveur de canal ne doit pas effectuer une opération de lecture de blocage tant que le client de canal n’a pas démarré. Dans le cas contraire, une condition de concurrence peut se produire. Cela se produit généralement lorsque le code d’initialisation, tel que celui de la bibliothèque Runtime C, doit verrouiller et examiner les handles hérités.

Quand un client et un serveur finissent par utiliser une instance de canal, le serveur doit d’abord appeler la fonction [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) pour s’assurer que tous les octets ou messages écrits sur le canal sont lus par le client. **FlushFileBuffers** ne retourne pas de données tant que le client n’a pas lu toutes les données du canal. Le serveur appelle ensuite la fonction [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) pour fermer la connexion au client du canal. Cette fonction rend le handle du client non valide, s’il n’a pas déjà été fermé. Toutes les données non lues dans le canal sont ignorées. Une fois le client déconnecté, le serveur appelle la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) pour fermer son handle vers l’instance de canal. Le serveur peut également utiliser [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) pour permettre à un nouveau client de se connecter à cette instance du canal.

Un processus peut récupérer des informations sur un canal nommé en appelant la fonction [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) , qui retourne le type du canal, la taille des mémoires tampons d’entrée et de sortie, et le nombre maximal d’instances de canal qui peuvent être créées. La fonction [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) signale les modes de lecture et d’attente d’un handle de canal, le nombre actuel d’instances de canal et des informations supplémentaires pour les canaux qui communiquent sur un réseau. La fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) définit le mode de lecture et les modes d’attente d’un handle de canal. Pour les clients de canal communiquant avec un serveur distant, la fonction contrôle également le nombre maximal d’octets à collecter ou la durée d’attente maximale avant la transmission d’un message (en supposant que le descripteur du client n’a pas été ouvert avec le mode écriture activée).

 

 
