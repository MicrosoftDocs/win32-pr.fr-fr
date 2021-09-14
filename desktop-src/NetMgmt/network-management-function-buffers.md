---
title: Mémoires tampons de fonctions de gestion de réseau
description: La bibliothèque Runtime RPC gère les tampons requis par les fonctions de gestion de réseau de l’extraction de données 32 bits comme suit.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194711"
---
# <a name="network-management-function-buffers"></a>Mémoires tampons de fonctions de gestion de réseau

La bibliothèque Runtime RPC gère les tampons requis par les fonctions de gestion de réseau de l’extraction de données 32 bits comme suit :

-   **Envoi de données au serveur** (données spécifiées par les \[ \] paramètres in).

    L’appelant doit allouer et libérer la mémoire tampon pour la structure d’informations (ou structures) appropriée et passer une variable pointeur à la fonction. L’appelant n’a pas besoin de spécifier la longueur de la mémoire tampon.

    Exemple : [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Récupération de données à partir du serveur** (données spécifiées par les \[ \] paramètres out).

    Le système alloue la mémoire tampon pour les informations retournées. L’appelant doit passer une variable pointeur à la fonction en entrée. En cas de retour réussi, le pointeur reçoit l’adresse de la mémoire tampon allouée par le système qui contient les informations retournées. Cela simplifie le code appelant, car l’appelant n’a pas besoin d’estimer la taille de la mémoire tampon, ou de redimensionner la mémoire tampon et de réexécuter la fonction.

    Lorsque l’appelant a terminé de traiter les informations renvoyées, il doit libérer la mémoire allouée par le système en appelant la fonction [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) . Pour plus d’informations sur la spécification des tailles de mémoire tampon, consultez [Lengths de la mémoire tampon des fonctions de gestion réseau](network-management-function-buffer-lengths.md).

    Exemple : [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




