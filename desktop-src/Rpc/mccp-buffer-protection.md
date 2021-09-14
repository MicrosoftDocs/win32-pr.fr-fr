---
title: Protection de la mémoire tampon MCCP
description: à partir de Windows Vista, le moteur de marshaling RPC prend d’autres mesures pour empêcher les dépassements de mémoire tampon côté client en raison des données renvoyées. Cette fonctionnalité est appelée « protection de la conformité de la mini-calcul » (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d04de57974bd9665d659129590d72513eb83e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194072"
---
# <a name="mccp-buffer-protection"></a>Protection de la mémoire tampon MCCP

à partir de Windows Vista, le moteur de marshaling RPC prend d’autres mesures pour empêcher les dépassements de mémoire tampon côté client en raison des données renvoyées. Cette fonctionnalité est appelée « protection de la conformité de la mini-calcul » (MCCP).

Lorsque le client passe un pointeur vers une mémoire tampon existante à un \[ paramètre [**out**](/windows/desktop/Midl/out-idl) \] ou \[ [**in**](/windows/desktop/Midl/in),**out** , les \] données retournées pour ce paramètre sont copiées dans la mémoire tampon existante. Si les données retournées sont plus volumineuses que la mémoire tampon passée, un dépassement de mémoire tampon peut se produire lorsque RPC copie les données renvoyées dans la mémoire tampon trop petite. Consultez [les pointeurs de niveau supérieur et incorporé](top-level-and-embedded-pointers.md).

Avec MCCP, RPC tente de détecter cette condition et de rejeter l’appel si elle est détectée. Pour les mémoires tampons avec une valeur de corrélation, telle que \[ la [**taille \_**](/windows/desktop/Midl/size-is) \] , si les données retournées ne tiennent pas dans la taille de mémoire tampon spécifiée, l’appel est rejeté et l' \_ exception RPC X \_ Data stub incorrecte \_ \_ est levée. Pour les chaînes non dimensionnées, l’appel est rejeté si la taille de chaîne existante (longueur jusqu’à la marque de fin **null** ) est insuffisante pour contenir la chaîne retournée, l’appel est rejeté. RPC ne peut pas détecter les dépassements de mémoire tampon dans toutes les conditions. il est donc recommandé au développeur de continuer à prendre des précautions normales contre les dépassements de mémoire tampon.

Si le client ne passe pas de mémoire tampon existante pour un paramètre de \[ [**sortie**](/windows/desktop/Midl/out-idl) \] , mais passe un pointeur déréférencé à la **valeur null**, RPC suit les règles normales pour allouer une nouvelle mémoire tampon au nom du client. Cette mémoire tampon sera allouée avec un espace suffisant pour contenir les données retournées.

Une deuxième protection est que pour les paramètres corrélés, RPC s’impose qu’une mémoire tampon non **null** est transmise lorsque la variable de nombre de corrélations est non **null**.

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Si *myString* a la **valeur null**, RPC rejette l’appel, sauf si *Length* a la valeur 0. Notez que RPC autorise la *longueur* à être égale à 0 alors que *myString* est non **null** et que RPC traite *myString* comme une allocation de mémoire tampon de longueur 0.

 

 