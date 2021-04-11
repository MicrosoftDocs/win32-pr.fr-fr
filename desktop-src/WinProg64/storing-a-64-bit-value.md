---
title: Stockage d’une valeur 64 bits
description: Pour stocker une valeur de pointeur 64 bits, utilisez ULONG \_ ptr. Une \_ valeur PTR ulong est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- stockage des valeurs 64 bits de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310057"
---
# <a name="storing-a-64-bit-value"></a>Stockage d’une valeur 64 bits

Pour stocker une valeur de pointeur 64 bits, utilisez **ULong \_ ptr**. Une **valeur \_ ptr ULONG** est 32 bits quand elle est compilée avec un compilateur 32 bits et 64 bits lorsqu’elle est compilée avec un compilateur 64 bits.

Les exemples suivants utilisent du code réel qui a été porté sur Windows 64 bits. Des commentaires sur les étapes permettant de rendre le code compatible 64 bits sont inclus.

## <a name="example-1-getting-an-address"></a>Exemple 1 : obtention d’une adresse

Le code suivant illustre un moyen portable d’obtenir une adresse.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Utilisation de ULONG (méthode 32 bits uniquement)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>Utilisation de ULONG_PTR (méthode portable)</td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>Exemple 2 : calcul d’une adresse

Le code suivant illustre un moyen portable de calculer une adresse.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Utilisation de ULONG (méthode 32 bits uniquement)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>Utilisation de ULONG_PTR (méthode portable)</td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




