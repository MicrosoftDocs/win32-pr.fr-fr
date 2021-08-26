---
description: Un canal nommé est un canal nommé, unidirectionnel ou duplex pour la communication entre le serveur de canal et un ou plusieurs clients de canal.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Canaux nommés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06e7f291776e2ecba3b9da93a94d235d4fbe7df151353a7c3d379eb4d50fdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014899"
---
# <a name="named-pipes"></a>Canaux nommés

Un *canal nommé* est un canal nommé, unidirectionnel ou duplex pour la communication entre le serveur de canal et un ou plusieurs clients de canal. Toutes les instances d’un canal nommé partagent le même nom de canal, mais chaque instance possède ses propres tampons et Handles et fournit un canal de communication distinct pour la communication client/serveur. L’utilisation d’instances permet à plusieurs clients de canal d’utiliser simultanément le même canal nommé.

Tout processus peut accéder à des canaux nommés, soumis à des vérifications de sécurité, ce qui fait des canaux nommés une forme simple de communication entre les processus liés ou non associés.

Tout processus peut agir à la fois comme un serveur et un client, ce qui rend possible la communication d’égal à égal. Comme c’est le cas ici, le terme « serveur de canal » fait référence à un processus qui crée un canal nommé, et le terme « client de canal » fait référence à un processus qui se connecte à une instance d’un canal nommé. La fonction côté serveur pour instancier un canal nommé est [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). La fonction côté serveur pour accepter une connexion est [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe). Un processus client se connecte à un canal nommé à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .

Les canaux nommés peuvent être utilisés pour assurer la communication entre les processus sur le même ordinateur ou entre des processus sur différents ordinateurs sur un réseau. Si le service serveur est en cours d’exécution, tous les canaux nommés sont accessibles à distance. Si vous envisagez d’utiliser un canal nommé localement uniquement, refusez l’accès au réseau de l’autorité NT \\ ou basculez en RPC local.

Pour plus d'informations, voir les rubriques suivantes :

-   [Noms de canaux](pipe-names.md)
-   [Modes ouverts du canal nommé](named-pipe-open-modes.md)
-   [Modes de type canal nommé, lecture et attente](named-pipe-type-read-and-wait-modes.md)
-   [Instances de canal nommé](named-pipe-instances.md)
-   [Opérations de canal nommé](named-pipe-operations.md)
-   [Entrée et sortie synchrones et superposées](synchronous-and-overlapped-input-and-output.md)
-   [Sécurité des canaux nommés et droits d’accès](named-pipe-security-and-access-rights.md)
-   [Emprunt de l’identité d’un client de canal nommé](impersonating-a-named-pipe-client.md)
-   [Utilisation de canaux](using-pipes.md)

 

 
