---
title: Définitions de types, déclarations de construction et importations
description: Les définitions de type, les déclarations de construction et les importations peuvent se produire en dehors du corps de l’interface.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfaces MIDL, définitions de type
- interfaces MIDL, déclarations de construction
- interfaces MIDL, importations
- définitions de types MIDL
- construire des déclarations MIDL
- importations MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829219"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Définitions de types, déclarations de construction et importations

Les définitions de type, les déclarations de construction et les importations peuvent se produire en dehors du corps de l’interface. Toutes les définitions du fichier IDL principal s’affichent dans le fichier d’en-tête généré, et toutes les procédures de toutes les interfaces dans le fichier IDL principal génèrent des routines de stub. Cela permet aux applications qui prennent en charge plusieurs interfaces de fusionner des fichiers IDL en un seul fichier IDL combiné.

Par conséquent, il faut moins de temps pour compiler les fichiers et permet également à MIDL de réduire les redondances dans les stubs générés. Cela peut améliorer considérablement les interfaces d' [**objet**](object.md) grâce à la possibilité de partager du code commun pour les interfaces de base et les interfaces dérivées. Pour les interfaces qui ne sont pas des **objets** , les noms des procédures doivent être uniques dans toutes les interfaces. Pour les interfaces d' **objet** , les noms de procédure doivent être uniques uniquement dans une interface. Notez que plusieurs interfaces ne sont pas autorisées lorsque vous utilisez le commutateur [**/OSF**](-osf.md) .

## <a name="declarative-constructs"></a>Constructions déclaratives

La syntaxe des constructions déclaratives dans le fichier IDL est semblable à celle de C. MIDL prend en charge toutes les constructions déclaratives Microsoft C/C++, à l’exception de ce qui suit :

-   Déclarateurs de style plus anciens qui autorisent la spécification d’un déclarateur sans spécificateur de type, tel que :

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Les déclarations avec initialiseurs (MIDL acceptent uniquement les déclarations qui sont conformes à la syntaxe de l’MIDL [**const**](const.md) ).

Le mot clé [**Import**](import.md) spécifie les noms d’un ou de plusieurs fichiers IDL à importer. La directive import est similaire à la directive [**include**](include.md) C, à ceci près que seuls les types de données sont assimilés dans le fichier IDL d’importation.

## <a name="constant-declaration"></a>Déclaration de constante

La déclaration de constante spécifie des constantes [**booléennes**](boolean.md), des entiers, des caractères, des caractères larges, des chaînes et des **void \** _. Pour plus d’informations, consultez [_ *const* *](const.md).

## <a name="general-declaration"></a>Déclaration générale

Une déclaration générale est semblable à l’instruction C [**typedef**](typedef.md) , avec l’ajout d’attributs de type IDL. Sauf en mode [**/OSF**](-osf.md) , le compilateur MIDL autorise également une déclaration implicite sous la forme d’une définition de variable.

## <a name="function-declaration"></a>Déclaration de fonction

Le déclarateur de fonction est un cas particulier de la déclaration générale. Vous pouvez utiliser les attributs IDL pour spécifier le comportement du type de retour de la fonction et chacun des paramètres.

## <a name="examples"></a>Exemples

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




