---
title: attribut represent_as
description: L’attribut \ \_ Renamed as \ ACF associe un type local nommé dans le repr de langage cible à un type de transfert nommé-type qui est transféré entre le client et le serveur.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104029970"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="812b5-104">représenter \_ en tant qu’attribut</span><span class="sxs-lookup"><span data-stu-id="812b5-104">represent\_as attribute</span></span>

<span data-ttu-id="812b5-105">L’attribut **\[ dereprésente \_ As \]** ACF associe un type local nommé dans le *repr* de langage cible à un type de transfert *nommé-type* qui est transféré entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="812b5-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="812b5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="812b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812b5-107">*type nommé*</span><span class="sxs-lookup"><span data-stu-id="812b5-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="812b5-108">Spécifie le type de données de transfert nommé qui est transféré entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="812b5-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="812b5-109">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="812b5-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="812b5-110">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="812b5-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="812b5-111">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="812b5-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="812b5-112">*repr-type*</span><span class="sxs-lookup"><span data-stu-id="812b5-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="812b5-113">Spécifie le type local représenté dans la langue cible présentée aux applications clientes et serveur.</span><span class="sxs-lookup"><span data-stu-id="812b5-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="812b5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="812b5-114">Remarks</span></span>

<span data-ttu-id="812b5-115">Lors de l’utilisation de l’objet **\[ représenter \_ en tant que \]**, vous devez fournir des routines qui effectuent une conversion entre les types local et de transfert et qui libèrent de la mémoire utilisée pour stocker les données converties.</span><span class="sxs-lookup"><span data-stu-id="812b5-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="812b5-116">L’attribut **\[ dereprésente \_ en tant que \]** indique aux stubs d’appeler les routines de conversion fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="812b5-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="812b5-117">Le type transféré *nommé-type* doit correspondre à un type de base MIDL, à un type prédéfini ou à un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="812b5-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="812b5-118">Pour plus d’informations, consultez [types de base MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="812b5-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="812b5-119">Vous devez fournir les routines suivantes :</span><span class="sxs-lookup"><span data-stu-id="812b5-119">You must supply the following routines:</span></span>



| <span data-ttu-id="812b5-120">Nom de la routine</span><span class="sxs-lookup"><span data-stu-id="812b5-120">Routine name</span></span>                   | <span data-ttu-id="812b5-121">Description</span><span class="sxs-lookup"><span data-stu-id="812b5-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="812b5-122">*\_type nommé \* \* \* \_ à partir de l' \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="812b5-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="812b5-123">Convertit les données du type local en type de réseau.</span><span class="sxs-lookup"><span data-stu-id="812b5-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="812b5-124">La routine alloue de la mémoire pour le type de données réseau, y compris la mémoire pour toutes les données référencées par des pointeurs dans le type de données réseau.</span><span class="sxs-lookup"><span data-stu-id="812b5-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="812b5-125">*\_type nommé \* \* \* \_ vers \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="812b5-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="812b5-126">Convertit les données du type de réseau en type local.</span><span class="sxs-lookup"><span data-stu-id="812b5-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="812b5-127">La routine est chargée d’allouer de la mémoire pour les données référencées par des pointeurs dans le type local.</span><span class="sxs-lookup"><span data-stu-id="812b5-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="812b5-128">RPC alloue de la mémoire pour le type local lui-même.</span><span class="sxs-lookup"><span data-stu-id="812b5-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="812b5-129">*\_type nommé \* \* \* \_ libre \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="812b5-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="812b5-130">Libère la mémoire allouée pour les données référencées par des pointeurs dans le type local.</span><span class="sxs-lookup"><span data-stu-id="812b5-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="812b5-131">RPC libère de la mémoire pour le type lui-même</span><span class="sxs-lookup"><span data-stu-id="812b5-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="812b5-132">*\_type nommé \* \* \* \_ gratuit \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="812b5-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="812b5-133">Libère de la mémoire allouée pour les données référencées par des pointeurs dans le type de réseau et pour le type de réseau lui-même.</span><span class="sxs-lookup"><span data-stu-id="812b5-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="812b5-134">Le stub client appelle le *type nommé \* \* \* \_ à partir de \_ local*\* pour allouer de l’espace pour le type transmis et pour convertir les données du type local en type de réseau.</span><span class="sxs-lookup"><span data-stu-id="812b5-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="812b5-135">Le stub serveur alloue de l’espace pour le type de données d’origine et appelle le type *nommé \* \* \* \_ à \_ local*\* pour convertir les données du type de réseau en type local.</span><span class="sxs-lookup"><span data-stu-id="812b5-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="812b5-136">Lors du retour du code d’application, les stubs client et serveur appellent le *type \* \* \* \_ Free \_ inst*\* pour libérer le stockage pour le type de réseau.</span><span class="sxs-lookup"><span data-stu-id="812b5-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="812b5-137">Le stub client appelle le *type nommé \* \* \* \_ Free \_ local*\* pour libérer le stockage retourné par la routine.</span><span class="sxs-lookup"><span data-stu-id="812b5-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="812b5-138">Les types suivants ne peuvent pas avoir un attribut **\[ dereprésente \_ comme \]** attribut :</span><span class="sxs-lookup"><span data-stu-id="812b5-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="812b5-139">Tableaux à variation variable conformes, variables ou conformes</span><span class="sxs-lookup"><span data-stu-id="812b5-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="812b5-140">Structures dans lesquelles le dernier membre est un tableau conforme (structure conforme)</span><span class="sxs-lookup"><span data-stu-id="812b5-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="812b5-141">Pointeurs ou types qui contiennent un pointeur</span><span class="sxs-lookup"><span data-stu-id="812b5-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="812b5-142">Canaux ou types qui contiennent des canaux</span><span class="sxs-lookup"><span data-stu-id="812b5-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="812b5-143">Types utilisés comme type de base pour un canal</span><span class="sxs-lookup"><span data-stu-id="812b5-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="812b5-144">Les types prédéfinis [**gèrent \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="812b5-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="812b5-145">Types qui ont l’attribut [**\[ handle \]**](handle.md)</span><span class="sxs-lookup"><span data-stu-id="812b5-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="812b5-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="812b5-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="812b5-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="812b5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812b5-148">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="812b5-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="812b5-149">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="812b5-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="812b5-150">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="812b5-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="812b5-151">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="812b5-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="812b5-152">**typedef**</span><span class="sxs-lookup"><span data-stu-id="812b5-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="812b5-153">**void**</span><span class="sxs-lookup"><span data-stu-id="812b5-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




