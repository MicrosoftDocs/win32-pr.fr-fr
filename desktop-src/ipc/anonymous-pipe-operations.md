---
description: Opérations de canal anonyme, y compris la création de canal, l’écriture dans un canal, les handles de canal.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Opérations de canal anonyme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963d7127c51859b05e570d00291470a49be5ba66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122281"
---
# <a name="anonymous-pipe-operations"></a>Opérations de canal anonyme

La fonction [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) crée un canal anonyme et retourne deux Handles : un handle de lecture vers le canal et un handle d’écriture sur le canal. Le handle de lecture a un accès en lecture seule au canal et le handle d’écriture dispose d’un accès en écriture seule au canal. Pour communiquer à l’aide du canal, le serveur de canaux doit passer un handle de canal à un autre processus. En général, cette opération est effectuée par héritage ; autrement dit, le processus permet à un handle d’être hérité par un processus enfant. Le processus peut également dupliquer un handle de canal à l’aide de la fonction [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) et l’envoyer à un processus non lié à l’aide d’une forme de communication interprocessus, telle que DDE ou la mémoire partagée.

Un serveur de canaux peut envoyer le descripteur de lecture ou le descripteur d’écriture au client du canal, selon que le client doit ou non utiliser le canal anonyme pour envoyer des informations ou recevoir des informations. Pour lire à partir du canal, utilisez la poignée de lecture du canal dans un appel à la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . L’appel à **ReadFile** retourne lorsqu’un autre processus a écrit sur le canal. L’appel **ReadFile** peut également retourner si tous les descripteurs d’écriture du canal ont été fermés ou si une erreur se produit avant la fin de l’opération de lecture.

Pour écrire dans le canal, utilisez le handle d’écriture du canal dans un appel à la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) . L’appel **WriteFile** ne retourne pas jusqu’à ce qu’il ait écrit le nombre d’octets spécifié dans le canal ou qu’une erreur se produise. Si la mémoire tampon du canal est pleine et qu’il y a plus d’octets à écrire, **WriteFile** ne retourne pas jusqu’à ce qu’un autre processus Lise à partir du canal, ce qui rend plus l’espace de mémoire tampon disponible. Le serveur de canaux spécifie la taille de la mémoire tampon pour le canal lorsqu’il appelle [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe).

Les opérations de lecture et d’écriture asynchrones (avec chevauchement) ne sont pas prises en charge par les canaux anonymes. Cela signifie que vous ne pouvez pas utiliser les fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) avec des canaux anonymes. En outre, le paramètre *lpOverlapped* de [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) est ignoré lorsque ces fonctions sont utilisées avec des canaux anonymes.

Un canal anonyme existe jusqu’à ce que tous les descripteurs de canal, en lecture et en écriture, aient été fermés. Un processus peut fermer ses descripteurs de canal à l’aide de la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Tous les descripteurs de canal sont également fermés lorsque le processus se termine.

Les canaux anonymes sont implémentés à l’aide d’un canal nommé portant un nom unique. Par conséquent, vous pouvez souvent transmettre un handle à un canal anonyme vers une fonction qui requiert un handle vers un canal nommé.

 

 
