---
title: Espace d’adressage virtuel (Guide de programmation pour Windows 64 bits)
description: Par défaut, les applications basées sur Microsoft Windows 64 bits disposent d’un espace d’adressage en mode utilisateur de plusieurs téraoctets.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, espace d’adressage virtuel
- espace d’adressage virtuel 64-programmation Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032162"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Espace d’adressage virtuel (Guide de programmation pour Windows 64 bits)

Par défaut, les applications basées sur Microsoft Windows 64 bits disposent d’un espace d’adressage en mode utilisateur de plusieurs téraoctets. Pour obtenir des valeurs précises, consultez [limites de mémoire pour les versions de Windows et Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases). Toutefois, les applications peuvent spécifier que le système doit allouer toute la mémoire pour l’application inférieure à 2 gigaoctets. Cette fonctionnalité est utile pour les applications 64 bits si les conditions suivantes sont remplies :

-   Un espace d’adressage de 2 Go suffit.
-   Le code contient de nombreux avertissements de troncation de pointeur.
-   Les pointeurs et les entiers sont librement mélangés.
-   Le code présente un polymorphisme utilisant des types de données 32 bits.

Tous les pointeurs sont toujours des pointeurs 64 bits, mais le système garantit que toutes les allocations de mémoire se produisent au-dessous de la limite de 2 Go, de sorte que si l’application tronque un pointeur, aucune donnée significative n’est perdue. Les pointeurs peuvent être tronqués aux valeurs 32 bits, puis étendus aux valeurs 64 bits par extension de signe ou par extension de zéro.

Pour spécifier cette limitation de mémoire, utilisez l’option **/LARGEADDRESSAWARE : no** linker. Notez que **/LARGEADDRESSAWARE : no** est ignoré pour un binaire ARM64. Toutefois, gardez à l’esprit que des problèmes peuvent survenir lors de l’utilisation de cette option. Si vous générez une DLL qui utilise cette option et que la DLL est appelée par une application qui n’utilise pas cette option, la DLL peut tronquer un pointeur 64 bits dont les 32 premiers bits sont significatifs. Cela peut entraîner une défaillance de l’application sans aucun avertissement.

 

 
