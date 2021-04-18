---
title: Attribut user_marshal
description: L’attribut \ user \_ Marshal \ est un attribut de type ACF similaire à la syntaxe pour que \ représente \_ comme \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Appel de procédure distante RPC, attributs, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bb3237b2d5df001dc94ede5fb03de72b5563eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463490"
---
# <a name="the-user_marshal-attribute"></a><span data-ttu-id="d8657-105">Attribut de \_ Marshal d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d8657-105">The user\_marshal Attribute</span></span>

<span data-ttu-id="d8657-106">L' \[ attribut [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] est un attribut de type ACF similaire à la syntaxe à \[ [représenter \_ comme](/windows/desktop/Midl/represent-as) \] .</span><span class="sxs-lookup"><span data-stu-id="d8657-106">The \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attribute is an ACF-type attribute similar in syntax to \[ [represent\_as](/windows/desktop/Midl/represent-as)\].</span></span> <span data-ttu-id="d8657-107">Comme avec l’attribut IDL, le \[ [ \_ Marshal de câble](/windows/desktop/Midl/wire-marshal) \] , il offre un moyen plus efficace de marshaler les données sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="d8657-107">As with the IDL attribute, \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\], it offers a more efficient way to marshal data across a network.</span></span> <span data-ttu-id="d8657-108">En tant qu’attribut ACF, le **\[ \_ Marshal \] d’utilisateur** vous permet de marshaler des types de données personnalisés qui sont inconnus de MIDL.</span><span class="sxs-lookup"><span data-stu-id="d8657-108">As an ACF attribute, **\[user\_marshal\]** lets you marshal custom data types that are unknown to MIDL.</span></span> <span data-ttu-id="d8657-109">Chaque type spécifique à l’application a un type pouvant être transmis correspondant qui définit la représentation filaire.</span><span class="sxs-lookup"><span data-stu-id="d8657-109">Each application-specific type has a corresponding transmittable type that defines the wire representation.</span></span>

<span data-ttu-id="d8657-110">Votre type spécifique à votre application peut être un type simple, composite ou pointeur.</span><span class="sxs-lookup"><span data-stu-id="d8657-110">Your application-specific type can be a simple, composite, or pointer type.</span></span> <span data-ttu-id="d8657-111">La restriction principale est que l’instance de type doit avoir une taille de mémoire fixe et bien définie.</span><span class="sxs-lookup"><span data-stu-id="d8657-111">The main restriction is that the type instance must have a fixed, well-defined memory size.</span></span> <span data-ttu-id="d8657-112">Si la taille de votre instance de type doit être modifiée, utilisez un champ de pointeur plutôt qu’un tableau conforme.</span><span class="sxs-lookup"><span data-stu-id="d8657-112">If the size of your type instance needs to change, use a pointer field rather than a conformant array.</span></span> <span data-ttu-id="d8657-113">Vous pouvez également définir un pointeur vers le type modifiable.</span><span class="sxs-lookup"><span data-stu-id="d8657-113">Alternatively, you can define a pointer to the changeable type.</span></span>

<span data-ttu-id="d8657-114">Comme avec l’attribut **\[ Wire \_ Marshal \]** , vous fournissez des routines pour le dimensionnement, le marshaling, le démarshaling et les passes de libération.</span><span class="sxs-lookup"><span data-stu-id="d8657-114">As with the **\[wire\_marshal\]** attribute, you supply routines for the sizing, marshaling, unmarshaling, and freeing passes.</span></span> <span data-ttu-id="d8657-115">Le tableau suivant décrit les quatre noms de routines fournis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8657-115">The following table describes the four user-supplied routine names.</span></span> <span data-ttu-id="d8657-116"><type>Est le *type* utilisateur spécifié dans la définition de type de **\[ \_ Marshal \] utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="d8657-116">The <type> is the userm-*type* specified in the **\[user\_marshal\]** type definition.</span></span>



| <span data-ttu-id="d8657-117">Routine</span><span class="sxs-lookup"><span data-stu-id="d8657-117">Routine</span></span>                                                            | <span data-ttu-id="d8657-118">Description</span><span class="sxs-lookup"><span data-stu-id="d8657-118">Description</span></span>                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="d8657-119"><type>\_Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d8657-119"><type>\_UserSize</span></span>](the-type-usersize-function.md)           | <span data-ttu-id="d8657-120">Dimensionne la mémoire tampon de données RPC avant le marshaling côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d8657-120">Sizes the RPC data buffer before marshaling on the client or server side.</span></span> |
| [<span data-ttu-id="d8657-121"><type>\_UserMarshal</span><span class="sxs-lookup"><span data-stu-id="d8657-121"><type>\_UserMarshal</span></span>](the-type-usermarshal-function.md)     | <span data-ttu-id="d8657-122">Marshale les données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d8657-122">Marshals the data on the client or server side.</span></span>                           |
| [<span data-ttu-id="d8657-123"><type>\_UserUnmarshal</span><span class="sxs-lookup"><span data-stu-id="d8657-123"><type>\_UserUnmarshal</span></span>](the-type-userunmarshal-function.md) | <span data-ttu-id="d8657-124">Démarshale les données côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d8657-124">Unmarshals the data on the client or server side.</span></span>                         |
| [<span data-ttu-id="d8657-125"><type>\_UserFree</span><span class="sxs-lookup"><span data-stu-id="d8657-125"><type>\_UserFree</span></span>](the-type-userfree-function.md)           | <span data-ttu-id="d8657-126">Libère les données côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d8657-126">Frees the data on the server side.</span></span>                                        |



 

<span data-ttu-id="d8657-127">Ces routines fournies par l’utilisateur sont fournies par le client ou l’application serveur, en fonction des attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="d8657-127">These user-supplied routines are provided by either the client or the server application, based on the directional attributes.</span></span>

<span data-ttu-id="d8657-128">Si le paramètre est \[ uniquement [dans](/windows/desktop/Midl/in) \] , le client transmet au serveur.</span><span class="sxs-lookup"><span data-stu-id="d8657-128">If the parameter is \[ [in](/windows/desktop/Midl/in)\] only, the client transmits to the server.</span></span> <span data-ttu-id="d8657-129">Le client a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="d8657-129">The client needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions.</span></span> <span data-ttu-id="d8657-130">Le serveur a besoin des fonctions **<type> \_ UserUnmarshal** et **<type> \_ UserFree** .</span><span class="sxs-lookup"><span data-stu-id="d8657-130">The server needs the **<type>\_UserUnmarshal** and **<type>\_UserFree** functions.</span></span>

<span data-ttu-id="d8657-131">Pour un \[ paramètre en [sortie](/windows/desktop/Midl/out-idl) \] seule, le serveur transmet au client.</span><span class="sxs-lookup"><span data-stu-id="d8657-131">For an \[ [out](/windows/desktop/Midl/out-idl)\]-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="d8657-132">Le serveur a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** , tandis que le client a besoin de la fonction **<type> \_ UserMarshal** .</span><span class="sxs-lookup"><span data-stu-id="d8657-132">The server needs the **<type>\_UserSize** and **<type>\_UserMarshal** functions, while the client needs the **<type>\_UserMarshal** function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8657-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d8657-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8657-134">Attribut de \_ Marshal de câble</span><span class="sxs-lookup"><span data-stu-id="d8657-134">The wire\_marshal Attribute</span></span>](the-wire-marshal-attribute.md)
</dt> <dt>

[<span data-ttu-id="d8657-135">Règles de marshaling pour le marshaling d’utilisateur et le \_ marshaling de câble</span><span class="sxs-lookup"><span data-stu-id="d8657-135">Marshaling Rules for user marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="d8657-136">Marshal d’utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="d8657-136">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="d8657-137">Marshal de câble \_</span><span class="sxs-lookup"><span data-stu-id="d8657-137">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="d8657-138">**NdrGetUserMarshalInfo**</span><span class="sxs-lookup"><span data-stu-id="d8657-138">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 