---
title: mot clé Union (RPC)
description: Les unions requièrent des mots clés MIDL spéciaux pour prendre en charge leur utilisation avec l’appel de procédure distante (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315240"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="94110-103">mot clé Union (RPC)</span><span class="sxs-lookup"><span data-stu-id="94110-103">union keyword (RPC)</span></span>

<span data-ttu-id="94110-104">Certaines fonctionnalités du langage C, telles que les unions, requièrent des mots clés MIDL spéciaux pour prendre en charge leur utilisation dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="94110-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="94110-105">Une Union dans le langage C est une variable qui contient des objets de différents types et tailles.</span><span class="sxs-lookup"><span data-stu-id="94110-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="94110-106">Le développeur crée généralement une variable pour effectuer le suivi des types stockés dans l’Union.</span><span class="sxs-lookup"><span data-stu-id="94110-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="94110-107">Pour fonctionner correctement dans un environnement distribué, la variable qui indique le type de l’Union, ou *discriminante*, doit également être disponible pour l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="94110-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="94110-108">MIDL fournit le \[ [**\_ type de commutateur**](/windows/desktop/Midl/switch-type) \] et le \[ [**commutateur \_ est**](/windows/desktop/Midl/switch-is) un \] mot clé pour identifier le type et le nom discriminante.</span><span class="sxs-lookup"><span data-stu-id="94110-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="94110-109">MIDL exige que le discriminante soit transmis avec l’Union de deux manières :</span><span class="sxs-lookup"><span data-stu-id="94110-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="94110-110">L’Union et le discriminante doivent être fournis en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="94110-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="94110-111">L’Union et le discriminante doivent être empaquetés dans une structure.</span><span class="sxs-lookup"><span data-stu-id="94110-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="94110-112">Deux types fondamentaux d’unions discriminées sont fournis par MIDL : [**\_ Union**](/windows/desktop/Midl/nonencapsulated-unions) et [**\_ Union encapsulée**](/windows/desktop/Midl/encapsulated-unions).</span><span class="sxs-lookup"><span data-stu-id="94110-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="94110-113">Le discriminante d’une Union non encapsulée est un autre paramètre si l’Union est un paramètre.</span><span class="sxs-lookup"><span data-stu-id="94110-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="94110-114">Il s’agit d’un autre champ si l’Union est un champ d’une structure.</span><span class="sxs-lookup"><span data-stu-id="94110-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="94110-115">La définition d’une Union encapsulée est transformée en définition de structure dont le premier champ est le discriminante et dont le deuxième et le dernier champs sont l’Union.</span><span class="sxs-lookup"><span data-stu-id="94110-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="94110-116">L’exemple suivant montre comment fournir les paramètres Union et discriminante :</span><span class="sxs-lookup"><span data-stu-id="94110-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="94110-117">Dans l’exemple précédent, l’Union peut contenir une valeur unique : **short**, **float** ou **char**.</span><span class="sxs-lookup"><span data-stu-id="94110-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="94110-118">La définition de type pour l’Union comprend l’attribut de **\_ type de commutateur** MIDL qui spécifie le type de discriminante.</span><span class="sxs-lookup"><span data-stu-id="94110-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="94110-119">Ici, \[ \_ type de commutateur (short) \] spécifie que le discriminante est de type **short**.</span><span class="sxs-lookup"><span data-stu-id="94110-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="94110-120">Le commutateur doit être un type entier.</span><span class="sxs-lookup"><span data-stu-id="94110-120">The switch must be an integer type.</span></span>

<span data-ttu-id="94110-121">Si l’Union est un membre d’une structure, discriminante doit être un membre de la même structure.</span><span class="sxs-lookup"><span data-stu-id="94110-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="94110-122">Si l’Union est un paramètre, discriminante doit être un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="94110-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="94110-123">Le prototype de la fonction **UnionParamProc** dans l’exemple précédent montre le *sUtype* discriminante en tant que dernier paramètre de l’appel.</span><span class="sxs-lookup"><span data-stu-id="94110-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="94110-124">(Le discriminante peut apparaître à n’importe quelle position dans l’appel.) Le type du paramètre spécifié dans le **\[ commutateur \_ est \]** attribute doit correspondre au type spécifié dans l’attribut de **\[ \_ type \] de commutateur** .</span><span class="sxs-lookup"><span data-stu-id="94110-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="94110-125">L’exemple suivant illustre l’utilisation d’une structure unique qui empaquette le discriminante avec l’Union :</span><span class="sxs-lookup"><span data-stu-id="94110-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="94110-126">Le compilateur Microsoft RPC MIDL autorise les déclarations d’Union en dehors des constructions [**typedef**](/windows/desktop/Midl/typedef) .</span><span class="sxs-lookup"><span data-stu-id="94110-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="94110-127">Cette fonctionnalité est une extension de l’IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="94110-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="94110-128">Pour plus d’informations, consultez [**Union**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="94110-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 