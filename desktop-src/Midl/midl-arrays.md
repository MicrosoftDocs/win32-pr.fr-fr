---
title: Tableaux MIDL
description: Tableaux MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- types de données MIDL, tableaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031185"
---
# <a name="midl-arrays"></a><span data-ttu-id="3214a-104">Tableaux MIDL</span><span class="sxs-lookup"><span data-stu-id="3214a-104">MIDL Arrays</span></span>

<span data-ttu-id="3214a-105">Les déclarateurs de tableau apparaissent dans le corps de l’interface du fichier IDL comme l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3214a-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="3214a-106">Partie d’une déclaration générale</span><span class="sxs-lookup"><span data-stu-id="3214a-106">Part of a general declaration</span></span>
-   <span data-ttu-id="3214a-107">Membre d’un déclarateur de structure ou d’Union</span><span class="sxs-lookup"><span data-stu-id="3214a-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="3214a-108">Paramètre d’un appel de procédure distante</span><span class="sxs-lookup"><span data-stu-id="3214a-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="3214a-109">Les limites de chaque dimension du tableau sont exprimées à l’intérieur d’une paire de crochets distincts.</span><span class="sxs-lookup"><span data-stu-id="3214a-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="3214a-110">Une expression qui prend la valeur *n* signifie une limite inférieure de zéro et une limite supérieure de *n-1*.</span><span class="sxs-lookup"><span data-stu-id="3214a-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="3214a-111">Si les crochets sont vides ou contiennent un seul astérisque ( \* ), la limite inférieure est égale à zéro et la limite supérieure est déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3214a-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="3214a-112">Le tableau peut également contenir deux valeurs séparées par des points de suspension représentant les limites inférieure et supérieure du tableau, comme dans l’exemple \[ *inférieur*... *supérieur* \] .</span><span class="sxs-lookup"><span data-stu-id="3214a-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="3214a-113">Microsoft RPC requiert une limite inférieure de zéro.</span><span class="sxs-lookup"><span data-stu-id="3214a-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="3214a-114">Le compilateur MIDL ne reconnaît pas les constructions qui spécifient des limites inférieures égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="3214a-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="3214a-115">Les tableaux peuvent être associés à la taille des attributs du champ : la [**taille \_**](size-is.md) [**maximale \_**](max-is.md), la [**longueur \_ est**](length-is.md), la [**première \_ est**](first-is.md)et la [**dernière \_ la valeur**](last-is.md) de la taille du tableau ou de la partie du tableau qui contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="3214a-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="3214a-116">Ces attributs de champ identifient le paramètre, le champ de structure ou la constante qui spécifie la dimension ou l’index du tableau.</span><span class="sxs-lookup"><span data-stu-id="3214a-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="3214a-117">Le tableau doit être associé à l’identificateur spécifié par l’attribut field de la manière suivante : quand le tableau est un paramètre, l’identificateur doit également être un paramètre de la même fonction. Lorsque le tableau est un champ de structure, l’identificateur doit être un autre champ de structure de cette même structure.</span><span class="sxs-lookup"><span data-stu-id="3214a-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="3214a-118">Un tableau est appelé « conforme » si la limite supérieure d’une dimension est déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3214a-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="3214a-119">(Seules les limites supérieures peuvent être déterminées au moment de l’exécution.) Pour déterminer la limite supérieure, la déclaration de tableau doit inclure [**une \_ taille**](size-is.md) ou un attribut [**Max \_ est**](max-is.md) un attribut.</span><span class="sxs-lookup"><span data-stu-id="3214a-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="3214a-120">Un tableau est appelé « varying » quand ses limites sont déterminées au moment de la compilation, mais la plage d’éléments transmis est déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3214a-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="3214a-121">Pour déterminer la plage d’éléments transmis, la déclaration de tableau doit inclure [**une \_ longueur**](length-is.md), [**First \_ is**](first-is.md)ou [**Last \_ is**](last-is.md) Attribute.</span><span class="sxs-lookup"><span data-stu-id="3214a-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="3214a-122">Un tableau variable conforme (également appelé « Open ») est un tableau dont la limite supérieure et la plage d’éléments transmis sont déterminées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3214a-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="3214a-123">Au maximum, un tableau variable conforme ou conforme peut être imbriqué dans une structure C et doit être le dernier élément de la structure.</span><span class="sxs-lookup"><span data-stu-id="3214a-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="3214a-124">En revanche, les tableaux à variation non conformes peuvent apparaître n’importe où dans une structure.</span><span class="sxs-lookup"><span data-stu-id="3214a-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="3214a-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="3214a-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="3214a-126">Pour plus d’informations, consultez [tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="3214a-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="3214a-127">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="3214a-127">Multidimensional Arrays</span></span>

<span data-ttu-id="3214a-128">L’utilisateur peut déclarer des types qui sont des tableaux, puis déclarer des tableaux d’objets de ce type.</span><span class="sxs-lookup"><span data-stu-id="3214a-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="3214a-129">La sémantique des tableaux *m*-dimensionnels de types de tableau à *n* dimensions est identique à la sémantique des tableaux *m* + *n*-dimension.</span><span class="sxs-lookup"><span data-stu-id="3214a-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="3214a-130">Par exemple, le type RECT \_ type peut être défini comme un tableau à deux dimensions et la variable *Rect* peut être définie en tant que tableau de \_ type Rect.</span><span class="sxs-lookup"><span data-stu-id="3214a-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="3214a-131">Cette valeur est équivalente à l' *équivalent \_ Rect* du tableau à trois dimensions :</span><span class="sxs-lookup"><span data-stu-id="3214a-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="3214a-132">Microsoft RPC est orienté C.</span><span class="sxs-lookup"><span data-stu-id="3214a-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="3214a-133">Conformément aux conventions de langage C, seule la première dimension d’un tableau multidimensionnel peut être déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3214a-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="3214a-134">L’interopérabilité avec des tableaux IDL DCE prenant en charge d’autres langues est limitée à :</span><span class="sxs-lookup"><span data-stu-id="3214a-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="3214a-135">Tableaux multidimensionnels avec limites (au moment de la compilation).</span><span class="sxs-lookup"><span data-stu-id="3214a-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="3214a-136">Tableaux multidimensionnels avec toutes les limites constantes, à l’exception de la première dimension.</span><span class="sxs-lookup"><span data-stu-id="3214a-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="3214a-137">La limite supérieure et la plage d’éléments transmis de la première dimension dépendent du Runtime.</span><span class="sxs-lookup"><span data-stu-id="3214a-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="3214a-138">Tableau unidimensionnel avec une limite inférieure de zéro.</span><span class="sxs-lookup"><span data-stu-id="3214a-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="3214a-139">Lorsque l' **\[** [](string.md) **\]** attribut de chaîne est utilisé sur des tableaux multidimensionnels, l’attribut s’applique au tableau le plus à droite.</span><span class="sxs-lookup"><span data-stu-id="3214a-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="3214a-140">Tableaux de pointeurs</span><span class="sxs-lookup"><span data-stu-id="3214a-140">Arrays of Pointers</span></span>

<span data-ttu-id="3214a-141">Les pointeurs de référence doivent pointer vers des données valides.</span><span class="sxs-lookup"><span data-stu-id="3214a-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="3214a-142">L’application cliente doit allouer toute la mémoire pour un **\[** [**dans**](in.md) **\]** ou **\[** **dans,**[](out-idl.md) un **\]** tableau de pointeurs de référence, en particulier lorsque le tableau est associé à **\[ dans \]**, ou **\[** **dans, out \]**, la **\[** [**longueur \_ est**](length-is.md)ou que la **\]** **\[** [**dernière valeur \_ est**](last-is.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3214a-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="3214a-143">L’application cliente doit également initialiser tous les éléments de tableau avant l’appel.</span><span class="sxs-lookup"><span data-stu-id="3214a-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="3214a-144">Avant de retourner au client, l’application serveur doit vérifier que tous les éléments de tableau de la plage transmis pointent vers un stockage valide.</span><span class="sxs-lookup"><span data-stu-id="3214a-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="3214a-145">Côté serveur, le stub alloue le stockage pour tous les éléments de tableau, quelle que soit la **\[** [**longueur \_**](length-is.md) **\]** ou la **\[** [**dernière \_**](last-is.md) **\]** valeur au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="3214a-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="3214a-146">Cette fonctionnalité peut affecter les performances de votre application.</span><span class="sxs-lookup"><span data-stu-id="3214a-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="3214a-147">Aucune restriction n’est placée sur les tableaux de pointeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="3214a-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="3214a-148">Sur le client et sur le serveur, le stockage est alloué pour les pointeurs null.</span><span class="sxs-lookup"><span data-stu-id="3214a-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="3214a-149">Lorsque les pointeurs ne sont pas null, les données sont placées dans un stockage préalloué.</span><span class="sxs-lookup"><span data-stu-id="3214a-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="3214a-150">Un déclarateur de pointeur facultatif peut précéder le déclarateur de tableau.</span><span class="sxs-lookup"><span data-stu-id="3214a-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="3214a-151">Lorsque les pointeurs de référence incorporés sont des **\[** [](out-idl.md) **\]** paramètres de sortie uniquement, le code du gestionnaire de serveur doit assigner des valeurs valides au tableau de pointeurs de référence.</span><span class="sxs-lookup"><span data-stu-id="3214a-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="3214a-152">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3214a-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="3214a-153">Les stubs générés allouent le tableau et assignent des valeurs NULL à tous les pointeurs incorporés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3214a-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 