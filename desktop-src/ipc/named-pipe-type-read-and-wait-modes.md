---
description: Le serveur de canaux spécifie le mode de type de canal, le mode lecture et le mode Wait dans le paramètre dwPipeMode de la fonction CreateNamedPipe. Les clients de canal peuvent spécifier ces modes de canal pour leurs handles de canal à l’aide de la fonction CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Modes de type canal nommé, lecture et attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014889"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Modes de type canal nommé, lecture et attente

Le serveur de canaux spécifie le mode de type de canal, le mode lecture et le mode Wait dans le paramètre *dwPipeMode* de la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Les clients de canal peuvent spécifier ces modes de canal pour leurs handles de canal à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="type-mode"></a>Mode de type

Le mode de type d’un canal détermine la façon dont les données sont écrites dans un canal nommé. Les données peuvent être transmises via un canal nommé en tant que flux d’octets ou en tant que flux de messages. Le serveur de canaux spécifie le type de canal lors de l’appel de [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) pour créer une instance d’un canal nommé. Les modes de type doivent être les mêmes pour toutes les instances d’un canal.

Pour créer un canal de type octet, spécifiez \_ octet type de canal \_ ou utilisez la valeur par défaut. Les données sont écrites dans le canal sous la forme d’un flux d’octets et le système ne fait pas la différence entre les octets écrits dans des opérations d’écriture différentes.

Pour créer un canal de type de message, spécifiez le message de type de canal \_ \_ . Le système traite les octets écrits dans chaque opération d’écriture sur le canal en tant qu’unité de message. Le système effectue toujours des opérations d’écriture sur les canaux de type message comme si le mode d’écriture directe était activé.

## <a name="read-mode"></a>Mode lecture

Le mode de lecture d’un canal détermine la façon dont les données sont lues à partir d’un canal nommé. Le serveur de canal spécifie le mode de lecture initial pour un handle de canal lors de l’appel de [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). Les données peuvent être lues en mode lecture en octets ou en mode lecture de message. Un handle vers un canal de type octet peut être en mode lecture octet uniquement. Un handle vers un canal de type de message peut être en lecture octet ou en mode de lecture de message. Pour un canal de type de message, le mode de lecture peut être différent pour les handles de serveur et de client vers la même instance de canal.

Pour créer le descripteur de canal en mode lecture octet, spécifiez canal \_ READMODE \_ octet ou utilisez la valeur par défaut. Les données sont lues à partir du canal sous la forme d’un flux d’octets. Une opération de lecture s’est terminée correctement lorsque tous les octets disponibles dans le canal sont lus ou lorsque le nombre d’octets spécifié est lu.

Pour créer le descripteur de canal en mode de lecture de message, spécifiez le \_ message READMODE du canal \_ . Les données sont lues à partir du canal sous la forme d’un flux de messages. Une opération de lecture ne se termine correctement que lorsque le message entier est lu. Si le nombre d’octets spécifié à lire est inférieur à la taille du message suivant, la fonction lit la plus grande partie possible du message avant de retourner zéro (la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ plus de \_ données). Le reste du message peut être lu à l’aide d’une autre opération de lecture.

Pour un client de canal, un handle de canal retourné par [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) est toujours en mode lecture octet initialement. Les clients de canal et les serveurs de canaux peuvent utiliser la fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) pour modifier le mode de lecture d’un handle de canal. Le handle de canal doit avoir le \_ droit d’accès écriture de fichier \_ .

## <a name="wait-mode"></a>Mode attente

Le mode d’attente d’un descripteur de canal détermine la façon dont les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) gèrent les opérations de longue durée. En mode d’attente de blocage, les fonctions attendent indéfiniment un processus à l’autre extrémité du canal pour terminer une opération. En mode attente sans blocage, les fonctions retournent immédiatement dans les situations qui nécessiteraient normalement une attente indéterminée.

Une opération [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) est affectée par le mode d’attente d’un handle de canal quand le canal est vide. Avec un handle d’attente de blocage, l’opération ne se termine pas correctement tant que les données ne sont pas disponibles à partir d’un thread qui écrit à l’autre extrémité du canal. À l’aide d’un handle d’attente sans blocage, la fonction retourne immédiatement zéro, et la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ aucune \_ donnée.

Une opération [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) est affectée par le mode d’attente d’un handle de canal quand l’espace est insuffisant dans la mémoire tampon du canal. Avec un handle d’attente de blocage, l’opération d’écriture ne peut pas être effectuée tant qu’un espace suffisant n’a pas été créé dans la mémoire tampon par un thread lisant à l’autre extrémité du canal. Avec un handle d’attente sans blocage, l’opération d’écriture retourne immédiatement une valeur différente de zéro, sans écrire d’octets (pour un canal de type de message) ou après avoir écrit autant d’octets que la mémoire tampon contient (pour un canal de type octet).

Une opération [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) est affectée par le mode d’attente d’un handle de canal quand aucun client n’est connecté ou en attente de connexion à l’instance de canal. Avec un handle d’attente de blocage, l’opération de connexion ne fonctionne pas tant qu’un client de canal ne se connecte pas à l’instance de canal en appelant la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Avec un handle d’attente sans blocage, l’opération de connexion retourne immédiatement zéro, et la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le canal d’erreur à l' \_ \_ écoute.

Par défaut, tous les descripteurs de canaux nommés retournés par la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ou [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) sont créés avec le mode d’attente de blocage activé. Pour créer le canal en mode de non-blocage-Wait, le serveur de canaux spécifie la valeur de la barre d’attente de canal lors de l' \_ appel de **CreateNamedPipe**.

Les clients de canal et les serveurs de canal peuvent modifier le mode d’attente d’un handle de canal en spécifiant l’attente de canal \_ ou la valeur de canal \_ d’attente dans un appel à la fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .

> [!Note]  
> Le mode d’attente sans blocage est pris en charge pour la compatibilité avec Microsoft LAN Manager version 2,0. Ce mode ne doit pas être utilisé pour obtenir une entrée et une sortie (e/s) avec des canaux nommés. Les e/s avec chevauchement doivent être utilisées à la place, car elles permettent aux opérations de longue durée de s’exécuter en arrière-plan après le retour de la fonction. Pour plus d’informations sur les e/s avec chevauchement, consultez [entrées et sorties synchrones et avec chevauchement](synchronous-and-overlapped-input-and-output.md).

 

 

 
