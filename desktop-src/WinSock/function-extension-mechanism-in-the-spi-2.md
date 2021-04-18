---
description: Étant donné que la DLL WinSock proprement dite n’est plus fournie par chaque fournisseur de pile, il n’est pas possible pour un fournisseur de pile d’offrir des fonctionnalités étendues en ajoutant des points d’entrée à la DLL WinSock.
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: Mécanisme d’extension de fonction dans l’index SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cfa6c9dfaf3afcec8e6861a9a0d3545a7ed0c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519299"
---
# <a name="function-extension-mechanism-in-the-spi"></a>Mécanisme d’extension de fonction dans l’index SPI

Étant donné que la DLL WinSock proprement dite n’est plus fournie par chaque fournisseur de pile, il n’est pas possible pour un fournisseur de pile d’offrir des fonctionnalités étendues en ajoutant des points d’entrée à la DLL WinSock. Pour surmonter cette limitation, Winsock tire parti de la nouvelle fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) pour s’adapter aux fournisseurs de services qui souhaitent offrir des extensions de fonctionnalités spécifiques au fournisseur. Ce mécanisme suppose qu’une application connaît une extension particulière et comprend la sémantique et la syntaxe impliquées. Ces informations sont généralement fournies par le fournisseur du fournisseur de services.

Pour appeler une fonction d’extension, l’application doit d’abord demander un pointeur vers la fonction souhaitée. Pour ce faire, utilisez la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) en utilisant \_ le \_ Code de commande du pointeur de fonction d’extension SIO \_ \_ . La mémoire tampon d’entrée de la fonction **WSAIoctl** contient un identificateur pour la fonction d’extension souhaitée et la mémoire tampon de sortie contiendra le pointeur de fonction lui-même. L’application peut ensuite appeler la fonction d’extension directement sans passer par le \_32.dll Ws2.

Les identificateurs assignés aux fonctions d’extension sont des identificateurs globaux uniques (GUID) qui sont alloués par les fournisseurs de fournisseurs de services. Les fournisseurs qui créent des fonctions d’extension sont invités à publier des détails complets sur la fonction, y compris la syntaxe du prototype de fonction. Cela facilite la proposition de fonctions d’extension communes et/ou populaires par plusieurs fournisseurs de services. Une application peut obtenir le pointeur de fonction et utiliser la fonction sans avoir à connaître le fournisseur de services qui implémente la fonction.

 

 



