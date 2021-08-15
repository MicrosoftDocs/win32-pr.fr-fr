---
description: Les pages de l’espace d’adressage virtuel d’un processus peuvent avoir l’un des États suivants.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: État de la page
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ec9c162220cd0c1accdb35e35309082a2e94c4af6023af7e7d9d7cd55be620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386402"
---
# <a name="page-state"></a>État de la page

Les pages de l’espace d’adressage virtuel d’un processus peuvent avoir l’un des États suivants.



| État     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuit      | La page n’est ni validée ni réservée. La page n’est pas accessible au processus. Elles peuvent être réservées, validées ou réservées et validées simultanément. Toute tentative de lecture ou d’écriture dans une page libre entraîne une exception de violation d’accès. <br/> Un processus peut utiliser la fonction [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) pour libérer les pages réservées ou validées de son espace d’adressage, en les renvoyant à l’État libre.<br/>                                                                                                                                                                                                                                                                                                                              |
| Réservé  | La page a été réservée pour une utilisation ultérieure. La plage d’adresses ne peut pas être utilisée par d’autres fonctions d’allocation. La page n’est pas accessible et n’est associée à aucun stockage physique. Elle est disponible pour être validée. <br/> Un processus peut utiliser la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) pour réserver des pages de son espace d’adressage et ultérieurement pour valider les pages réservées. Elle peut utiliser [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) ou [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) pour désengager les pages validées et les retourner à l’État réservé.<br/>                                                                                                                                                                                                                          |
| Committed | Des frais de mémoire ont été alloués à partir de la taille globale de la mémoire RAM et des fichiers d’échange sur le disque. La page est accessible et l’accès est contrôlé par l’une des [constantes de protection](memory-protection-constants.md)de la mémoire. Le système initialise et charge chaque page validée dans la mémoire physique uniquement lors de la première tentative de lecture ou d’écriture sur cette page. Lorsque le processus se termine, le système libère le stockage pour les pages validées. <br/> Un processus peut utiliser [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) ou [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) pour valider des pages physiques à partir d’une région réservée. Ils peuvent également réserver et valider des pages simultanément.<br/> Les fonctions [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) et [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) allouent des pages validées avec un accès en lecture/écriture.<br/> |



 

 

 
