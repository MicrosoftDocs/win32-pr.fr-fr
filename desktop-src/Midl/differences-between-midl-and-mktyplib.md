---
title: Différences entre MIDL et MkTypLib
description: Différences entre MIDL et MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL et ODL MIDL, différences entre MIDL et MkTypLib
- MIDL de MkTypLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093666"
---
# <a name="differences-between-midl-and-mktyplib"></a>Différences entre MIDL et MkTypLib

> [!Note]  
> L’outil Mktyplib.exe est obsolète. Utilisez plutôt le compilateur MIDL.

 

Il existe quelques domaines clés dans lesquels le compilateur MIDL diffère de MkTypLib. La plupart de ces différences se produisent, car MIDL est orienté vers la syntaxe C plutôt que MkTypLib.

En général, vous pouvez utiliser la syntaxe MIDL dans vos fichiers IDL. Toutefois, si vous devez compiler un fichier ODL existant ou maintenir la compatibilité avec MkTypLib, utilisez l’option du compilateur [**/Mktyplib203**](-mktyplib203.md) MIDL pour forcer le comportement de midl comme Mkktyplib.exe, version 2,03. (Il s’agit de la dernière version de l’outil MkTypLib.) Plus précisément, l’option **/mktyplib203** résout ces différences :

-   syntaxe typedef pour les types de données complexes

    Dans MkTypLib, les deux définitions suivantes génèrent un \_ enregistrement TKIND pour « This \_ struct » dans la bibliothèque de types. La balise « struct struct \_ » est facultative et, si elle est utilisée, n’apparaît pas dans la bibliothèque de types.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Si une balise facultative est manquante, MIDL la génère, en ajoutant une balise à la définition fournie par l’utilisateur. Étant donné que la première définition a une balise, MIDL génère un \_ enregistrement TKIND pour « This \_ struct » et un \_ alias TKIND pour « This struct \_ » (définissant « This \_ struct » en tant qu’alias pour « \_ tag struct »). Étant donné que la balise est manquante dans la deuxième définition, MIDL génère un \_ enregistrement TKIND pour un nom tronqué, interne à MIDL, qui n’est pas significatif pour l’utilisateur et un \_ alias TKIND pour « ce \_ struct ».

    Cela a des implications potentielles pour les navigateurs de bibliothèques de types qui affichent simplement le nom d’un enregistrement dans leur interface utilisateur. Si vous vous attendez \_ à ce qu’un enregistrement TKIND ait un nom réel, les noms non reconnaissables peuvent apparaître dans l’interface utilisateur. Ce comportement s’applique également aux définitions d' [**Union**](union.md) et d' [**enum**](enum.md) , avec le compilateur MIDL qui génère des \_ unions TKIND et des \_ énumérations TKIND, respectivement.

    MIDL autorise également les définitions de [**struct**](struct.md), d' [**Union**](union.md)et d' [**énumération**](enum.md) de style C. Par exemple, la définition suivante est légale dans MIDL :

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   types de données Boolean

    Dans MkTypLib, le type de base [**booléen**](boolean.md) et le type de données mktyplib bool sont équivalents à VT \_ bool, qui correspond à variant \_ bool et qui est défini comme [**short**](short.md). Dans MIDL, le type de base **booléen** est équivalent à VT \_ UI1, qui est défini comme [**unsigned char**](unsigned.md)et le type de données bool est défini comme [**long**](long.md). Cela génère des difficultés si vous combinez la syntaxe IDL et la syntaxe ODL dans le même fichier tout en essayant de maintenir la compatibilité avec MkTypLib. Étant donné que les types de données sont de tailles différentes, le code de marshaling ne correspondra pas à ce qui est décrit dans les informations de type. Si vous souhaitez un \_ booléen VT dans votre bibliothèque de types, vous devez utiliser le \_ type de données variant bool.

-   Définitions de GUID dans les fichiers d’en-tête

    Dans MkTypLib, les GUID sont définis dans le fichier d’en-tête avec une macro qui peut être compilée de manière conditionnelle pour générer une prédéfinition de GUID ou un GUID instancié. MIDL place normalement les prédéfinitions de GUID dans ses fichiers d’en-tête générés et les instanciations de GUID uniquement dans le fichier généré par le commutateur [**/IID**](-iid.md) .

Les différences de comportement suivantes ne peuvent pas être résolues à l’aide du commutateur [**/mktyplib203**](-mktyplib203.md) :

-   Respect de la casse

    MIDL respecte la casse, mais pas l’Automation OLE.

-   Portée des symboles dans une déclaration enum

    Dans MkTypLib, l’étendue des symboles d’une énumération est locale. Dans MIDL, la portée des symboles d’une énumération est globale, comme c’est le cas en C. Par exemple, le code suivant est compilé dans MkTypLib, mais génère une erreur de nom dupliqué dans MIDL :

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Portée de l’attribut public

    Si vous appliquez l’attribut [**public**](public.md) à un bloc d’interface, mktyplib traite chaque typedef dans ce bloc d’interface comme public. Avec MIDL, vous devez appliquer explicitement l’attribut **public** aux typedefs que vous souhaitez public.

-   Ordre de recherche importlib

    Si vous importez plusieurs bibliothèques de types et si ces bibliothèques contiennent des références dupliquées, MkTypLib le résout à l’aide de la première référence trouvée. MIDL utilise la dernière référence qu’il trouve. Par exemple, étant donné la syntaxe ODL suivante, la bibliothèque C utilise le typedef MUGISSEMENT de la bibliothèque A si vous compilez avec MkTypLib et le typedef MUGISSEMENT de la bibliothèque B si vous compilez avec MIDL :

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    La solution de contournement appropriée consiste à qualifier chaque référence avec le nom correct de la bibliothèque d’importation, comme suit :

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   Type de données VOID non reconnu

    MIDL reconnaît le type de données [**void**](void.md) du langage C et ne reconnaît pas le type de données void OLE Automation. Si vous avez un fichier ODL qui utilise VOID, placez cette définition en haut du fichier :

    ``` syntax
#define VOID void
    ```

-   Notation exponentielle

    MIDL exige que les valeurs exprimées en notation exponentielle soient contenues entre guillemets. Par exemple, « -2,5 E + 3 »

-   Valeurs et constantes LCID

    En général, MIDL ne prend pas en compte le LCID lors de l’analyse des fichiers. Pour forcer ce comportement pour une valeur, ou si vous devez utiliser une notation spécifique aux paramètres régionaux lors de la définition d’une constante, mettez-la entre guillemets.

Pour plus d’informations, consultez [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)et [marshaling des types de données OLE](marshaling-ole-data-types.md).

 

 




