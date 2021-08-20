---
title: Les outils
description: Cette rubrique décrit les outils que vous pouvez utiliser pour rendre votre application 64 bits prête. Windows 10 est disponible pour les processeurs x64 et ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- guide de programmation Windows 64 bits 64-bits Windows programmation, outils
- outils de programmation Windows bits 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28084c445d664e130a9bb6dc5c087f8421cdaa5746845308258662739ee9084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569889"
---
# <a name="the-tools"></a>Les outils

Cette rubrique décrit les outils que vous pouvez utiliser pour rendre votre application 64 bits prête. Windows 10 est disponible pour les processeurs x64 et ARM64.

## <a name="include-files"></a>Fichiers include

Les éléments d’API sont pratiquement identiques entre les Windows 32 et 64 bits. les fichiers d’en-tête Windows ont été modifiés afin de pouvoir être utilisés pour le code 32 et 64 bits. les nouveaux types et macros 64 bits sont définis dans un nouveau fichier d’en-tête, Basetsd. h, qui se trouve dans le jeu de fichiers d’en-tête inclus par Windows. h. Basetsd. h comprend les nouvelles définitions de type de données pour faciliter la création d’une taille de mot de code source indépendante.

## <a name="new-data-types"></a>Nouveaux types de données

les fichiers d’en-tête Windows contiennent de nouveaux types de données. Ces types sont principalement destinés à la compatibilité de type avec les types de données 32 bits. Les nouveaux types fournissent exactement le même type que les types existants, tout en assurant la prise en charge de l’Windows 64 bits. Pour plus d’informations, consultez [les nouveaux types de données](the-new-data-types.md) ou le fichier d’en-tête Basetsd. h.

## <a name="predefined-macros"></a>Macros prédéfinies

Le compilateur définit les macros suivantes pour identifier la plateforme.



| Macro   | Signification                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| \_WIN64 | Une plateforme 64 bits. Cela comprend à la fois x64 et ARM64.                                                        |
| \_32 | Une plateforme 32 bits. Cette valeur est également définie par le compilateur 64 bits pour la compatibilité descendante.<br/> |
| \_WIN16 | Plateforme 16 bits                                                                                           |



 

Les macros suivantes sont spécifiques à l’architecture.



| Macro      | Signification                |
|------------|------------------------|
| \_M \_ ia64  | Plateforme Intel Itanium |
| \_M \_ ix86  | plateforme x86           |
| \_M \_ x64   | plateforme x64           |
| \_M \_ ARM64 | Plateforme ARM64         |



 

N’utilisez pas ces macros, à l’exception du code propre à l’architecture, à la place, utilisez \_ Win64, Win32 et Win16 dans la mesure du \_ \_ possible.

## <a name="helper-functions"></a>Fonctions d’assistance

Les fonctions inline suivantes (définies dans Basetsd. h) peuvent vous aider à convertir en toute sécurité des valeurs d’un type vers un autre.

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> **IntToPtr** signe-étend la valeur **int** , **UIntToPtr** zéro étend la valeur **unsigned int** , **LongToPtr** signe étend la valeur **long** et **ULongToPtr** zéro-étend la valeur **long non signée** .

 

## <a name="64-bit-compiler"></a>Compilateur 64 bits

Les compilateurs 64 bits peuvent être utilisés pour identifier la troncation de pointeur, les casts de type incorrects et d’autres problèmes spécifiques à 64 bits.

Lorsque le compilateur est exécuté pour la première fois, il génère probablement de nombreux avertissements de troncation de pointeur ou d’incompatibilité de type, comme suit :

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

Utilisez ces avertissements comme guide pour rendre le code plus robuste. Il est conseillé d’éliminer tous les avertissements, en particulier les avertissements de troncation de pointeur.

## <a name="64-bit-compiler-switches-and-warnings"></a>Avertissements et commutateurs du compilateur 64 bits

Notez que ce compilateur active le modèle de données LLP64.

Il existe une option d’avertissement pour faciliter le portage vers LLP64. Le commutateur-Wp64-W3 active les avertissements suivants :

-   C4305 : avertissement de troncation. Par exemple, « Return » : troncation de « unsigned int64 » à « long ».
-   C4311 : avertissement de troncation. Par exemple, « cast de type » : troncation de pointeur de « int \* \_ ptr64 » à « int ».
-   C4312 : conversion en avertissement de taille supérieure. Par exemple, « cast de type » : conversion de « int » en « int \* \_ ptr64 » d’une plus grande taille.
-   C4318 : passage de longueur nulle. Par exemple, le passage de la constante zéro comme longueur à la fonction **memset** .
-   C4319 : opérateur NOT. Par exemple, « ~ » : zéro étendant « unsigned long » à « unsigned \_ Int64 » d’une taille supérieure.
-   C4313 : appel de la famille de fonctions **printf** avec des spécificateurs et des arguments de type de conversion conflictuels. Par exemple, « printf » : « % p » dans la chaîne de mise en forme est en conflit avec l’argument 2 de type « \_ Int64 ». Un autre exemple est l’appel de printf ("% x", valeur de pointeur \_ ); cela provoque une troncation des 32 bits supérieurs. L’appel correct est printf ("% p", valeur du pointeur \_ ).
-   C4244 : identique à l’C4242 d’avertissement existant. Par exemple, « Return » : conversion de « \_ Int64 » en « unsigned int », perte possible de données.

## <a name="64-bit-linker-and-libraries"></a>Bibliothèques et éditeur de liens 64 bits

pour générer des applications, utilisez l’éditeur de liens et les bibliothèques fournis par le SDK Windows. La plupart des bibliothèques 32 bits ont une version 64 bits correspondante, mais certaines bibliothèques héritées sont disponibles uniquement dans les versions 32 bits. Le code qui appelle ces bibliothèques n’est pas lié lorsque l’application est générée pour une Windows de 64 bits.

 

 





