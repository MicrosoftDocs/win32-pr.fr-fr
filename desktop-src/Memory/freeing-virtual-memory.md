---
description: La fonction VirtualFree annule la validation des pages et les libère conformément aux règles suivantes.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Libération de la mémoire virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094150"
---
# <a name="freeing-virtual-memory"></a>Libération de la mémoire virtuelle

La fonction [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) annule la validation des pages et les libère conformément aux règles suivantes :

-   Annule la validation d’une ou plusieurs pages validées, en remplaçant l’état des pages par réservé. La désactivation des pages libère le stockage physique associé aux pages, ce qui la rend disponible pour être allouée par n’importe quel processus. Tout bloc de pages validées peut être dévalidée.
-   Libère un bloc d’une ou de plusieurs pages réservées, en modifiant l’état des pages à libérer. La libération d’un bloc de pages rend la plage d’adresses réservées disponible qui sera allouée par le processus. Les pages réservées ne peuvent être libérées qu’en libérant l’intégralité du bloc qui a été initialement réservé par [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).
-   Annule la validation et libère un bloc d’une ou plusieurs pages validées simultanément, en modifiant l’état des pages à libérer. Le bloc spécifié doit inclure le bloc entier initialement réservé par [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), et toutes les pages doivent être validées actuellement.

Après la libération ou la dévalidation d’un bloc de mémoire, vous ne pouvez plus y faire référence. Toutes les informations qui se trouvent dans cette mémoire sont infinies. Toute tentative de lecture ou d’écriture dans une page libre entraîne une exception de violation d’accès. Si vous avez besoin d’informations, ne désvalidez pas ou ne libérez pas la mémoire qui contient ces informations.

Pour spécifier que les données d’une plage de mémoire ne présentent plus d’intérêt, appelez [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) avec la **\_ réinitialisation de mem**. Les pages ne seront pas lues ou écrites dans le fichier d’échange. Toutefois, le bloc de mémoire peut être réutilisé ultérieurement.

 

 
