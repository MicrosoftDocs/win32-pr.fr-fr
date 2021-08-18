---
title: Gestion de la mémoire sous WOW64
description: La gestion de la mémoire sous WOW64 dépend de l’architecture du processeur.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 bits Windows programmation, gestion de la mémoire
- gestion de la mémoire 64-bits Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132832"
---
# <a name="memory-management-under-wow64"></a>Gestion de la mémoire sous WOW64

La gestion de la mémoire sous WOW64 dépend de l’architecture du processeur.

## <a name="itanium-support"></a>Prise en charge d’Itanium

WOW64 simule des pages de 4 Ko en plus des pages natives de 8 Ko que le processeur Itanium utilise. Le processeur vous aide en fournissant une excellente simulation avec une faible surcharge. Le code de simulation ne peut pas gérer les cas suivants :

-   Suivi des écritures. Les fonctions [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) et [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sont implémentées dans le noyau à l’aide de la granularité de taille de page native, ce qui signifie que la simulation de page WOW64 4 Ko ne peut pas déterminer les pages de 4 Ko simulées qui sont écrites dans la page de 8 Ko sous-jacente.
-   [AWE (Address Windowing Extensions)](/windows/desktop/Memory/address-windowing-extensions). Les fonctions AWE fonctionnent sur les numéros de page et il n’existe aucun moyen de mapper les numéros de page 64 bits sur les numéros de page 32 bits.
-   Alignement des sections. Pour les images exécutables avec un alignement de section inférieur à 8 Ko (la valeur par défaut est 4 Ko pour les images x86), WOW64 doit incorrectiser toutes les pages d’image. Cela copie efficacement chaque page dans le fichier d’échange et empêche le partage des pages d’images en lecture seule entre les processus.
-   Les fonctions [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) ne sont pas prises en charge.

## <a name="x64-and-arm64-support"></a>Prise en charge x64 et ARM64

La taille de page native est de 4 Ko. Par conséquent, les éléments suivants sont pris en charge :

-   Les fonctions [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) et [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sont prises en charge.
-   Les fonctions [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) sont prises en charge.
-   L’utilisation d’adresses volumineuses présente des avantages, car x64 WOW64 prend en charge un espace d’adressage virtuel de 4 Go.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[limites de mémoire pour les versions de Windows](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Réglage de RAM 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 