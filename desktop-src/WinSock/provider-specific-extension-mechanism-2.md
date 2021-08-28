---
description: La fonction WSAIoctl permet aux fournisseurs de services d’offrir des extensions de fonctionnalités spécifiques au fournisseur.
ms.assetid: 8b0d86ad-2f8b-4f5e-a8a6-839cb8dba4d8
title: Provider-Specific mécanisme d’extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed627aefdfefda2bf4b395098f6680086fd37dd7a302d977d9bf238f77d89d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733569"
---
# <a name="provider-specific-extension-mechanism"></a>Provider-Specific mécanisme d’extension

La fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permet aux fournisseurs de services d’offrir des extensions de fonctionnalités spécifiques au fournisseur. Ce mécanisme suppose, bien sûr, qu’une application soit consciente d’une extension particulière et comprenne la sémantique et la syntaxe impliquées. Ces informations sont généralement fournies par le fournisseur du fournisseur de services.

Pour appeler une fonction d’extension, l’application doit d’abord demander un pointeur vers la fonction souhaitée. Pour ce faire, utilisez la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) en utilisant \_ le \_ Code de commande du pointeur de fonction d’extension SIO \_ \_ . La mémoire tampon d’entrée de **WSAIoctl** contient un identificateur pour la fonction d’extension souhaitée, tandis que la mémoire tampon de sortie contient le pointeur de fonction lui-même. L’application peut ensuite appeler la fonction d’extension directement sans passer par le \_32.dll Ws2.

Les identificateurs assignés aux fonctions d’extension sont des identificateurs globaux uniques (GUID) qui sont alloués par les fournisseurs de fournisseurs de services. Les fournisseurs qui créent des fonctions d’extension sont invités à publier des détails complets sur la fonction, y compris la syntaxe du prototype de fonction. Cela permet à plusieurs fournisseurs de fournisseurs de services d’offrir des fonctions d’extension communes et populaires. Une application peut obtenir le pointeur de fonction et utiliser la fonction sans avoir à connaître le fournisseur de services qui implémente la fonction.

sur Windows Vista et versions ultérieures, les nouvelles extensions système winsock sont exportées directement à partir de la DLL winsock. la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) n’est donc pas nécessaire pour charger ces extensions. les nouvelles fonctions d’extension disponibles sur Windows Vista et versions ultérieures incluent les fonctions [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) et [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) exportées à partir de *Ws2 \_32.dll*.

 

 
