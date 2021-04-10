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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029851"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="5e8e8-105">Différences entre MIDL et MkTypLib</span><span class="sxs-lookup"><span data-stu-id="5e8e8-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="5e8e8-106">L’outil Mktyplib.exe est obsolète.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="5e8e8-107">Utilisez plutôt le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="5e8e8-108">Il existe quelques domaines clés dans lesquels le compilateur MIDL diffère de MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="5e8e8-109">La plupart de ces différences se produisent, car MIDL est orienté vers la syntaxe C plutôt que MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="5e8e8-110">En général, vous pouvez utiliser la syntaxe MIDL dans vos fichiers IDL.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="5e8e8-111">Toutefois, si vous devez compiler un fichier ODL existant ou maintenir la compatibilité avec MkTypLib, utilisez l’option du compilateur [**/Mktyplib203**](-mktyplib203.md) MIDL pour forcer le comportement de midl comme Mkktyplib.exe, version 2,03.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="5e8e8-112">(Il s’agit de la dernière version de l’outil MkTypLib.) Plus précisément, l’option **/mktyplib203** résout ces différences :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="5e8e8-113">syntaxe typedef pour les types de données complexes</span><span class="sxs-lookup"><span data-stu-id="5e8e8-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="5e8e8-114">Dans MkTypLib, les deux définitions suivantes génèrent un \_ enregistrement TKIND pour « This \_ struct » dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="5e8e8-115">La balise « struct struct \_ » est facultative et, si elle est utilisée, n’apparaît pas dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="5e8e8-116">Si une balise facultative est manquante, MIDL la génère, en ajoutant une balise à la définition fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="5e8e8-117">Étant donné que la première définition a une balise, MIDL génère un \_ enregistrement TKIND pour « This \_ struct » et un \_ alias TKIND pour « This struct \_ » (définissant « This \_ struct » en tant qu’alias pour « \_ tag struct »).</span><span class="sxs-lookup"><span data-stu-id="5e8e8-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="5e8e8-118">Étant donné que la balise est manquante dans la deuxième définition, MIDL génère un \_ enregistrement TKIND pour un nom tronqué, interne à MIDL, qui n’est pas significatif pour l’utilisateur et un \_ alias TKIND pour « ce \_ struct ».</span><span class="sxs-lookup"><span data-stu-id="5e8e8-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="5e8e8-119">Cela a des implications potentielles pour les navigateurs de bibliothèques de types qui affichent simplement le nom d’un enregistrement dans leur interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="5e8e8-120">Si vous vous attendez \_ à ce qu’un enregistrement TKIND ait un nom réel, les noms non reconnaissables peuvent apparaître dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="5e8e8-121">Ce comportement s’applique également aux définitions d' [**Union**](union.md) et d' [**enum**](enum.md) , avec le compilateur MIDL qui génère des \_ unions TKIND et des \_ énumérations TKIND, respectivement.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="5e8e8-122">MIDL autorise également les définitions de [**struct**](struct.md), d' [**Union**](union.md)et d' [**énumération**](enum.md) de style C.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="5e8e8-123">Par exemple, la définition suivante est légale dans MIDL :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="5e8e8-124">types de données Boolean</span><span class="sxs-lookup"><span data-stu-id="5e8e8-124">Boolean data types</span></span>

    <span data-ttu-id="5e8e8-125">Dans MkTypLib, le type de base [**booléen**](boolean.md) et le type de données mktyplib bool sont équivalents à VT \_ bool, qui correspond à variant \_ bool et qui est défini comme [**short**](short.md).</span><span class="sxs-lookup"><span data-stu-id="5e8e8-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="5e8e8-126">Dans MIDL, le type de base **booléen** est équivalent à VT \_ UI1, qui est défini comme [**unsigned char**](unsigned.md)et le type de données bool est défini comme [**long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="5e8e8-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="5e8e8-127">Cela génère des difficultés si vous combinez la syntaxe IDL et la syntaxe ODL dans le même fichier tout en essayant de maintenir la compatibilité avec MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="5e8e8-128">Étant donné que les types de données sont de tailles différentes, le code de marshaling ne correspondra pas à ce qui est décrit dans les informations de type.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="5e8e8-129">Si vous souhaitez un \_ booléen VT dans votre bibliothèque de types, vous devez utiliser le \_ type de données variant bool.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="5e8e8-130">Définitions de GUID dans les fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e8e8-130">GUID definitions in header files</span></span>

    <span data-ttu-id="5e8e8-131">Dans MkTypLib, les GUID sont définis dans le fichier d’en-tête avec une macro qui peut être compilée de manière conditionnelle pour générer une prédéfinition de GUID ou un GUID instancié.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="5e8e8-132">MIDL place normalement les prédéfinitions de GUID dans ses fichiers d’en-tête générés et les instanciations de GUID uniquement dans le fichier généré par le commutateur [**/IID**](-iid.md) .</span><span class="sxs-lookup"><span data-stu-id="5e8e8-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="5e8e8-133">Les différences de comportement suivantes ne peuvent pas être résolues à l’aide du commutateur [**/mktyplib203**](-mktyplib203.md) :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="5e8e8-134">Respect de la casse</span><span class="sxs-lookup"><span data-stu-id="5e8e8-134">Case sensitivity</span></span>

    <span data-ttu-id="5e8e8-135">MIDL respecte la casse, mais pas l’Automation OLE.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="5e8e8-136">Portée des symboles dans une déclaration enum</span><span class="sxs-lookup"><span data-stu-id="5e8e8-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="5e8e8-137">Dans MkTypLib, l’étendue des symboles d’une énumération est locale.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="5e8e8-138">Dans MIDL, la portée des symboles d’une énumération est globale, comme c’est le cas en C. Par exemple, le code suivant est compilé dans MkTypLib, mais génère une erreur de nom dupliqué dans MIDL :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="5e8e8-139">Portée de l’attribut public</span><span class="sxs-lookup"><span data-stu-id="5e8e8-139">Scope of public attribute</span></span>

    <span data-ttu-id="5e8e8-140">Si vous appliquez l’attribut [**public**](public.md) à un bloc d’interface, mktyplib traite chaque typedef dans ce bloc d’interface comme public.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="5e8e8-141">Avec MIDL, vous devez appliquer explicitement l’attribut **public** aux typedefs que vous souhaitez public.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="5e8e8-142">Ordre de recherche importlib</span><span class="sxs-lookup"><span data-stu-id="5e8e8-142">Importlib search order</span></span>

    <span data-ttu-id="5e8e8-143">Si vous importez plusieurs bibliothèques de types et si ces bibliothèques contiennent des références dupliquées, MkTypLib le résout à l’aide de la première référence trouvée.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="5e8e8-144">MIDL utilise la dernière référence qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="5e8e8-145">Par exemple, étant donné la syntaxe ODL suivante, la bibliothèque C utilise le typedef MUGISSEMENT de la bibliothèque A si vous compilez avec MkTypLib et le typedef MUGISSEMENT de la bibliothèque B si vous compilez avec MIDL :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

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

    <span data-ttu-id="5e8e8-146">La solution de contournement appropriée consiste à qualifier chaque référence avec le nom correct de la bibliothèque d’importation, comme suit :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="5e8e8-147">Type de données VOID non reconnu</span><span class="sxs-lookup"><span data-stu-id="5e8e8-147">VOID data type not recognized</span></span>

    <span data-ttu-id="5e8e8-148">MIDL reconnaît le type de données [**void**](void.md) du langage C et ne reconnaît pas le type de données void OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="5e8e8-149">Si vous avez un fichier ODL qui utilise VOID, placez cette définition en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="5e8e8-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="5e8e8-150">Notation exponentielle</span><span class="sxs-lookup"><span data-stu-id="5e8e8-150">Exponential notation</span></span>

    <span data-ttu-id="5e8e8-151">MIDL exige que les valeurs exprimées en notation exponentielle soient contenues entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="5e8e8-152">Par exemple, « -2,5 E + 3 »</span><span class="sxs-lookup"><span data-stu-id="5e8e8-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="5e8e8-153">Valeurs et constantes LCID</span><span class="sxs-lookup"><span data-stu-id="5e8e8-153">LCID values and constants</span></span>

    <span data-ttu-id="5e8e8-154">En général, MIDL ne prend pas en compte le LCID lors de l’analyse des fichiers.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="5e8e8-155">Pour forcer ce comportement pour une valeur, ou si vous devez utiliser une notation spécifique aux paramètres régionaux lors de la définition d’une constante, mettez-la entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="5e8e8-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="5e8e8-156">Pour plus d’informations, consultez [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)et [marshaling des types de données OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="5e8e8-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




