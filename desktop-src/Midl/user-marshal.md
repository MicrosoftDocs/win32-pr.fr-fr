---
title: attribut user_marshal
description: L' \_ attribut ACF de Marshal d’utilisateur associe un type local nommé dans le langage cible (type utilisateur) à un type de transfert (type filaire) qui est transféré entre le client et le serveur.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal MIDL de l’attribut
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314796"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="b7dc6-104">\_attribut de Marshal utilisateur</span><span class="sxs-lookup"><span data-stu-id="b7dc6-104">user\_marshal attribute</span></span>

<span data-ttu-id="b7dc6-105">L’attribut ACF de **\_ Marshal d’utilisateur** associe un type local nommé dans le langage cible (*type utilisateur*) à un type de transfert (*type filaire*) qui est transféré entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="b7dc6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7dc6-107">*type d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-108">Spécifie l’identificateur du type de données utilisateur à marshaler.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="b7dc6-109">Le *type utilisateur* n’a pas besoin d’être transmissible et n’a pas besoin d’être un type connu du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b7dc6-110">*type de câble*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-111">Spécifie le type de données de transfert nommé qui est réellement transféré entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="b7dc6-112">Le type de câble doit être un type de base MIDL, un type prédéfini ou un identificateur de type d’un type qui peut être transmis sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="b7dc6-113">*pFlags*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-114">Spécifie un pointeur vers un champ d’indicateur ( [**unsigned**](unsigned.md) [**long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="b7dc6-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="b7dc6-115">Le mot de poids fort spécifie les indicateurs de représentation des données de rapport de non-remise tels qu’ils sont définis par DCE pour la représentation à virgule flottante, Big-endian et caractère.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="b7dc6-116">Le mot de poids faible spécifie un indicateur de contexte de marshaling.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="b7dc6-117">La disposition exacte des indicateurs est décrite dans [la fonction type d' \_ utilisateur](/windows/desktop/Rpc/the-type-usersize-function).</span><span class="sxs-lookup"><span data-stu-id="b7dc6-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="b7dc6-118">*StartingSize*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-119">Spécifie la taille de la mémoire tampon actuelle (décalage) avant le dimensionnement de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="b7dc6-120">*pUser \_ typeObject*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-121">Spécifie un pointeur vers un objet de *\_ type utilisateur*.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="b7dc6-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="b7dc6-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b7dc6-123">Spécifie le pointeur de la mémoire tampon actuelle.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7dc6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b7dc6-124">Remarks</span></span>

<span data-ttu-id="b7dc6-125">Chaque type local nommé, *utilisateur-type*, a une correspondance un-à-un avec un *type de câble* qui définit la représentation filaire du type.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="b7dc6-126">Vous devez fournir des routines pour dimensionner les données pour le marshaling, pour marshaler et démarshaler les données, ainsi que pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="b7dc6-127">Pour plus d’informations sur ces routines, consultez [l' \_ attribut User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="b7dc6-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="b7dc6-128">Notez que s’il existe des types incorporés dans vos données qui sont également définis avec le **\_ Marshal utilisateur** ou \[ le [**\[ \_ Marshal \] de câble**](wire-marshal.md), vous devez également gérer la maintenance de ces types incorporés.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="b7dc6-129">Le *type de câble* ne peut pas être un pointeur d’interface ou un pointeur complet.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="b7dc6-130">Le *type de câble* doit avoir une taille de mémoire bien définie.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="b7dc6-131">Pour plus d’informations sur la façon de marshaler un *type de câble* donné, consultez la page [règles de marshaling pour le marshaleur d’utilisateur \_ et le \_ marshaling de réseau](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="b7dc6-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="b7dc6-132">Le *type utilisateur* ne doit pas être un pointeur d’interface, car ceux-ci peuvent être marshalés directement.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="b7dc6-133">Si le type d’utilisateur est un pointeur complet, vous devez gérer vous-même les alias.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="b7dc6-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7dc6-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="b7dc6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7dc6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dc6-136">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="b7dc6-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-137">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="b7dc6-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-138">**long**</span><span class="sxs-lookup"><span data-stu-id="b7dc6-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-139">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="b7dc6-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-140">**non signé**</span><span class="sxs-lookup"><span data-stu-id="b7dc6-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-141">Attribut de \_ Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b7dc6-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="b7dc6-142">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="b7dc6-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="b7dc6-143">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="b7dc6-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 