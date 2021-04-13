---
title: attribut de canal
description: Le constructeur de type pipe permet de transmettre un flux ouvert de données typées à travers un appel de procédure distante.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- MIDL (MIDL), attribut de canal
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314760"
---
# <a name="pipe-attribute"></a><span data-ttu-id="7084d-104">attribut de canal</span><span class="sxs-lookup"><span data-stu-id="7084d-104">pipe attribute</span></span>

<span data-ttu-id="7084d-105">Le constructeur de type **pipe** permet de transmettre un flux ouvert de données typées à travers un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="7084d-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="7084d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7084d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7084d-107">*type d’élément*</span><span class="sxs-lookup"><span data-stu-id="7084d-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7084d-108">Définit la taille d’un élément unique dans la mémoire tampon de transfert.</span><span class="sxs-lookup"><span data-stu-id="7084d-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="7084d-109">Le type d' *élément* peut être un [type de base](midl-base-types.md), un type prédéfini \_ , un [**struct**](struct.md), une [**énumération 32b**](v1-enum.md)ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="7084d-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="7084d-110">Plusieurs restrictions s’appliquent aux *\_ types d’éléments*, comme décrit dans la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7084d-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="7084d-111">*canal-déclarateur*</span><span class="sxs-lookup"><span data-stu-id="7084d-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="7084d-112">Spécifie un ou plusieurs identificateurs ou pointeurs vers des identificateurs.</span><span class="sxs-lookup"><span data-stu-id="7084d-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="7084d-113">Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7084d-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7084d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7084d-114">Remarks</span></span>

<span data-ttu-id="7084d-115">Vous pouvez utiliser le constructeur de type **pipe** pour transmettre des données dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="7084d-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="7084d-116">Un **\[** [](in.md) **\]** paramètre in pipe permet au serveur d’extraire le flux de données du client pendant un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="7084d-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="7084d-117">Un **\[** paramètre de [**sortie**](out-idl.md) de **\]** canal permet au serveur d’envoyer à nouveau le flux de données au client.</span><span class="sxs-lookup"><span data-stu-id="7084d-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="7084d-118">Vous fournissez les routines côté client pour l’envoi et l’extraction du flux de données et pour allouer une mémoire tampon globale pour les données.</span><span class="sxs-lookup"><span data-stu-id="7084d-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="7084d-119">Les routines de stub client et serveur marshalent et démarshalent les données et transmettent une référence à la mémoire tampon à l’application.</span><span class="sxs-lookup"><span data-stu-id="7084d-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="7084d-120">Les restrictions suivantes s’appliquent aux canaux :</span><span class="sxs-lookup"><span data-stu-id="7084d-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="7084d-121">Un élément pipe ne peut pas être ou contenir un pointeur, un tableau conforme ou variable, un handle ou un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="7084d-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="7084d-122">En outre, dans l’implémentation Microsoft des canaux, un élément pipe ne peut pas être ou contenir une [**Union**](union.md), une [**énumération 16B**](enum.md)ou un [**\_ \_ int3264**](--int3264.md).</span><span class="sxs-lookup"><span data-stu-id="7084d-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="7084d-123">Vous ne pouvez pas appliquer les **\[** attributs de [**transmission \_ en tant que**](transmit-as.md) **\]** , de marshaling en tant que, **\[** [**\_**](represent-as.md) **\]** **\[** de [**\_ marshaling de câble**](wire-marshal.md)ou de **\]** **\[** [**\_ Marshal utilisateur**](user-marshal.md) **\]** à un type de canal ou au *type d’élément*.</span><span class="sxs-lookup"><span data-stu-id="7084d-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="7084d-124">Un type de canal ne peut pas être un membre d’une structure ou d’une Union, la cible d’un pointeur ou le type de base d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="7084d-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="7084d-125">Un type de données déclaré comme étant un type de canal ne peut être utilisé qu’en tant que paramètre d’un appel distant.</span><span class="sxs-lookup"><span data-stu-id="7084d-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="7084d-126">Vous pouvez passer un paramètre de canal dans l’une ou l’autre direction par valeur ou par référence ( **\[** pointeur [**ref**](ref.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="7084d-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="7084d-127">Toutefois, vous ne pouvez pas appliquer l' **\[** [](ptr.md) **\]** attribut PTR à un canal qui est passé par référence.</span><span class="sxs-lookup"><span data-stu-id="7084d-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="7084d-128">Vous ne pouvez pas spécifier un paramètre de canal avec un **\[** [](unique.md) **\]** pointeur unique ou complet, quelle que soit la direction.</span><span class="sxs-lookup"><span data-stu-id="7084d-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="7084d-129">Vous ne pouvez pas utiliser de canaux dans des interfaces d' **\[** [**objet**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7084d-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="7084d-130">Vous ne pouvez pas appliquer l' **\[** [](idempotent.md) **\]** attribut idempotent à une routine qui a un paramètre pipe.</span><span class="sxs-lookup"><span data-stu-id="7084d-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="7084d-131">Vous ne pouvez pas utiliser les attributs de sérialisation, **\[** [**Encoder**](encode.md) **\]** et **\[** [**décoder**](decode.md) **\]** avec des canaux.</span><span class="sxs-lookup"><span data-stu-id="7084d-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="7084d-132">Vous ne pouvez pas utiliser de handles automatiques, par défaut, ou avec l’attribut de **\[** [**\_ gestion automatique**](auto-handle.md) **\]** , avec des canaux.</span><span class="sxs-lookup"><span data-stu-id="7084d-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="7084d-133">Le compilateur MIDL prend en charge les canaux en mode [**/OIF**](-oi.md) uniquement.</span><span class="sxs-lookup"><span data-stu-id="7084d-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="7084d-134">Pour plus d’informations sur l’implémentation des routines avec des paramètres de canal, consultez [canaux](/windows/desktop/Rpc/pipes) dans le Guide du programmeur RPC et référence.</span><span class="sxs-lookup"><span data-stu-id="7084d-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="7084d-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="7084d-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="7084d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7084d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7084d-137">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="7084d-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="7084d-138">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="7084d-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7084d-139">**décoder**</span><span class="sxs-lookup"><span data-stu-id="7084d-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="7084d-140">**contraire**</span><span class="sxs-lookup"><span data-stu-id="7084d-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="7084d-141">**variables**</span><span class="sxs-lookup"><span data-stu-id="7084d-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="7084d-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="7084d-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="7084d-143">**in**</span><span class="sxs-lookup"><span data-stu-id="7084d-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="7084d-144">**object**</span><span class="sxs-lookup"><span data-stu-id="7084d-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="7084d-145">**à**</span><span class="sxs-lookup"><span data-stu-id="7084d-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="7084d-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="7084d-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7084d-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="7084d-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="7084d-148">**représenter \_ comme**</span><span class="sxs-lookup"><span data-stu-id="7084d-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="7084d-149">**modélis**</span><span class="sxs-lookup"><span data-stu-id="7084d-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="7084d-150">**transmettre \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="7084d-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="7084d-151">**unique**</span><span class="sxs-lookup"><span data-stu-id="7084d-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="7084d-152">**Marshal d’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="7084d-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="7084d-153">**Marshal de câble \_**</span><span class="sxs-lookup"><span data-stu-id="7084d-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 