---
title: Gestion des définitions dans les fichiers IDL
description: Cette page décrit les raisons pour lesquelles les symboles définis avec une \ define disparaissent des fichiers H générés par le compilateur MIDL et ce que vous pouvez en faire. Cette explication s’applique à tous les fichiers traités par MIDL, tels que les fichiers \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL du compilateur MIDL, traitant des définitions
- définit MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029166"
---
# <a name="dealing-with-defines-in-idl-files"></a>Gestion des \# définitions dans les fichiers IDL

Cette page décrit les raisons pour lesquelles les symboles définis avec une **\# définition** disparaissent des fichiers H générés par le compilateur MIDL et ce que vous pouvez en faire. Cette explication s’applique à tous les fichiers traités par MIDL, tels que les \* fichiers. idl, \* . ACF et \* . h.

La disparition des symboles de **\# définition** est le résultat de la délégation par MIDL du prétraitement des fichiers d’entrée à un préprocesseur. Par défaut, le préprocesseur est un préprocesseur C/C++ de l’environnement de génération. Après le prétraitement, le processus MIDL de flux d’entrée reçoit uniquement des \# directives de préprocesseur de ligne. En particulier, le préprocesseur déroulera toutes les définitions de macros dans les fichiers d’entrée, et par conséquent, MIDL ne peut pas détecter sa présence. Par conséquent, lorsque MIDL réplique les définitions de types à partir d’un fichier d’entrée dans le fichier H généré, les définitions ne \# sont pas répliquées. Par conséquent, n’utilisez pas \# de définit directement dans les fichiers IDL s’ils doivent être utilisés ultérieurement à partir du fichier H généré.

Les quatre solutions de contournement suivantes sont recommandées :

-   Utilisez la spécification de Déclaration [**const**](const.md) .
-   Utilisez des fichiers d’en-tête distincts qui sont importés ou inclus dans le fichier IDL, puis inclus ultérieurement dans le code source C.
-   Utilisez des constantes d’énumération dans le fichier IDL.
-   Utilisez [**le \_ Devis RPC**](cpp-quote.md) pour reproduire la **\# définition** dans le fichier d’en-tête généré.

Vous pouvez reproduire des constantes de manifeste à l’aide de la **syntaxe de déclaration de constante IDL**. Notez que le [**const**](const.md) dans la déclaration de constante IDL est différent de la sémantique **const** C/C++ et introduit simplement une constante nommée pour une compilation IDL. Par exemple :

``` syntax
const short ARRSIZE = 10
```

Cet exemple spécifie que **ARRSIZE** est une constante avec une valeur de 10. Les constantes nommées peuvent être utilisées dans les déclarateurs de tableau IDL et dans d’autres emplacements où un programmeur C utiliserait un manifeste défini. En outre, cette syntaxe entraîne la génération de la ligne suivante dans le fichier d’en-tête :

``` syntax
#define ARRSIZE 10
```

Une autre façon de gérer **\#** les instructions de définition consiste à les empaqueter dans un fichier d’en-tête distinct, soit dans un fichier dédié pour **\#** définir des instructions, soit dans un fichier qui contient uniquement des définitions de type. Un fichier qui contient uniquement des directives de préprocesseur peut être inclus en toute sécurité à la fois par le fichier IDL et les fichiers sources C. Bien que les directives ne soient pas disponibles dans le fichier d’en-tête généré par le compilateur MIDL, le programme source C peut inclure le fichier d’en-tête distinct. De la même façon, un fichier d’en-tête avec des **\#** instructions de définition et des définitions de type standard peut être importé à partir de votre fichier IDL. Cette approche encapsule les **\#** instructions define et typedef en les utilisant dans un fichier H, de sorte que les **\#** symboles de définition ne sont pas utilisés directement dans le fichier IDL d’importation. L’importation d’un fichier d’en-tête ou d’un fichier IDL dans un autre fichier IDL empêche les instructions typedef d’être répliquées dans le fichier H généré par MIDL (contrairement aux **\#** instructions Include). Cette approche permet au fichier d’en-tête d’origine d’être référencé en toute sécurité à partir du code C le long du fichier H généré sans avoir de problème avec les définitions dupliquées.

L’utilisation de constantes d’énumération dans le fichier IDL est également effective. Ces constantes peuvent être utilisées dans des expressions constantes dans IDL, par exemple dans des déclarateurs de tableau. Les constantes d’énumération ne sont pas supprimées lors des premières phases de la compilation MIDL par le préprocesseur du compilateur C. ainsi, les constantes d’énumération sont disponibles dans le fichier d’en-tête généré par le compilateur MIDL. Prenons l'instruction suivante :

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Cette instruction ne sera pas supprimée pendant la compilation MIDL par le préprocesseur C et le typedef sera répliqué dans le fichier H généré. La constante MAXSTRINGCOUNT est disponible pour les programmes source C qui incluent le fichier d’en-tête généré par le compilateur MIDL.

Enfin, la directive de [**\_ citation CPP**](cpp-quote.md) de MIDL peut être utilisée pour écrire une chaîne arbitraire directement dans le fichier H généré. Par exemple, pour obtenir la constante de manifeste utilisée précédemment sur cette page avec le **\_ guillemet CPP**, vous pouvez utiliser l’instruction suivante :

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Cette instruction entraîne la génération de la ligne suivante dans le fichier d’en-tête :

``` syntax
#define ARRSIZE 10
```

 

 




