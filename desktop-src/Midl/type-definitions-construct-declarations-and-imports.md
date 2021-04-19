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
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509370"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="54cac-109">Définitions de types, déclarations de construction et importations</span><span class="sxs-lookup"><span data-stu-id="54cac-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="54cac-110">Les définitions de type, les déclarations de construction et les importations peuvent se produire en dehors du corps de l’interface.</span><span class="sxs-lookup"><span data-stu-id="54cac-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="54cac-111">Toutes les définitions du fichier IDL principal s’affichent dans le fichier d’en-tête généré, et toutes les procédures de toutes les interfaces dans le fichier IDL principal génèrent des routines de stub.</span><span class="sxs-lookup"><span data-stu-id="54cac-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="54cac-112">Cela permet aux applications qui prennent en charge plusieurs interfaces de fusionner des fichiers IDL en un seul fichier IDL combiné.</span><span class="sxs-lookup"><span data-stu-id="54cac-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="54cac-113">Par conséquent, il faut moins de temps pour compiler les fichiers et permet également à MIDL de réduire les redondances dans les stubs générés.</span><span class="sxs-lookup"><span data-stu-id="54cac-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="54cac-114">Cela peut améliorer considérablement les interfaces d' [**objet**](object.md) grâce à la possibilité de partager du code commun pour les interfaces de base et les interfaces dérivées.</span><span class="sxs-lookup"><span data-stu-id="54cac-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="54cac-115">Pour les interfaces qui ne sont pas des **objets** , les noms des procédures doivent être uniques dans toutes les interfaces.</span><span class="sxs-lookup"><span data-stu-id="54cac-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="54cac-116">Pour les interfaces d' **objet** , les noms de procédure doivent être uniques uniquement dans une interface.</span><span class="sxs-lookup"><span data-stu-id="54cac-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="54cac-117">Notez que plusieurs interfaces ne sont pas autorisées lorsque vous utilisez le commutateur [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="54cac-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="54cac-118">Constructions déclaratives</span><span class="sxs-lookup"><span data-stu-id="54cac-118">Declarative Constructs</span></span>

<span data-ttu-id="54cac-119">La syntaxe des constructions déclaratives dans le fichier IDL est semblable à celle de C. MIDL prend en charge toutes les constructions déclaratives Microsoft C/C++, à l’exception de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="54cac-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="54cac-120">Déclarateurs de style plus anciens qui autorisent la spécification d’un déclarateur sans spécificateur de type, tel que :</span><span class="sxs-lookup"><span data-stu-id="54cac-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="54cac-121">Les déclarations avec initialiseurs (MIDL acceptent uniquement les déclarations qui sont conformes à la syntaxe de l’MIDL [**const**](const.md) ).</span><span class="sxs-lookup"><span data-stu-id="54cac-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="54cac-122">Le mot clé [**Import**](import.md) spécifie les noms d’un ou de plusieurs fichiers IDL à importer.</span><span class="sxs-lookup"><span data-stu-id="54cac-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="54cac-123">La directive import est similaire à la directive [**include**](include.md) C, à ceci près que seuls les types de données sont assimilés dans le fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="54cac-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="54cac-124">Déclaration de constante</span><span class="sxs-lookup"><span data-stu-id="54cac-124">Constant Declaration</span></span>

<span data-ttu-id="54cac-125">La déclaration de constante spécifie des constantes [**booléennes**](boolean.md), des entiers, des caractères, des caractères larges, des chaînes et des **void \*** .</span><span class="sxs-lookup"><span data-stu-id="54cac-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="54cac-126">Pour plus d’informations, consultez [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="54cac-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="54cac-127">Déclaration générale</span><span class="sxs-lookup"><span data-stu-id="54cac-127">General Declaration</span></span>

<span data-ttu-id="54cac-128">Une déclaration générale est semblable à l’instruction C [**typedef**](typedef.md) , avec l’ajout d’attributs de type IDL.</span><span class="sxs-lookup"><span data-stu-id="54cac-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="54cac-129">Sauf en mode [**/OSF**](-osf.md) , le compilateur MIDL autorise également une déclaration implicite sous la forme d’une définition de variable.</span><span class="sxs-lookup"><span data-stu-id="54cac-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="54cac-130">Déclaration de fonction</span><span class="sxs-lookup"><span data-stu-id="54cac-130">Function Declaration</span></span>

<span data-ttu-id="54cac-131">Le déclarateur de fonction est un cas particulier de la déclaration générale.</span><span class="sxs-lookup"><span data-stu-id="54cac-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="54cac-132">Vous pouvez utiliser les attributs IDL pour spécifier le comportement du type de retour de la fonction et chacun des paramètres.</span><span class="sxs-lookup"><span data-stu-id="54cac-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="54cac-133">Exemples</span><span class="sxs-lookup"><span data-stu-id="54cac-133">Examples</span></span>

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

 

 




