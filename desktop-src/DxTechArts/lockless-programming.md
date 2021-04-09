---
title: Considérations sur la programmation sans verrou pour Xbox 360 et Microsoft Windows
description: Cet article donne une vue d’ensemble de certains des problèmes à prendre en compte lors de la tentative d’utilisation de techniques de programmation avec blocage.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "103941464"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Considérations sur la programmation sans verrou pour Xbox 360 et Microsoft Windows

La programmation sans blocage est un moyen de partager en toute sécurité des données modifiées entre plusieurs threads sans avoir à acquérir et à libérer des verrous. Cela ressemble à une panacée, mais la programmation sans verrou est complexe et subtile, et peut parfois ne pas offrir les avantages qu’elle promet. La programmation avec blocage est particulièrement complexe sur la Xbox 360.

La programmation sans blocage est une technique valide pour la programmation multithread, mais elle ne doit pas être utilisée de façon légère. Avant de l’utiliser, vous devez comprendre les complexités, et vous devez effectuer une mesure avec soin pour vous assurer qu’elle vous donne réellement les gains attendus. Dans de nombreux cas, il existe des solutions plus simples et plus rapides, telles que le partage de données moins fréquemment, qui doivent être utilisées à la place.

L’utilisation de la programmation sans blocage correctement et en toute sécurité nécessite une connaissance significative de votre matériel et de votre compilateur. Cet article donne une vue d’ensemble de certains des problèmes à prendre en compte lors de la tentative d’utilisation de techniques de programmation avec blocage.

## <a name="programming-with-locks"></a>Programmation à l’aide de verrous

Lors de l’écriture de code multithread, il est souvent nécessaire de partager des données entre les threads. Si plusieurs threads lisent et écrivent simultanément des structures de données partagées, une altération de la mémoire peut se produire. Le moyen le plus simple de résoudre ce problème consiste à utiliser des verrous. Par exemple, si ManipulateSharedData doit être exécutée par un seul thread à la fois, une \_ section critique peut être utilisée pour garantir cela, comme dans le code suivant :

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

Ce code est relativement simple et simple, et il est facile de savoir qu’il est correct. Toutefois, la programmation avec des verrous est accompagnée de plusieurs inconvénients potentiels. Par exemple, si deux threads essaient d’acquérir les deux mêmes verrous, mais les acquièrent dans un ordre différent, vous pouvez obtenir un blocage. Si un programme maintient un verrou trop long, en raison d’une conception médiocre ou parce que le thread a été échangé par un thread de priorité plus élevée, les autres threads peuvent être bloqués pendant une longue période. Ce risque est particulièrement intéressant sur la Xbox 360 parce que les threads logiciels reçoivent un thread matériel par le développeur et que le système d’exploitation ne les déplace pas vers un autre thread matériel, même si l’un d’eux est inactif. La Xbox 360 ne dispose pas non plus d’une protection contre l’inversion de priorité, où un thread de priorité élevée tourne dans une boucle en attendant qu’un thread de faible priorité libère un verrou. Enfin, si un appel de procédure différé ou une routine de service d’interruption tente d’acquérir un verrou, vous risquez d’obtenir un blocage.

Malgré ces problèmes, les primitives de synchronisation, telles que les sections critiques, sont généralement la meilleure façon de coordonner plusieurs threads. Si les primitives de synchronisation sont trop lentes, la meilleure solution consiste généralement à les utiliser moins fréquemment. Toutefois, pour ceux qui peuvent se permettre d’avoir une complexité supplémentaire, une autre option est la programmation avec verrouillage.

## <a name="lockless-programming"></a>Programmation avec blocage

La programmation sans blocage, comme son nom l’indique, est une famille de techniques permettant de manipuler en toute sécurité des données partagées sans utiliser de verrous. Il existe des algorithmes de verrouillage disponibles pour transmettre des messages, partager des listes et des files d’attente de données, et d’autres tâches.

Lors de la programmation sans verrou, vous devez gérer deux défis : les opérations non atomiques et la réorganisation.

## <a name="non-atomic-operations"></a>Opérations non atomiques

Une opération atomique est une opération indivisible, dans laquelle d’autres threads sont assurés de ne jamais voir l’opération quand elle est à moitié terminée. Les opérations atomiques sont importantes pour la programmation sans blocage, car sans elles, les autres threads peuvent voir des valeurs semi-écrites ou un état incohérent.

Sur tous les processeurs modernes, vous pouvez supposer que les lectures et les écritures des types natifs à alignement naturellement sont atomiques. Tant que le bus de mémoire est au moins aussi grand que le type en cours de lecture ou d’écriture, l’UC lit et écrit ces types dans une transaction bus unique, ce qui empêche les autres threads de les voir dans un état semi-fini. Sur les systèmes x86 et x64, il n’est pas garanti que les lectures et écritures supérieures à huit octets sont atomiques. Cela signifie que les lectures et écritures de 16 octets des registres d’extension streaming SIMD (SSE), et les opérations de chaîne, peuvent ne pas être atomiques.

Les lectures et les écritures des types qui ne sont pas alignés naturellement, par exemple l’écriture de DWORDs qui traversent des limites de 4 octets, ne sont pas garanties atomiques. L’UC peut être amenée à effectuer ces opérations de lecture et d’écriture sous forme de transactions de bus multiples, ce qui peut permettre à un autre thread de modifier ou d’afficher les données au milieu de la lecture ou de l’écriture.

Les opérations composites, telles que la séquence de lecture-modification-écriture qui se produit lorsque vous incrémentez une variable partagée, ne sont pas atomiques. Sur la Xbox 360, ces opérations sont implémentées sous la forme de plusieurs instructions (LWZ, addi et STW), et le thread peut être transféré à partir de la séquence. Sur les systèmes x86 et x64, il existe une seule instruction (Inc) qui peut être utilisée pour incrémenter une variable en mémoire. Si vous utilisez cette instruction, l’incrémentation d’une variable est atomique sur les systèmes à un seul processeur, mais elle n’est toujours pas atomique sur les systèmes multiprocesseurs. L’atomicité de Inc sur les systèmes multiprocesseurs x86 et x64 nécessite l’utilisation du préfixe de verrouillage, qui empêche un autre processeur d’effectuer sa propre séquence de lecture-modification-écriture entre la lecture et l’écriture de l’instruction Inc.

Le code suivant montre des exemples :

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>Garantie de l’atomicité

Vous pouvez vous assurer que vous utilisez des opérations atomiques à l’aide d’une combinaison des éléments suivants :

-   Opérations Atomic atomiques
-   Verrous pour encapsuler des opérations composites
-   Fonctions du système d’exploitation qui implémentent des versions atomiques des opérations composites populaires

L’incrémentation d’une variable n’est pas une opération atomique et l’incrémentation peut entraîner une altération des données si elle est exécutée sur plusieurs threads.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 est fourni avec une famille de fonctions qui offrent des versions de lecture-modification-écriture atomiques de plusieurs opérations courantes. Il s’agit de la famille de fonctions InterlockedXxx. Si toutes les modifications de la variable partagée utilisent ces fonctions, les modifications seront thread-safe.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Réorganisation

La réorganisation est un problème plus subtil. Les lectures et écritures ne se produisent pas toujours dans l’ordre dans lequel vous les avez écrites dans votre code, ce qui peut entraîner des problèmes très confus. Dans de nombreux algorithmes multithread, un thread écrit des données, puis écrit dans un indicateur qui indique à d’autres threads que les données sont prêtes. C’est ce qu’on appelle une version d’écriture. Si les écritures sont réorganisées, d’autres threads peuvent voir que l’indicateur est défini avant de pouvoir voir les données écrites.

De même, dans de nombreux cas, un thread lit à partir d’un indicateur, puis lit des données partagées si l’indicateur indique que le thread a acquis l’accès aux données partagées. C’est ce qu’on appelle une acquisition en lecture. Si les lectures sont réorganisées, les données peuvent être lues à partir du stockage partagé avant l’indicateur, et les valeurs affichées peuvent ne pas être à jour.

La réorganisation des lectures et des écritures peut être effectuée à la fois par le compilateur et par le processeur. Les compilateurs et les processeurs ont effectué cette réorganisation depuis des années, mais sur des ordinateurs à un seul processeur, le problème était moindre. Cela est dû au fait que la réorganisation de l’UC des lectures et écritures est invisible sur les ordinateurs à un seul processeur (pour le code de pilote sans périphérique qui ne fait pas partie d’un pilote de périphérique), et la réorganisation du compilateur des lectures et des écritures est moins susceptible de provoquer des problèmes sur les ordinateurs à un seul processeur.

Si le compilateur ou l’UC réorganise les écritures affichées dans le code suivant, un autre thread peut voir que l’indicateur Alive est défini tout en continuant à voir les anciennes valeurs pour x ou y. Une réorganisation similaire peut se produire lors de la lecture.

Dans ce code, un thread ajoute une nouvelle entrée au tableau Sprite :

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

Dans ce bloc de code suivant, un autre thread lit le tableau Sprite :

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Pour garantir la sécurité de ce Sprite, nous devons empêcher le compilateur et la réorganisation des lectures et des écritures par le processeur.

### <a name="understanding-cpu-rearrangement-of-writes"></a>Présentation de la réorganisation de l’UC des écritures

Certains processeurs réorganisent les écritures afin qu’elles soient visibles en externe par d’autres processeurs ou périphériques dans l’ordre des programmes. Cette réorganisation n’est jamais visible pour le code non-thread unique, mais elle peut provoquer des problèmes dans le code multithread.

### <a name="xbox-360"></a>Xbox 360

Bien que l’UC Xbox 360 ne réorganise pas les instructions, elle réorganise les opérations d’écriture, qui se terminent après les instructions elles-mêmes. Cette réorganisation des écritures est spécifiquement autorisée par le modèle de mémoire PowerPC.

Les écritures sur la Xbox 360 n’accèdent pas directement au cache L2. Au lieu de cela, pour améliorer la bande passante d’écriture dans le cache L2, elles passent par les files d’attente du magasin, puis pour le stockage des tampons. Les mémoires tampons de regroupement de magasins permettent d’écrire des blocs de 64 octets dans le cache L2 en une seule opération. Il existe huit mémoires tampons de regroupement de magasins, qui permettent d’écrire efficacement dans plusieurs zones de mémoire différentes.

Les mémoires tampons de la boutique sont normalement écrites dans le cache L2 dans l’ordre FIFO (premier entré, premier sorti). Toutefois, si la ligne de cache cible d’une écriture ne se trouve pas dans le cache L2, cette écriture peut être retardée lorsque la ligne de cache est extraite de la mémoire.

Même lorsque les mémoires tampons de stockage sont écrites dans le cache L2 dans un ordre FIFO strict, cela ne garantit pas que les écritures individuelles sont écrites dans le cache L2 dans l’ordre. Par exemple, imaginez que l’UC écrit à l’emplacement 0x1000, puis à l’emplacement 0x2000, puis à l’emplacement 0x1004. La première écriture alloue une mémoire tampon de regroupement et la place au début de la file d’attente. La deuxième écriture alloue une autre mémoire tampon de stockage et la place ensuite dans la file d’attente. La troisième écriture ajoute ses données à la première mémoire tampon de regroupement, qui reste au début de la file d’attente. Ainsi, la troisième écriture finit par passer au cache L2 avant la deuxième écriture.

La réorganisation provoquée par les mémoires tampons de la collecte des magasins est fondamentalement imprévisible, en particulier parce que les deux threads d’un noyau partagent les tampons de stockage, ce qui rend l’allocation et le vidage des mémoires tampons de la location de magasin extrêmement variables.

C’est un exemple de la façon dont les écritures peuvent être réorganisées. Il peut y avoir d’autres possibilités.

### <a name="x86-and-x64"></a>x86 et x64

Même si les processeurs x86 et x64 réorganisent les instructions, ils ne réorganisent généralement pas les opérations d’écriture par rapport à d’autres écritures. Il existe certaines exceptions pour la mémoire allouée en écriture. En outre, les opérations de chaîne (AVI et STOS) et les écritures SSE de 16 octets peuvent être réorganisées en interne, mais dans le cas contraire, les écritures ne sont pas réorganisées les unes par rapport aux autres.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Présentation de la réorganisation de l’UC des lectures

Certains processeurs réorganisent les lectures afin qu’elles proviennent d’un stockage partagé dans un ordre non-programme. Cette réorganisation n’est jamais visible pour le code non-thread unique, mais peut provoquer des problèmes dans le code multithread.

### <a name="xbox-360"></a>Xbox 360

Les absences dans le cache peuvent entraîner des retards de lecture, ce qui fait que les lectures proviennent de la mémoire partagée dans le désordre et que le minutage de ces absences du cache est fondamentalement imprévisible. La prérécupération et la prédiction de branche peuvent également entraîner la sortie de données de la mémoire partagée dans le désordre. Voici quelques exemples de la façon dont les lectures peuvent être réorganisées. Il peut y avoir d’autres possibilités. Cette réorganisation des lectures est spécifiquement autorisée par le modèle de mémoire PowerPC.

### <a name="x86-and-x64"></a>x86 et x64

Même si les processeurs x86 et x64 réorganisent les instructions, ils ne réorganisent généralement pas les opérations de lecture par rapport à d’autres lectures. Les opérations de chaîne (AVI et STOS) et les lectures SSE de 16 octets peuvent être réorganisées en interne, mais dans le cas contraire, les lectures ne sont pas réorganisées les unes par rapport aux autres.

### <a name="other-reordering"></a>Autre réorganisation

Même si les processeurs x86 et x64 ne réorganisent pas les écritures par rapport à d’autres écritures, ou réorganisent les lectures par rapport à d’autres lectures, elles peuvent réorganiser les lectures par rapport aux écritures. Plus précisément, si un programme écrit dans un emplacement, puis lit à partir d’un autre emplacement, les données lues peuvent provenir de la mémoire partagée avant que les données écrites ne le fassent ici. Cette réorganisation peut rompre certains algorithmes, tels que les algorithmes d’exclusion mutuelle de Dekker. Dans l’algorithme de Dekker, chaque thread définit un indicateur pour indiquer qu’il souhaite entrer dans la zone critique, puis vérifie l’indicateur de l’autre thread pour déterminer si l’autre thread se trouve dans la zone critique ou s’il essaie de l’entrer. Le code initial suit.

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

Le problème est que la lecture de la touche F1 dans P0Acquire peut lire à partir du stockage partagé avant que l’écriture dans F0 la rende dans le stockage partagé. Pendant ce temps, la lecture de F0 dans P1Acquire peut lire à partir d’un stockage partagé avant que l’écriture dans la F1 le fasse dans le stockage partagé. L’effet net est que les deux threads attribuent à leurs indicateurs la valeur TRUE et que les deux threads voient l’indicateur de l’autre thread comme ayant la valeur FALSe, de sorte qu’ils entrent tous deux dans la région critique. Par conséquent, même si les problèmes de réorganisation sur des systèmes x86 et x64 sont moins courants que sur la Xbox 360, ils peuvent toujours se produire. L’algorithme de Dekker ne fonctionne pas sans barrières de mémoire matérielle sur l’une de ces plateformes.

les processeurs x86 et x64 ne réorganisent pas une écriture anticipée d’une lecture précédente. les processeurs x86 et x64 réorganisent uniquement les lectures anticipées des Écritures précédentes s’ils ciblent des emplacements différents.

Les processeurs PowerPC peuvent réorganiser les lectures en avance sur les écritures et peuvent réorganiser les écritures avant les lectures, à condition qu’elles soient sur des adresses différentes.

### <a name="reordering-summary"></a>Réorganisation du résumé

L’UC Xbox 360 réorganise les opérations de mémoire de façon plus agressive que les processeurs x86 et x64, comme indiqué dans le tableau suivant. Pour plus d’informations, consultez la documentation du processeur.



| Réorganisation de l’activité           | x86 et x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Lectures anticipées   | Non          | Oui      |
| Les écritures se déplacent avant les écritures | Non          | Oui      |
| Les écritures se déplacent avant les lectures  | Non          | Oui      |
| Lectures anticipées des écritures  | Oui         | Oui      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Barrières Read-Acquire et Write-Release

Les constructions principales utilisées pour empêcher la réorganisation des lectures et des écritures sont appelées barrières de lecture-acquisition et de libération d’écriture. Une instruction Read-Acquire est la lecture d’un indicateur ou d’une autre variable pour obtenir la propriété d’une ressource, couplée à une barrière contre la réorganisation. De même, une mise en écriture est une écriture d’un indicateur ou d’une autre variable pour accorder la propriété d’une ressource, couplée à une barrière contre la réorganisation.

Les définitions formelles, avec l’aimable Sutter des Herbs, sont les suivantes :

-   Une opération d’acquisition en lecture s’exécute avant toutes les lectures et écritures effectuées par le même thread qui le suit dans l’ordre du programme.
-   Une mise en écriture est exécutée après que toutes les opérations de lecture et d’écriture ont été effectuées par le même thread qui la précède dans l’ordre du programme.

Lorsque votre code acquiert la propriété de la mémoire, soit en obtenant un verrou, soit en extrayant un élément d’une liste liée partagée (sans verrou), il y a toujours une lecture impliquée (test d’un indicateur ou d’un pointeur pour voir si la propriété de la mémoire a été acquise). Cette lecture peut faire partie d’une opération **InterlockedXxx** , auquel cas elle implique une lecture et une écriture, mais c’est la lecture qui indique si la propriété a été acquise. Une fois que la propriété de la mémoire est acquise, les valeurs sont généralement lues ou écrites dans cette mémoire, et il est très important que ces lectures et écritures s’exécutent après avoir acquis la propriété. Un cloisonnement de lecture-acquisition garantit cela.

Lorsque la propriété d’une partie de la mémoire est libérée, soit en libérant un verrou, soit en envoyant un élément à une liste liée partagée, il y a toujours une écriture impliquée qui notifie d’autres threads que la mémoire est à présent disponible. Alors que votre code était propriétaire de la mémoire, il est probablement lu ou écrit dans celui-ci, et il est très important que ces lectures et écritures s’exécutent avant la libération de la propriété. Une barrière d’écriture garantit cela.

Il est plus simple de considérer les barrières de lecture-acquisition et de libération en écriture comme des opérations uniques. Toutefois, elles doivent parfois être construites à partir de deux parties : une lecture ou une écriture et un cloisonnement qui ne permet pas de déplacer des lectures ou des écritures. Dans ce cas, le placement du cloisonnement est essentiel. Pour un cloisonnement en lecture-acquisition, la lecture de l’indicateur est prise en premier, puis le cloisonnement, puis les lectures et écritures des données partagées. Pour une barrière en écriture, les lectures et écritures des données partagées sont d’abord effectuées, puis le cloisonnement, puis l’écriture de l’indicateur.

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

La seule différence entre une lecture-acquisition et une version d’écriture est l’emplacement de la barrière de mémoire. Une acquisition en lecture a le cloisonnement après l’opération de verrouillage, et une libération en écriture a le cloisonnement avant. Dans les deux cas, le cloisonnement est entre les références à la mémoire verrouillée et les références au verrou.

Pour comprendre pourquoi les barrières sont nécessaires lors de l’acquisition et lors de la publication des données, il est préférable (et plus précis) de considérer ces barrières comme garantissant la synchronisation avec la mémoire partagée, et non avec d’autres processeurs. Si un processeur utilise une mise en écriture pour libérer de la mémoire partagée d’une structure de données, et qu’un autre processeur utilise une acquisition en lecture pour accéder à cette structure de données à partir de la mémoire partagée, le code fonctionnera correctement. Si l’un des processeurs n’utilise pas la barrière appropriée, le partage de données peut échouer.

L’utilisation de la barrière appropriée pour empêcher le compilateur et la réorganisation de l’UC pour votre plateforme est essentielle.

L’un des avantages de l’utilisation des primitives de synchronisation fournies par le système d’exploitation est que tous ces éléments incluent les barrières de mémoire appropriées.

## <a name="preventing-compiler-reordering"></a>Empêcher la réorganisation du compilateur

Le travail d’un compilateur consiste à optimiser de manière agressive votre code afin d’améliorer les performances. Cela comprend la réorganisation des instructions là où elles sont utiles et où qu’elles ne changent pas le comportement. Étant donné que la norme C++ ne mentionne jamais le multithread et que le compilateur ne sait pas quel code doit être thread-safe, le compilateur suppose que votre code est monothread lors de la détermination des redispositions qu’il peut en toute sécurité. Par conséquent, vous devez indiquer au compilateur qu’il n’est pas possible de réorganiser les lectures et les écritures.

Avec Visual C++ vous pouvez empêcher la réorganisation du compilateur à l’aide de l' [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)intrinsèque du compilateur. Lorsque vous insérez **\_ ReadWriteBarrier** dans votre code, le compilateur ne déplace pas les lectures et les écritures dans celui-ci.

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

Dans le code suivant, un autre thread lit le tableau Sprite :

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Il est important de comprendre que [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) n’insère pas d’instructions supplémentaires et qu’il n’empêche pas le processeur de réorganiser les lectures et les écritures ; il empêche uniquement le compilateur de les réorganiser. Par conséquent, **\_ ReadWriteBarrier** est suffisant quand vous implémentez une barrière d’écriture sur x86 et x64 (comme x86 et x64 ne réorganisent pas les écritures, et une écriture normale suffit pour libérer un verrou), mais dans la plupart des autres cas, il est également nécessaire d’empêcher le processeur de réorganiser les lectures et les écritures.

Vous pouvez également utiliser [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) quand vous écrivez dans une mémoire allouée en écriture non mise en cache pour empêcher la réorganisation des écritures. Dans ce cas, **\_ ReadWriteBarrier** permet d’améliorer les performances, en garantissant que les écritures ont lieu dans l’ordre linéaire préféré du processeur.

Il est également possible d’utiliser les intrinsèques [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) et [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) pour un contrôle plus précis de la réorganisation du compilateur. Le compilateur ne déplace pas les lectures sur un **\_ ReadBarrier** et ne déplace pas les écritures dans un **\_ WriteBarrier**.

## <a name="preventing-cpu-reordering"></a>Prévention de la réorganisation de l’UC

La réorganisation de l’UC est plus subtile que le compilateur réorganisation. Vous ne voyez pas que cela se produit directement, vous voyez simplement des bogues inexplicable. Pour empêcher la réorganisation de l’UC des lectures et des écritures, vous devez utiliser des instructions de barrière de mémoire sur certains processeurs. Le nom à usage général d’une instruction de barrière de mémoire, sur Xbox 360 et sur Windows, est [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Cette macro est implémentée de manière appropriée pour chaque plateforme.

Sur Xbox 360, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) est défini en tant que **lwsync** (Lightweight Sync), également disponible via le **\_ \_ lwsync** intrinsèque, qui est défini dans ppcintrinsics. h. **\_ \_ lwsync** sert également de barrière de mémoire du compilateur, ce qui empêche la réorganisation des lectures et des écritures par le compilateur.

L’instruction **lwsync** est une barrière de mémoire sur Xbox 360 qui synchronise un cœur de processeur avec le cache L2. Il garantit que toutes les écritures avant **lwsync** le font dans le cache L2 avant les écritures qui suivent. Cela garantit également que toutes les lectures qui suivent **lwsync** n’obtiennent pas les données plus anciennes de L2 que les lectures précédentes. Le type de réorganisation qu’il n’empêche pas est une lecture anticipée d’une écriture vers une autre adresse. Par conséquent, **lwsync** applique l’ordonnancement de mémoire qui correspond à l’ordonnancement de mémoire par défaut sur les processeurs x86 et x64. Pour obtenir un classement complet de la mémoire, l’instruction de synchronisation est plus coûteuse (également appelée synchronisation à haute densité), mais dans la plupart des cas, cela n’est pas obligatoire. Les options de réorganisation de la mémoire sur Xbox 360 sont indiquées dans le tableau suivant.



| Réorganisation de la Xbox 360           | Aucune synchronisation | lwsync | synchronisation |
|-------------------------------|---------|--------|------|
| Lectures anticipées   | Oui     | Non     | Non   |
| Les écritures se déplacent avant les écritures | Oui     | Non     | Non   |
| Les écritures se déplacent avant les lectures  | Oui     | Non     | Non   |
| Lectures anticipées des écritures  | Oui     | Oui    | Non   |



 

PowerPC possède également les instructions de synchronisation **iSync** et **EIEIO** (qui sont utilisées pour contrôler la réorganisation de la mémoire empêchant la mise en cache). Ces instructions de synchronisation ne doivent pas être nécessaires à des fins de synchronisation normales.

Sur Windows, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) est défini dans Winnt. h et vous donne une instruction de barrière de mémoire différente selon que vous compilez pour x86 ou x64. L’instruction de barrière de mémoire sert de barrière complète, empêchant toute réorganisation des lectures et des écritures sur le cloisonnement. Par conséquent, **MemoryBarrier** sur Windows offre une garantie de réorganisation plus forte que sur la Xbox 360.

Sur la Xbox 360 et sur de nombreux autres processeurs, il est possible d’empêcher l’utilisation de la réorganisation de la lecture par le processeur. Si vous lisez un pointeur, puis utilisez ce pointeur pour charger d’autres données, l’UC garantit que les lectures du pointeur ne sont pas plus anciennes que la lecture du pointeur. Si votre indicateur de verrouillage est un pointeur et que toutes les lectures de données partagées sont en dehors du pointeur, le [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) peut être omis, pour une légère économie de performances.

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

L’instruction [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) empêche uniquement la réorganisation des lectures et des écritures dans la mémoire cache. Si vous allouez de la mémoire en tant que PAGE \_ NoCache ou page \_ WRITECOMBINE, une technique courante pour les créateurs de pilote de périphérique et pour les développeurs de jeux sur Xbox 360, **MemoryBarrier** n’a aucun effet sur les accès à cette mémoire. La plupart des développeurs n’ont pas besoin de synchroniser la mémoire qui ne peut pas être mise en cache. La procédure n'entre pas dans le cadre de cet article.

## <a name="interlocked-functions-and-cpu-reordering"></a>Fonctions verrouillées et réorganisation de l’UC

Parfois, la lecture ou l’écriture qui acquiert ou libère une ressource s’effectue à l’aide de l’une des fonctions **InterlockedXxx** . Sur Windows, cela simplifie les choses. étant donné que sur Windows, les fonctions **InterlockedXxx** sont toutes des barrières de mémoire saturée. Ils disposent en fait d’une barrière de mémoire processeur à la fois avant et après, ce qui signifie qu’il s’agit d’une barrière d’accès en lecture ou d’écriture complète.

Sur Xbox 360, les fonctions **InterlockedXxx** ne contiennent pas de barrières de mémoire processeur. Elles empêchent la réorganisation des lectures et des écritures par le compilateur, mais pas la réorganisation de l’UC. Par conséquent, dans la plupart des cas, lors de l’utilisation de fonctions **InterlockedXxx** sur Xbox 360, vous devez les précéder ou les suivre avec un **\_ \_ lwsync**, afin de leur donner une barrière d’acquisition en écriture ou de libération. Pour plus de commodité et pour faciliter la lisibilité, il existe des versions d' **acquisition** et de **publication** de nombreuses fonctions **InterlockedXxx** . Ils sont fournis avec une barrière de mémoire intégrée. Par exemple, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) effectue un incrément de verrouillage suivi d’une barrière de mémoire **\_ \_ lwsync** pour fournir la fonctionnalité de lecture-acquisition complète.

Il est recommandé d’utiliser les versions **Acquire** et **Release** des fonctions **InterlockedXxx** (dont la plupart sont également disponibles sur Windows, sans aucune pénalité de performances) pour rendre votre intention plus évidente et pour faciliter l’obtention des instructions de barrière de mémoire à l’endroit approprié. Toute utilisation de **InterlockedXxx** sur Xbox 360 sans barrière de mémoire doit être examinée très attentivement, car il s’agit souvent d’un bogue.

Cet exemple montre comment un thread peut passer des tâches ou d’autres données à un autre thread à l’aide des versions **Acquire** et **Release** des fonctions **InterlockedXxxSList** . Les fonctions **InterlockedXxxSList** sont une famille de fonctions permettant de conserver une liste liée de façon unique et partagée sans verrou. Notez que les variantes d' **acquisition** et de **libération** de ces fonctions ne sont pas disponibles sur Windows, mais les versions régulières de ces fonctions constituent une barrière de mémoire complète sur Windows.

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Variables volatiles et réorganisation

La norme C++ indique que les lectures de variables volatiles ne peuvent pas être mises en cache, que les écritures volatiles ne peuvent pas être retardées, et que les lectures et écritures volatiles ne peuvent pas être déplacées au-delà. Cela suffit pour la communication avec les périphériques matériels, qui est l’objectif du mot clé volatile dans la norme C++.

Toutefois, les garanties de la norme ne sont pas suffisantes pour l’utilisation de volatile pour le Multi-Threading. La norme C++ n’empêche pas le compilateur de réorganiser les lectures et écritures non volatiles relatives aux lectures et écritures volatiles, et n’indique rien sur la prévention de la réorganisation de l’UC.

Visual C++ 2005 va au-delà du C++ standard pour définir la sémantique de Multi-Threading pour l’accès aux variables volatiles. À compter de Visual C++ 2005, les lectures à partir des variables volatiles sont définies pour avoir une sémantique d’acquisition en lecture, et les écritures dans des variables volatiles sont définies pour avoir une sémantique en écriture. Cela signifie que le compilateur ne réorganise pas les lectures et les écritures qui se sont passées, et sous Windows, il s’assure que le processeur ne le fait pas non plus.

Il est important de comprendre que ces nouvelles garanties s’appliquent uniquement à Visual C++ 2005 et aux futures versions de Visual C++. Les compilateurs d’autres fournisseurs implémentent généralement une sémantique différente, sans les garanties supplémentaires de Visual C++ 2005. En outre, sur Xbox 360, le compilateur n’insère aucune instruction pour empêcher le processeur de réorganiser les lectures et les écritures.

## <a name="example-of-a-lock-free-data-pipe"></a>Exemple de canal de données Lock-Free

Un canal est une construction qui permet à un ou plusieurs threads d’écrire des données qui sont ensuite lues par d’autres threads. Une version verrouillée d’un canal peut être un moyen élégant et efficace de passer le travail d’un thread à un thread. Le kit de développement logiciel (SDK) DirectX fournit des **LockFreePipe**, un seul lecteur et un canal de verrouillage à un seul enregistreur, qui est disponible dans DXUTLockFreePipe. h. Le même **LockFreePipe** est disponible dans le kit de développement logiciel (SDK) Xbox 360 dans AtgLockFreePipe. h.

**LockFreePipe** peut être utilisé lorsque deux threads ont une relation producteur/consommateur. Le thread producteur peut écrire des données dans le canal pour que le thread de consommateur soit traité à une date ultérieure, sans jamais se bloquer. Si le canal est rempli, les écritures échouent et le thread producteur devra réessayer plus tard, mais cela ne se produit que si le thread producteur est en avance. Si le canal est vidé, les lectures échouent et le thread de consommateur devra réessayer plus tard, mais cela ne se produit que si le thread de consommateur n’a pas de travail à effectuer. Si les deux threads sont bien équilibrés et que le canal est suffisamment grand, le canal les permet de passer facilement des données sans aucun retard ni bloc.

## <a name="xbox-360-performance"></a>Performances de la Xbox 360

Les performances des instructions de synchronisation et des fonctions sur Xbox 360 varient en fonction de l’autre code en cours d’exécution. L’acquisition de verrous prendra plus de temps si un autre thread possède actuellement le verrou. Les opérations de section [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) et critique prendront plus de temps si d’autres threads écrivent sur la même ligne de cache. Le contenu des files d’attente du magasin peut également avoir une incidence sur les performances. Par conséquent, tous ces nombres sont simplement des approximations, générés à partir de tests très simples :

-   **lwsync** a été mesuré comme utilisant des cycles de 33-48.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) a été mesuré comme utilisant des cycles de 225-260.
-   L’acquisition ou la libération d’une section critique a été mesurée en prenant environ 345 cycles.
-   L’acquisition ou la libération d’un mutex a été mesurée comme s’effectuant environ 2350 cycles.

## <a name="windows-performance"></a>Performances Windows

Les performances des instructions de synchronisation et des fonctions sur Windows varient considérablement en fonction du type et de la configuration du processeur, et de la nature du code en cours d’exécution. Les systèmes multicœurs et multisockets prennent souvent plus de temps pour exécuter des instructions de synchronisation et l’acquisition de verrous prend plus de temps si un autre thread possède actuellement le verrou.

Toutefois, même certaines mesures générées à partir de tests très simples sont utiles :

-   [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) a été mesuré comme utilisant des cycles de 20-90.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) a été mesuré comme utilisant des cycles de 36-90.
-   L’acquisition ou la libération d’une section critique a été mesurée en prenant 40-100 cycles.
-   L’acquisition ou la libération d’un mutex a été mesurée comme s’effectuant environ 750-2500 cycles.

Ces tests ont été effectués sur Windows XP sur une gamme de processeurs différents. Les courtes périodes étaient sur un ordinateur monoprocesseur, et plus longtemps sur un ordinateur multiprocesseur.

Bien que l’acquisition et la libération de verrous soient plus coûteuses que l’utilisation de la programmation sans verrou, il est même préférable de partager les données moins fréquemment, ce qui évite le coût.

## <a name="performance-thoughts"></a>Réflexions sur les performances

L’acquisition ou la libération d’une section critique se compose d’une barrière de mémoire, d’une opération **InterlockedXxx** et d’une vérification supplémentaire pour gérer la récursivité et pour revenir à un mutex, si nécessaire. Vous devez faire attention à l’implémentation de votre propre section critique, car le fait de tourner dans une boucle en attendant la libération d’un verrou, sans revenir à un mutex, peut gaspiller des performances considérables. Pour les sections critiques qui sont fortement sollicitées, mais qui ne sont pas détenues pendant longtemps, vous devez envisager d’utiliser [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) afin que le système d’exploitation tourne pendant un certain temps, en attendant que la section critique soit disponible au lieu d’être immédiatement différée à un mutex si la section critique est propriétaire lorsque vous essayez de l’acquérir. Afin d’identifier les sections critiques qui peuvent tirer parti d’un comptage de spins, il est nécessaire de mesurer la longueur de l’attente classique pour un verrou particulier.

Si un segment de mémoire partagé est utilisé pour les allocations de mémoire (comportement par défaut), chaque allocation de mémoire et la version libre impliquent l’acquisition d’un verrou. À mesure que le nombre de threads et le nombre d’allocations augmente, les niveaux de performances sont désactivés et la diminution finit. L’utilisation de tas par thread, ou la réduction du nombre d’allocations, peut éviter ce goulot d’étranglement de verrouillage.

Si un thread génère des données et qu’un autre thread consomme des données, il se peut qu’elles finissent par partager des données fréquemment. Cela peut se produire si un thread charge des ressources et qu’un autre thread effectue le rendu de la scène. Si le thread de rendu fait référence aux données partagées à chaque appel de dessin, la surcharge de verrouillage est élevée. De meilleures performances peuvent être obtenues si chaque thread a des structures de données privées qui sont ensuite synchronisées une fois par Frame ou moins.

Il n’est pas garanti que les algorithmes sans verrou soient plus rapides que les algorithmes qui utilisent des verrous. Vous devez vérifier si les verrous vous posent réellement des problèmes avant d’essayer de les éviter, et que vous devez effectuer une mesure pour voir si votre code sans verrouillage améliore réellement les performances.

## <a name="platform-differences-summary"></a>Résumé des différences de plateforme

-   Les fonctions **InterlockedXxx** empêchent la réorganisation du processeur en lecture/écriture sur Windows, mais pas sur la Xbox 360.
-   La lecture et l’écriture de variables volatiles à l’aide de Visual Studio C++ 2005 empêche la réorganisation de la lecture/écriture de l’UC sur Windows, mais sur Xbox 360, elle empêche uniquement la réorganisation en lecture/écriture du compilateur.
-   Les écritures sont réorganisées sur Xbox 360, mais pas sur x86 ou x64.
-   Les lectures sont réorganisées sur Xbox 360, mais sur x86 ou x64, elles sont réorganisées uniquement par rapport aux écritures, et uniquement si les lectures et les écritures ciblent des emplacements différents.

## <a name="recommendations"></a>Recommandations

-   Utilisez des verrous lorsque cela est possible, car ils sont plus faciles à utiliser correctement.
-   Évitez les verrouillages trop fréquents, afin que les coûts de verrouillage ne deviennent pas significatifs.
-   Évitez de maintenir des verrous trop longs, afin d’éviter les blocages longs.
-   Utilisez la programmation sans blocage, le cas échéant, mais assurez-vous que les gains justifient la complexité.
-   Utilisez la programmation en mode de verrouillage ou les verrous de spin dans les situations où d’autres verrous sont interdits, par exemple lors du partage de données entre des appels de procédure différés et du code normal.
-   Utilisez uniquement des algorithmes de programmation de verrouillage standard qui ont été prouvés comme corrects.
-   Lors de la programmation sans verrouillage, veillez à utiliser des variables d’indicateur volatiles et des instructions de barrière de mémoire en fonction des besoins.
-   Lorsque vous utilisez **InterlockedXxx** sur Xbox 360, utilisez les variantes **Acquire** et **Release** .

## <a name="references"></a>Références

-   Bibliothèque MSDN. «[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx). » Référence du langage C++.
-   Vance Morrison. «[Comprendre l’impact des techniques de Low-Lock dans les applications multithread](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)». MSDN Magazine, octobre 2005.
-   Lyons, Michael. «[Modèle de stockage PowerPC et programmation Aix](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)». IBM developerWorks, 16 novembre 2005.
-   McKenney, Paul E». «[classement de mémoire dans les microprocesseurs modernes, partie II](https://www.linuxjournal.com/article/8212)». Journal Linux, 2005 septembre. \[Cet article contient des informations détaillées sur x86.\]
-   Intel Corporation. «[Commande de mémoire d’architecture Intel® 64](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf). » 2007 août. \[S’applique aux processeurs IA-32 et Intel 64.\]
-   Niebler, Eric. «[Rapport de voyage : réunion ad hoc sur les threads en C++](https://www.artima.com/cppsource/threads_meeting.html)». Source C++, 17 octobre 2006.
-   Hart, Thomas E. 2006. «[Création d’une synchronisation en toute simplicité rapide : implications sur les performances de la récupération de la mémoire](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)». Procédure du Congrès international de traitement parallèle et distribué 2006 (IPDPS 2006), île Rhodes, Grèce, avril 2006.

 

 