---
title: wire_marshal (attribut)
description: L’attribut \ Wire \_ Marshal \ spécifie un type de données qui sera utilisé pour la transmission (type de câble) au lieu d’un type de données spécifique à l’application (type utilisateur).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal MIDL de l’attribut
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383116"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="93290-104">\_attribut Wire Marshal</span><span class="sxs-lookup"><span data-stu-id="93290-104">wire\_marshal attribute</span></span>

<span data-ttu-id="93290-105">L’attribut **\[ Wire \_ Marshal \]** spécifie un type de données qui sera utilisé pour la transmission ( *type de câble*) au lieu d’un type de données spécifique à l’application ( *type utilisateur*).</span><span class="sxs-lookup"><span data-stu-id="93290-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="93290-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93290-107">*type de câble*</span><span class="sxs-lookup"><span data-stu-id="93290-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-108">Spécifie le type de données de transfert nommé qui est réellement transféré entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="93290-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="93290-109">Le *type de câble* doit être un type de base MIDL, un type prédéfini ou un identificateur de type d’un type qui peut être transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="93290-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="93290-110">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="93290-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-111">Type pour lequel *User-type* deviendra un alias.</span><span class="sxs-lookup"><span data-stu-id="93290-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="93290-112">*type d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="93290-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-113">Spécifie l’identificateur du type de données utilisateur à marshaler.</span><span class="sxs-lookup"><span data-stu-id="93290-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="93290-114">Il peut s’agir de n’importe quel type, comme indiqué par le *type-specifier*, à condition qu’il ait une taille bien définie.</span><span class="sxs-lookup"><span data-stu-id="93290-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="93290-115">Le *type utilisateur* n’a pas besoin d’être transmissible, mais il doit être un type connu du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="93290-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="93290-116">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="93290-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-117">Spécifie un pointeur vers un champ d’indicateur ( [**unsigned**](unsigned.md) [**long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="93290-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="93290-118">Le mot de poids fort spécifie les indicateurs de représentation des données de rapport de non-remise tels qu’ils sont définis par DCE pour la représentation à virgule flottante, Big-endian et caractère.</span><span class="sxs-lookup"><span data-stu-id="93290-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="93290-119">Le mot de poids faible spécifie un indicateur de contexte de marshaling.</span><span class="sxs-lookup"><span data-stu-id="93290-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="93290-120">La disposition exacte des indicateurs est décrite dans [la fonction type d' \_ utilisateur](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="93290-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="93290-121">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="93290-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-122">Spécifie la taille de la mémoire tampon actuelle (décalage) avant le dimensionnement de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93290-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="93290-123">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="93290-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-124">Spécifie un pointeur vers un objet de *\_ type utilisateur.*</span><span class="sxs-lookup"><span data-stu-id="93290-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="93290-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="93290-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="93290-126">Spécifie le pointeur de la mémoire tampon actuelle.</span><span class="sxs-lookup"><span data-stu-id="93290-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93290-127">Notes</span><span class="sxs-lookup"><span data-stu-id="93290-127">Remarks</span></span>

<span data-ttu-id="93290-128">Chaque type de données spécifique à l’application, *utilisateur-type,* a une correspondance un-à-un avec un *type de câble* qui définit la représentation filaire du type.</span><span class="sxs-lookup"><span data-stu-id="93290-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="93290-129">Vous devez fournir des routines pour dimensionner les données pour le marshaling, pour marshaler et démarshaler les données, ainsi que pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="93290-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="93290-130">Notez que s’il existe des types incorporés dans vos données qui sont également définis avec un **\[ \_ marshaling \] de câble** ou un **\[** [**\_ Marshal d’utilisateur**](user-marshal.md) **\]** , vous devez également gérer la maintenance de ces types incorporés.</span><span class="sxs-lookup"><span data-stu-id="93290-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="93290-131">Pour plus d’informations sur ces routines, consultez [l' \_ attribut Wire Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="93290-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="93290-132">Votre implémentation doit suivre les règles de marshaling en fonction de la spécification OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="93290-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="93290-133">Pour plus d’informations sur la syntaxe de transfert de rapport de non-remise [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) , consultez.</span><span class="sxs-lookup"><span data-stu-id="93290-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="93290-134">Il n’est pas recommandé d’utiliser le **\[ \_ marshaling \] de câble** si vous n’êtes pas familiarisé avec le protocole câble.</span><span class="sxs-lookup"><span data-stu-id="93290-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="93290-135">Le *type de câble* ne peut pas être un pointeur d’interface ou un pointeur complet.</span><span class="sxs-lookup"><span data-stu-id="93290-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="93290-136">Le *type de câble* doit avoir une taille de mémoire bien définie.</span><span class="sxs-lookup"><span data-stu-id="93290-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="93290-137">Pour plus d’informations sur la façon de marshaler un *type de câble* donné, consultez la page [règles de marshaling pour le marshaleur d’utilisateur \_ et le \_ marshaling de réseau](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="93290-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="93290-138">L' *utilisateur-type* ne doit pas être un pointeur d’interface, car ceux-ci peuvent être marshalés directement.</span><span class="sxs-lookup"><span data-stu-id="93290-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="93290-139">Si le type d’utilisateur est un pointeur complet, vous devez gérer vous-même les alias.</span><span class="sxs-lookup"><span data-stu-id="93290-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="93290-140">Vous ne pouvez pas utiliser l’attribut **\[ Wire \_ \] Marshal** avec l' **\[** attribut [**allocate**](allocate.md) **\]** , directement ou indirectement, car le moteur de NDR ne contrôle pas l’allocation de mémoire pour le type transmis.</span><span class="sxs-lookup"><span data-stu-id="93290-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="93290-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="93290-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="93290-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93290-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93290-143">**lui**</span><span class="sxs-lookup"><span data-stu-id="93290-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="93290-144">Représentation des données</span><span class="sxs-lookup"><span data-stu-id="93290-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="93290-145">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="93290-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="93290-146">**long**</span><span class="sxs-lookup"><span data-stu-id="93290-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="93290-147">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="93290-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="93290-148">Attribut de \_ Marshal de câble</span><span class="sxs-lookup"><span data-stu-id="93290-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="93290-149">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="93290-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="93290-150">**non signé**</span><span class="sxs-lookup"><span data-stu-id="93290-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="93290-151">**Marshal d’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="93290-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 