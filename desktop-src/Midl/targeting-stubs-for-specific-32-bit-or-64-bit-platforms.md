---
title: Ciblage des stubs pour des plateformes 32 bits ou 64 bits spécifiques
description: Certaines des fonctionnalités de Microsoft RPC et des compilateurs MIDL 3,0 et versions ultérieures sont spécifiques à la plateforme.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL de plateformes 32 bits
- MIDL de plateformes 64 bits
- stubs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310730"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Ciblage des stubs pour des plateformes 32 bits ou 64 bits spécifiques

Certaines des fonctionnalités de Microsoft RPC et des compilateurs MIDL 3,0 et versions ultérieures sont spécifiques à la plateforme.

Par précaution, les compilateurs MIDL 3,0 et versions ultérieures génèrent des gardes qui facilitent la vérification de la compatibilité pendant la phase de compilation C. MIDL génère deux types de protecteurs : une protection dépendante de la plateforme (32 bits par rapport à 64 bits) et une protection dépendante de la version (dépendance de l’ensemble de fonctionnalités). Par exemple, MIDL génère la protection suivante pour empêcher la compilation en C d’un stub 32 bits pour d’autres plateformes :

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

La protection dépendante de la mise en version est déclenchée par un ensemble de fonctionnalités figurant dans le ou les fichiers IDL traités et par le commutateur [**/target**](-target.md) . Par exemple, si l’interface utilise des fonctionnalités prises en charge uniquement sur WindowsÂ 2000 ou une version ultérieure, MIDL génère une protection avec la cible \_ \_ NT50 \_ ou une \_ macro ultérieure.

Les macros Guard, définies dans Rpcndr. h, dépendent de la valeur de WINVER et \_ de \_ winnt Win32 et sont évaluées par le compilateur C/C++.

Si, au moment de la compilation, vous recevez un message d’erreur indiquant que vous avez besoin d’une plateforme spécifique pour exécuter un stub, commencez par vérifier que vous n’avez pas utilisé une fonctionnalité qui n’est pas disponible sur cette plateforme. Les fonctionnalités déclenchant une protection particulière sont répertoriées dans le corps de la protection. Dans l’exemple précédent, le commutateur-Oicf a déclenché la protection. Les fonctionnalités notables de ce type incluent le commutateur [**/Robust**](-robust.md) et l' \[ attribut [**async**](async.md) \] disponible sur WindowsÂ 2000 et versions ultérieures, le constructeur de type [**pipe**](pipe.md) , l’option de compilateur/OIF et les \[ attributs [**\_ Marshal d’utilisateur**](user-marshal.md) \] et \[ [**\_ marshaling de câble**](wire-marshal.md) \] . Les stubs utilisant ces fonctionnalités ne seront pas exécutés sur les systèmes antérieurs.

Si vous savez que votre plateforme cible est correcte pour les fonctionnalités que vous utilisez et que vous recevez toujours une erreur, vous devrez peut-être définir les variables d’environnement de façon appropriée.

**Pour générer des mises en production pour WindowsÂ 2000 ou versions ultérieures**

-   Ajoutez cette ligne à votre Makefile :

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**/Target**](-target.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**async**](async.md)
</dt> <dt>

[**\_UUID asynchrone**](async-uuid.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**canal**](pipe.md)
</dt> <dt>

[**Marshal de câble \_**](wire-marshal.md)
</dt> <dt>

[**Marshal d’utilisateur \_**](user-marshal.md)
</dt> <dt>

[Marshaling des types de données OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




