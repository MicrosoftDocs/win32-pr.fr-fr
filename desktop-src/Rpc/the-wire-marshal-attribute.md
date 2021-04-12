---
title: Attribut wire_marshal
description: L’attribut \ Wire \_ Marshal \ est un attribut de type IDL similaire à la syntaxe à envoyer \_ en tant que \, mais offrant un moyen plus efficace de marshaler les données sur un réseau.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Appel de procédure distante RPC, attributs, wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382351"
---
# <a name="the-wire_marshal-attribute"></a><span data-ttu-id="7ca61-105">Attribut de \_ Marshal de câble</span><span class="sxs-lookup"><span data-stu-id="7ca61-105">The wire\_marshal Attribute</span></span>

<span data-ttu-id="7ca61-106">L' \[ attribut [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] est un attribut de type IDL similaire à la syntaxe à \[ [transmettre \_ en tant que](/windows/desktop/Midl/transmit-as) \] , mais il offre un moyen plus efficace de marshaler les données sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="7ca61-106">The \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] attribute is an IDL-type attribute similar in syntax to \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\], but providing a more efficient way to marshal data across a network.</span></span>

<span data-ttu-id="7ca61-107">Vous utilisez l' \[ attribut **Wire \_ Marshal** \] pour spécifier un type de données qui sera transmis à la place du type de données spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="7ca61-107">You use the \[**wire\_marshal**\] attribute to specify a data type that will be transmitted in place of the application-specific data type.</span></span> <span data-ttu-id="7ca61-108">Chaque type spécifique à l’application a un type pouvant être transmis correspondant qui définit la représentation filaire (la représentation utilisée sur le réseau). Le type spécifique à l’application n’a pas besoin d’être transmissible, mais il doit être un type reconnu par MIDL.</span><span class="sxs-lookup"><span data-stu-id="7ca61-108">Each application-specific type has a corresponding transmittable type that defines the wire representation (the representation used on the network).The application-specific type need not be transmittable, but it must be a type that MIDL recognizes.</span></span> <span data-ttu-id="7ca61-109">Pour marshaler un type inconnu en MIDL, utilisez le \[ [ \_ Marshal d’utilisateur](/windows/desktop/Midl/user-marshal)d’attribut ACF \] .</span><span class="sxs-lookup"><span data-stu-id="7ca61-109">To marshal a type unknown to MIDL, use the ACF attribute \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\].</span></span>

<span data-ttu-id="7ca61-110">Votre type spécifique à votre application peut être un type simple, composite ou pointeur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="7ca61-111">La restriction principale est que l’instance de type doit avoir une taille de mémoire fixe et bien définie.</span><span class="sxs-lookup"><span data-stu-id="7ca61-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="7ca61-112">Si la taille de votre instance de type doit être modifiée, utilisez un champ de pointeur plutôt qu’un tableau conforme.</span><span class="sxs-lookup"><span data-stu-id="7ca61-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="7ca61-113">Vous pouvez également définir un pointeur vers le type modifiable.</span><span class="sxs-lookup"><span data-stu-id="7ca61-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="7ca61-114">Vous devez fournir les routines pour le dimensionnement, le marshaling et le démarshaling des données, ainsi que la libération de la mémoire associée.</span><span class="sxs-lookup"><span data-stu-id="7ca61-114">You must supply the routines for sizing, marshaling, and unmarshaling the data as well as freeing the associated memory.</span></span> <span data-ttu-id="7ca61-115">Le tableau suivant décrit les quatre noms de routines fournis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="7ca61-116"><type>Est le type utilisateur spécifié dans la définition de type de \[ **\_ Marshal de câble** \] .</span><span class="sxs-lookup"><span data-stu-id="7ca61-116">The <type> is the userm-type specified in the \[**wire\_marshal**\] type definition.</span></span>



| <span data-ttu-id="7ca61-117">Routine</span><span class="sxs-lookup"><span data-stu-id="7ca61-117">Routine</span></span>                                                            | <span data-ttu-id="7ca61-118">Description</span><span class="sxs-lookup"><span data-stu-id="7ca61-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="7ca61-119"><type>\_Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7ca61-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="7ca61-120">Dimensionne la mémoire tampon de données RPC avant le marshaling côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="7ca61-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="7ca61-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="7ca61-122">Marshale les données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="7ca61-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="7ca61-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="7ca61-124">Démarshale les données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="7ca61-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="7ca61-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="7ca61-126">Libère les données côté serveur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="7ca61-127">Ces routines fournies par le programmeur sont fournies par le client ou l’application serveur en fonction des attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="7ca61-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span>

<span data-ttu-id="7ca61-128">Si le paramètre est \[ uniquement [dans](/windows/desktop/Midl/in) \] , le client transmet au serveur.</span><span class="sxs-lookup"><span data-stu-id="7ca61-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="7ca61-129">Le client a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="7ca61-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="7ca61-130">Le serveur a besoin des fonctions **<type> \_ UserUnmarshal** et **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="7ca61-130">The server needs the **<type>\_UserUnmarshal**, and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="7ca61-131">Pour un \[ paramètre en [sortie](/windows/desktop/Midl/out-idl) \] seule, le serveur transmet au client.</span><span class="sxs-lookup"><span data-stu-id="7ca61-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="7ca61-132">Le serveur a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** , tandis que le client a besoin de la fonction **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="7ca61-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ca61-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ca61-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca61-134">Attribut de \_ Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7ca61-134">The user\_marshal Attribute</span></span>](the-user-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="7ca61-135">Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="7ca61-135">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="7ca61-136">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="7ca61-136">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="7ca61-137">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="7ca61-137">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="7ca61-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="7ca61-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 