---
title: Attribut represent_as
description: L’attribut \ represent \_ As \ vous permet de spécifier la manière dont un type de données transmissible particulier est représenté à l’application.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Appel de procédure distante RPC, attributs, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102224"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="054c7-105">L' \_ attribut représente en tant que</span><span class="sxs-lookup"><span data-stu-id="054c7-105">The represent\_as Attribute</span></span>

<span data-ttu-id="054c7-106">L' \[ attribut [dereprésente \_ comme](/windows/desktop/Midl/represent-as) \] attribut vous permet de spécifier la manière dont un type de données transmissible particulier est représenté à l’application.</span><span class="sxs-lookup"><span data-stu-id="054c7-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="054c7-107">Pour ce faire, spécifiez le nom du type représenté pour un type transmissible connu et fournissez les routines de conversion.</span><span class="sxs-lookup"><span data-stu-id="054c7-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="054c7-108">Vous devez également fournir les routines pour libérer la mémoire utilisée par les objets de type de données.</span><span class="sxs-lookup"><span data-stu-id="054c7-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="054c7-109">Utilisez l’attribut « **\[ représenter \_ en tant que \]** » pour présenter une application avec un type de données différent, éventuellement non transmissible, plutôt que le type réellement transmis entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="054c7-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="054c7-110">Il est également possible que le type manipulé par l’application ne soit pas connu au moment de la compilation MIDL.</span><span class="sxs-lookup"><span data-stu-id="054c7-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="054c7-111">Lorsque vous choisissez un type transmissible bien défini, vous ne devez pas vous préoccuper de la représentation des données dans l’environnement hétérogène.</span><span class="sxs-lookup"><span data-stu-id="054c7-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="054c7-112">L’attribut « **\[ représenter \_ en tant que \]** » peut améliorer l’efficacité de votre application en réduisant la quantité de données transmises sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="054c7-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="054c7-113">L’attribut **\[ dereprésente \_ \] comme** attribut est semblable à l' \[ attribut [transmit \_ As](/windows/desktop/Midl/transmit-as) \] .</span><span class="sxs-lookup"><span data-stu-id="054c7-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="054c7-114">Toutefois, lors de la **\[ transmission \_ en tant que \]** vous permet de spécifier un type de données qui sera utilisé pour la **\[ \_ \] transmission, representer** en tant que vous permet de spécifier la façon dont un type de données est représenté pour l’application.</span><span class="sxs-lookup"><span data-stu-id="054c7-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="054c7-115">Le type représenté n’a pas besoin d’être défini dans les fichiers traités MIDL ; Il peut être défini au moment où les stubs sont compilés avec le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="054c7-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="054c7-116">Pour ce faire, utilisez la directive include dans le fichier de configuration de l' [application (ACF)](the-application-configuration-file-acf-.md) pour compiler le fichier d’en-tête approprié.</span><span class="sxs-lookup"><span data-stu-id="054c7-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="054c7-117">Par exemple, le ACF suivant définit un type local pour l’application, **\_ type repr**, pour le type transmissible **nommé \_ type :**</span><span class="sxs-lookup"><span data-stu-id="054c7-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="054c7-118">Le tableau suivant décrit les quatre routines fournies par le programmeur.</span><span class="sxs-lookup"><span data-stu-id="054c7-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="054c7-119">Routine</span><span class="sxs-lookup"><span data-stu-id="054c7-119">Routine</span></span>                      | <span data-ttu-id="054c7-120">Description</span><span class="sxs-lookup"><span data-stu-id="054c7-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054c7-121">**\_type nommé \_ à partir de l' \_ local**</span><span class="sxs-lookup"><span data-stu-id="054c7-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="054c7-122">Alloue une instance du type de réseau et convertit le type local en type de réseau.</span><span class="sxs-lookup"><span data-stu-id="054c7-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="054c7-123">**\_type nommé \_ en \_ local**</span><span class="sxs-lookup"><span data-stu-id="054c7-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="054c7-124">Convertit du type de réseau en type local.</span><span class="sxs-lookup"><span data-stu-id="054c7-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="054c7-125">**\_type nommé \_ \_ local libre**</span><span class="sxs-lookup"><span data-stu-id="054c7-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="054c7-126">Libère la mémoire allouée par un appel **au \_ type nommé \_ dans \_** la routine locale, mais pas le type lui-même.</span><span class="sxs-lookup"><span data-stu-id="054c7-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="054c7-127">**\_type nommé \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="054c7-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="054c7-128">Libère le stockage pour le type de réseau (les deux côtés).</span><span class="sxs-lookup"><span data-stu-id="054c7-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="054c7-129">En dehors de ces quatre routines fournies par le programmeur, le type nommé n’est pas manipulé par l’application.</span><span class="sxs-lookup"><span data-stu-id="054c7-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="054c7-130">Le seul type visible pour l’application est le type représenté.</span><span class="sxs-lookup"><span data-stu-id="054c7-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="054c7-131">L’application utilise le nom de type représenté au lieu du nom de type transmis dans les prototypes et les stubs générés par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="054c7-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="054c7-132">Vous devez fournir le jeu de routines pour les deux côtés.</span><span class="sxs-lookup"><span data-stu-id="054c7-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="054c7-133">Pour les objets de **\_ type nommé** temporaires, le stub appelle le **\_ type nommé \_ Free \_ inst** pour libérer toute mémoire allouée par un appel à un **\_ type nommé \_ à partir de \_** l’état local.</span><span class="sxs-lookup"><span data-stu-id="054c7-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="054c7-134">Si le type représenté est un pointeur ou contient un pointeur, le **\_ type nommé \_ à \_** la routine locale doit allouer de la mémoire pour les données auxquelles les pointeurs pointent (l’objet de type représenté lui-même est manipulé de la manière habituelle).</span><span class="sxs-lookup"><span data-stu-id="054c7-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="054c7-135">Pour \[ [les](/windows/desktop/Midl/out-idl) \] paramètres out et \[ [in](/windows/desktop/Midl/in), out \] d’un type qui contiennent une **\[ représentation \_ sous la forme** ou l’un de ses composants, la routine **\_ \_ \_ locale libre de type nommé** est automatiquement appelée pour les objets de données qui contiennent l’attribut.</span><span class="sxs-lookup"><span data-stu-id="054c7-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="054c7-136">Pour les paramètres **\[ in \]** , la routine **\_ \_ \_ locale Free de type nommé** est appelée uniquement si l’attribut **\[ dereprésente \_ comme \]** attribut a été appliqué au paramètre.</span><span class="sxs-lookup"><span data-stu-id="054c7-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="054c7-137">Si l’attribut a été appliqué aux composants du paramètre, la routine *\* \*\*\* \_ Free \_ local*\* n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="054c7-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="054c7-138">Les routines de libération ne sont pas appelées pour les données incorporées et les appels au plus une fois (associés à l’attribut de niveau supérieur) pour un paramètre **\[ in \]** only.</span><span class="sxs-lookup"><span data-stu-id="054c7-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="054c7-139">Il est possible d’appliquer à la fois les attributs **\[ transmit \_ As \]** et **\[ \_ \] DEFAUT au même** type.</span><span class="sxs-lookup"><span data-stu-id="054c7-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="054c7-140">Lors du marshaling des données, la **\[ représentation \_ en tant que \]** conversion de type est appliquée en premier, puis la **\[ transmission \_ comme \]** conversion est appliquée.</span><span class="sxs-lookup"><span data-stu-id="054c7-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="054c7-141">L’ordre est inversé lors de l’annulation du marshaling des données.</span><span class="sxs-lookup"><span data-stu-id="054c7-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="054c7-142">Ainsi, lors du marshaling, \* **\_ à partir de \_ local** alloue une instance d’un type nommé et la convertit d’un objet de type local en objet de type nommé temporaire.</span><span class="sxs-lookup"><span data-stu-id="054c7-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="054c7-143">Cet objet est l’objet de type présenté utilisé pour la \* procédure **\_ de transmission de \_** la routine.</span><span class="sxs-lookup"><span data-stu-id="054c7-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="054c7-144">Le \* **\_ à \_** la place de la routine alloue ensuite un objet de type transmis et le convertit de l’objet (nommé) présenté à l’objet transmis.</span><span class="sxs-lookup"><span data-stu-id="054c7-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="054c7-145">Un tableau d’entiers longs peut être utilisé pour représenter une liste liée.</span><span class="sxs-lookup"><span data-stu-id="054c7-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="054c7-146">De cette façon, l’application manipule la liste et la transmission utilise un tableau d’entiers longs lorsqu’une liste de ce type est transmise.</span><span class="sxs-lookup"><span data-stu-id="054c7-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="054c7-147">Vous pouvez commencer par un tableau, mais l’utilisation d’une construction avec un tableau ouvert d’entiers longs est plus pratique.</span><span class="sxs-lookup"><span data-stu-id="054c7-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="054c7-148">L’exemple suivant vous montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="054c7-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="054c7-149">Notez que les prototypes des routines qui utilisent le type **LONGARR** sont réellement affichés dans les fichiers stub. h en tant **que \_ boîte de PLOC** à la place du type **LONGARR** .</span><span class="sxs-lookup"><span data-stu-id="054c7-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="054c7-150">Il en va de même pour les stubs appropriés dans le \_ fichier c. c du stub.</span><span class="sxs-lookup"><span data-stu-id="054c7-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="054c7-151">Vous devez fournir les quatre fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="054c7-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="054c7-152">Les routines indiquées ci-dessus effectuent les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="054c7-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="054c7-153">Le **LONGARR \_ de \_** la routine locale compte les nœuds de la liste, alloue un objet LONGARR avec la taille **sizeof**(**LONGARR**) + Count \* **sizeof**(**long**), définit le champ **Size** sur Count et copie les données dans le champ **DataArr** .</span><span class="sxs-lookup"><span data-stu-id="054c7-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="054c7-154">La routine **LONGARR \_ à \_ local** crée une liste avec des nœuds de taille et transfère le tableau aux nœuds appropriés.</span><span class="sxs-lookup"><span data-stu-id="054c7-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="054c7-155">La routine **LONGARR \_ Free \_ inst** ne libère rien dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="054c7-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="054c7-156">La **routine \_ \_ locale libre LONGARR** libère tous les nœuds de la liste.</span><span class="sxs-lookup"><span data-stu-id="054c7-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 