---
title: Considérations supplémentaires
description: Lorsque vous transférez votre code, tenez compte des points suivants.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- conseils sur le portage 64-bit Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 199f522bebf0d6d5552aa81d99aab12f77685dea35eb329b9e7d11d46b4f1500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561534"
---
# <a name="additional-considerations"></a>Considérations supplémentaires

Lorsque vous transférez votre code, tenez compte des points suivants :

- L’hypothèse suivante n’est plus valide :

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Toutefois, le compilateur 64 bits définit \_ Win32 pour la compatibilité descendante.

- L’hypothèse suivante n’est plus valide :

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   Dans ce cas, la clause else peut représenter \_ Win32 ou \_ Win64.

- Soyez vigilant avec l’alignement des types de données. La **macro \_ alignement de type** retourne les exigences d’alignement d’un type de données. Par exemple : `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 sur x86, 8 sur processeur Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 partout

    Par exemple, le code du noyau qui se présente comme suit :

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    doit probablement être remplacé par :

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Les correctifs automatiques des exceptions d’alignement en mode noyau sont désactivés pour les systèmes Intel Itanium.

- Soyez vigilant avec les opérations NOT. Tenez compte des éléments suivants :

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    Le problème est que ~ (b – 1) produit « 0x0000 0000 xxxx xxxx » et non pas « 0xFFFF FFFF xxxx xxxx ». Le compilateur ne détecte pas cela. Pour résoudre ce problème, modifiez le code comme suit :

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Effectuez des opérations non signées et signées avec prudence. Tenez compte des éléments suivants :

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    Le résultat est de taille inattendue. La règle est que si l’un des opérandes n’est pas signé, le résultat est non signé. Dans l’exemple précédent, une est convertie en valeur non signée, divisée par b et le résultat est stocké en c. La conversion n’implique aucune manipulation numérique.

    Voici un autre exemple :

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    Le problème survient car x n’est pas signé, ce qui rend l’expression entière non signée. Cela fonctionne bien sauf si y est négatif. Dans ce cas, y est converti en une valeur non signée, l’expression est évaluée à l’aide de la précision 32 bits, mise à l’échelle et ajoutée à pVar1. Un nombre négatif non signé 32 bits devient un grand nombre positif de 64 bits, ce qui donne un résultat erroné. Pour résoudre ce problème, déclarez x comme valeur signée ou convertissez-le explicitement en **long** dans l’expression.

- Soyez prudent lorsque vous effectuez des allocations de taille fragmentaire. Par exemple :

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    Le code suivant est incorrect, car le compilateur remplit la structure avec un 4 octets supplémentaires pour effectuer l’alignement sur 8 octets :

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    Le code suivant est correct :

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Ne pas passer `(HANDLE)0xFFFFFFFF` à des fonctions telles que [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga). Utilisez plutôt une **\_ \_ valeur de handle non valide**.
- Utilisez les spécificateurs de format appropriés lors de l’impression d’une chaîne. Utilisez% p pour imprimer des pointeurs au format hexadécimal. C’est le meilleur choix pour les pointeurs d’impression. Microsoft Visual C++ prend en charge% I pour imprimer des données polymorphes. Visual C++ prend également en charge% I64 pour imprimer des valeurs de 64 bits.

 

 