---
title: Stockage d’une valeur 64 bits
description: Pour stocker une valeur de pointeur 64 bits, utilisez ULONG \_ ptr. Une \_ valeur PTR ulong est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- stockage des valeurs 64 bits 64-bit Windows programmation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469066"
---
# <a name="storing-a-64-bit-value"></a>Stockage d’une valeur 64 bits

Pour stocker une valeur de pointeur 64 bits, utilisez **ULong \_ ptr**. Une **valeur \_ ptr ULONG** est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.

Les exemples suivants utilisent du code réel qui a été porté à la Windows 64 bits. Des commentaires sur les étapes permettant de rendre le code compatible 64 bits sont inclus.

## <a name="example-1-getting-an-address"></a>Exemple 1 : obtention d’une adresse

Le code suivant illustre un moyen portable d’obtenir une adresse.




| | | Utilisation de ULONG (méthode 32 bits uniquement) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Utilisation de ULONG_PTR (méthode portable) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Exemple 2 : calcul d’une adresse

Le code suivant illustre un moyen portable de calculer une adresse.




| | | Utilisation de ULONG (méthode 32 bits uniquement) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Utilisation de ULONG_PTR (méthode portable) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




