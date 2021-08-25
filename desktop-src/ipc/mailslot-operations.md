---
description: Descriptions des fonctions à utiliser lors de l’utilisation des mailslots, des clients et des serveurs.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Opérations mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829499"
---
# <a name="mailslot-operations"></a>Opérations mailslot

Lorsque vous utilisez des mailslots, les clients et les serveurs doivent utiliser uniquement les fonctions décrites dans les tableaux suivants. N’utilisez pas d’autres fonctions, même si elles acceptent des handles de fichiers ou des noms de fichiers en tant que paramètres, car elles ne sont pas conçues pour fonctionner avec des mailslots.

## <a name="mailslot-server-functions"></a>Fonctions du serveur mailslot

Les serveurs mailslot ont une utilisation exclusive de trois fonctions, comme indiqué dans le tableau suivant.



| Fonction                                   | Description                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Crée un mailslot et retourne un handle mailslot.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Récupère la taille maximale des messages, la taille des messages MailSlot, la taille du message suivant dans le mailslot, le nombre de messages dans le mailslot et la durée pendant laquelle une opération de lecture peut attendre un message. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Modifie le délai d’attente de lecture pour un mailslot.                                                                                                                                                                    |



 

Les fonctions suivantes sont également utilisées par les serveurs mailslot.



| Fonction                                                         | Description                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplique le handle mailslot.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Récupère les messages d’un mailslot.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Récupère la date et l’heure de création d’un mailslot. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Définit la date et l’heure de création d’un mailslot.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Récupère les propriétés du handle mailslot.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Définit les propriétés du handle mailslot.             |



 

## <a name="mailslot-client-functions"></a>Fonctions du client mailslot

Un processus client utilise les fonctions suivantes lors de l’interaction avec un mailslot.



| Fonction                                                             | Description                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Ferme un handle mailslot pour un processus client.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Crée un handle de mailslot pour un processus client. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplique un handle de mailslot.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Écrit des données sur un mailslot.                      |



 

 

 
