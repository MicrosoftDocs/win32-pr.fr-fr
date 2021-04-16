---
title: Attribut transmit_as
description: L’attribut \ transmit \_ As \ offre un moyen de contrôler le marshaling des données sans se soucier du marshaling des données à un niveau bas \ 8212 ; autrement dit, sans vous soucier de la taille des données ou de l’échange d’octets dans un environnement hétérogène.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Appel de procédure distante RPC, attributs, transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382352"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="61afa-105">L' \_ attribut transmit As</span><span class="sxs-lookup"><span data-stu-id="61afa-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="61afa-106">L' **\[** attribut [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) **\]** offre un moyen de contrôler le marshaling des données sans se soucier du marshaling des données à un niveau faible, autrement dit, sans se soucier de la taille des données ou de l’échange d’octets dans un environnement hétérogène.</span><span class="sxs-lookup"><span data-stu-id="61afa-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="61afa-107">En vous permettant de réduire la quantité de données transmises sur le réseau, l’attribut **\[ transmit \_ As \]** peut rendre votre application plus efficace.</span><span class="sxs-lookup"><span data-stu-id="61afa-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="61afa-108">L’attribut **\[ transmettre \_ en tant \] que** permet de spécifier un type de données que les stubs RPC transmettront sur le réseau au lieu d’utiliser le type de données fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="61afa-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="61afa-109">Vous fournissez des routines qui convertissent le type de données vers et à partir du type utilisé pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="61afa-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="61afa-110">Vous devez également fournir des routines pour libérer la mémoire utilisée pour le type de données et le type transmis.</span><span class="sxs-lookup"><span data-stu-id="61afa-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="61afa-111">Par exemple, le code suivant définit le **\_ type** de transmission en tant que type de données transmis pour toutes les données d’application spécifiées comme étant de type **\_ spec**:</span><span class="sxs-lookup"><span data-stu-id="61afa-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="61afa-112">Le tableau suivant décrit les quatre noms de routine fournis par le programmeur.</span><span class="sxs-lookup"><span data-stu-id="61afa-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="61afa-113">**Type** est le type de données connu de l’application, **et le type de \_ transmission est** le type de données utilisé pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="61afa-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="61afa-114">Routine</span><span class="sxs-lookup"><span data-stu-id="61afa-114">Routine</span></span>                                                 | <span data-ttu-id="61afa-115">Description</span><span class="sxs-lookup"><span data-stu-id="61afa-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61afa-116">**type \_ à transtransmission \_**</span><span class="sxs-lookup"><span data-stu-id="61afa-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="61afa-117">Alloue un objet du type transmis et convertit le type d’application en type transmis sur le réseau (appelant et objet appelé).</span><span class="sxs-lookup"><span data-stu-id="61afa-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="61afa-118">**Type \_ à partir de l' \_ émetteur**</span><span class="sxs-lookup"><span data-stu-id="61afa-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="61afa-119">Convertit le type transmis en type d’application (appelant et objet appelé).</span><span class="sxs-lookup"><span data-stu-id="61afa-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="61afa-120">**Tapez \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="61afa-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="61afa-121">Libère les ressources utilisées par le type d’application (objet appelé uniquement).</span><span class="sxs-lookup"><span data-stu-id="61afa-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="61afa-122">**Type de transmission \_ libre \_**</span><span class="sxs-lookup"><span data-stu-id="61afa-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="61afa-123">Libère le stockage retourné par le **type ***\_*** à \_** la routine de transmission (appelant et objet appelé).</span><span class="sxs-lookup"><span data-stu-id="61afa-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="61afa-124">En dehors de ces quatre fonctions fournies par le programmeur, le type transmis n’est pas manipulé par l’application.</span><span class="sxs-lookup"><span data-stu-id="61afa-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="61afa-125">Le type transmis est défini uniquement pour déplacer des données sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="61afa-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="61afa-126">Une fois les données converties dans le type utilisé par l’application, la mémoire utilisée par le type transmis est libérée.</span><span class="sxs-lookup"><span data-stu-id="61afa-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="61afa-127">Ces routines fournies par le programmeur sont fournies par le client ou l’application serveur en fonction des attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="61afa-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="61afa-128">Si le paramètre est **\[** uniquement [**dans**](/windows/desktop/Midl/in) **\]** , le client transmet au serveur.</span><span class="sxs-lookup"><span data-stu-id="61afa-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="61afa-129">Le client a besoin du type pour fournir des fonctions **\_ de \_** transmission **\_ gratuites \_** et de type.</span><span class="sxs-lookup"><span data-stu-id="61afa-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="61afa-130">Le serveur a besoin **du \_ type \_ à partir des fonctions de** transmission et de **type \_ Free \_ inst** .</span><span class="sxs-lookup"><span data-stu-id="61afa-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="61afa-131">Pour un **\[** paramètre en [**sortie**](/windows/desktop/Midl/out-idl) **\]** seule, le serveur transmet au client.</span><span class="sxs-lookup"><span data-stu-id="61afa-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="61afa-132">L’application serveur doit implémenter **le \_ type \_ pour** transmettre et taper des fonctions de transmission **\_ \_ gratuites** , tandis que le programme client doit fournir le **type \_ à partir de \_** la fonction de transmission.</span><span class="sxs-lookup"><span data-stu-id="61afa-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="61afa-133">Pour les objets **de \_ type** de transmission temporaire, le stub appelle le type de transmission \*\*\*\*\*\_\*\*\* libre \_\*\* pour libérer toute mémoire allouée par un appel de **type \_ à \_** la transmission.</span><span class="sxs-lookup"><span data-stu-id="61afa-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="61afa-134">Certaines instructions s’appliquent à l’instance de type d’application.</span><span class="sxs-lookup"><span data-stu-id="61afa-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="61afa-135">Si le type d’application est un pointeur ou contient un pointeur, le **type** \_ **de \_** la routine de transmission doit allouer de la mémoire pour les données sur lesquelles les pointeurs pointent (l’objet de type d’application lui-même est manipulé de la façon habituelle).</span><span class="sxs-lookup"><span data-stu-id="61afa-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="61afa-136">Pour les paramètres **\[ out \]** et **\[ in \] , \] out** , ou l’un de leurs composants, d’un type qui contient l’attribut **\[ transmit \_ As \]** , **la** \_ routine **Free \_ inst** est appelée automatiquement pour les objets de données qui ont l’attribut.</span><span class="sxs-lookup"><span data-stu-id="61afa-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="61afa-137">Pour les paramètres **in** , **la** \_ routine **Free \_ inst** est appelée uniquement si l’attribut **\[ transmit \_ As \]** a été appliqué au paramètre.</span><span class="sxs-lookup"><span data-stu-id="61afa-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="61afa-138">Si l’attribut a été appliqué aux composants du paramètre, le **type** \_ **Free \_ inst** routine n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="61afa-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="61afa-139">Il n’y a aucun appel de libération pour les données incorporées et un appel au maximum (lié à l’attribut de niveau supérieur) pour un paramètre **in** only.</span><span class="sxs-lookup"><span data-stu-id="61afa-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="61afa-140">Efficace avec MIDL 2,0, le client et le serveur doivent fournir les quatre fonctions.</span><span class="sxs-lookup"><span data-stu-id="61afa-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="61afa-141">Par exemple, une liste liée peut être transmise sous la forme d’un tableau de taille.</span><span class="sxs-lookup"><span data-stu-id="61afa-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="61afa-142">Le **type \_ à \_** la routine de transmission parcourt la liste liée et copie les données ordonnées dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="61afa-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="61afa-143">Les éléments du tableau sont triés de sorte que les nombreux pointeurs associés à la structure de la liste n’ont pas besoin d’être transmis.</span><span class="sxs-lookup"><span data-stu-id="61afa-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="61afa-144">Le **type \_ de \_** la routine de transmission lit le tableau et place ses éléments dans une structure de liste liée.</span><span class="sxs-lookup"><span data-stu-id="61afa-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="61afa-145">La liste \_ à double liaison (liste de liens doubles \_ ) comprend des données et des pointeurs vers les éléments de la liste précédente et suivante :</span><span class="sxs-lookup"><span data-stu-id="61afa-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="61afa-146">Au lieu d’expédier la structure complexe, l' **\[** attribut [**transmit \_ As**](/windows/desktop/Midl/transmit-as) **\]** peut être utilisé pour l’envoyer sur le réseau sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="61afa-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="61afa-147">La séquence d’éléments dans le tableau conserve l’ordre des éléments dans la liste à un coût inférieur :</span><span class="sxs-lookup"><span data-stu-id="61afa-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="61afa-148">L’attribut **\[ transmit \_ As \]** apparaît dans le fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="61afa-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="61afa-149">Dans l’exemple suivant, **ModifyListProc** définit le paramètre de type double \_ Link \_ comme un paramètre **\[ in, out \]** :</span><span class="sxs-lookup"><span data-stu-id="61afa-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="61afa-150">Les quatre fonctions définies par le programmeur utilisent le nom du type dans les noms de fonction, et utilisent les types présentés et transmis comme types de paramètres, selon les besoins :</span><span class="sxs-lookup"><span data-stu-id="61afa-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 