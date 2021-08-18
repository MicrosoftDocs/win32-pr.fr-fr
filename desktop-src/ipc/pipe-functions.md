---
description: La fonction suivante est utilisée avec les canaux anonymes.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Fonctions de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481603"
---
# <a name="pipe-functions"></a>Fonctions de canal

La fonction suivante est utilisée avec les canaux anonymes.



| Fonction                         | Description                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Crée un canal anonyme. |



 

Les fonctions suivantes sont utilisées avec les canaux nommés.



| Fonction                                                                 | Description                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Établit une connexion à un canal de type message, écrit dans le canal et les lit, puis ferme le canal.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Permet à un processus de serveur de canal nommé d’attendre qu’un processus client se connecte à une instance d’un canal nommé.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Crée une instance d’un canal nommé et retourne un handle pour les opérations de canal ultérieures. Un processus client se connecte à un canal nommé à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Déconnecte l’extrémité serveur d’une instance de canal nommé d’un processus client.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Récupère le nom de l’ordinateur client pour le canal nommé spécifié.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Récupère l’identificateur de processus client pour le canal nommé spécifié.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Récupère l’identificateur de session client pour le canal nommé spécifié.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Récupère des informations sur un canal nommé spécifié.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Récupère des informations sur le canal nommé spécifié.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Récupère l’identificateur de processus serveur pour le canal nommé spécifié.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Récupère l’identificateur de session serveur pour le canal nommé spécifié.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Emprunte l’identité d’une application cliente de canal nommé.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copie les données d’un canal nommé ou anonyme dans une mémoire tampon sans la supprimer du canal.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Définit le mode de lecture et le mode de blocage du canal nommé spécifié.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combine les fonctions qui écrivent un message et lit un message du canal nommé spécifié dans une opération de réseau unique.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Attend qu’un intervalle de délai d’attente soit écoulé ou qu’une instance du canal nommé spécifié soit disponible pour une connexion.                                                                                                            |



 

 

 
