---
title: Attributs de type
description: Les attributs de type appel de procédure distante (RPC) et MIDL qui peuvent être appliqués aux déclarations de type.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842321"
---
# <a name="type-attributes"></a><span data-ttu-id="8a8c0-103">Attributs de type</span><span class="sxs-lookup"><span data-stu-id="8a8c0-103">Type Attributes</span></span>

<span data-ttu-id="8a8c0-104">Les attributs de type sont les attributs MIDL qui peuvent être appliqués aux déclarations de type :</span><span class="sxs-lookup"><span data-stu-id="8a8c0-104">Type attributes are the MIDL attributes that can be applied to type declarations:</span></span>

-   <span data-ttu-id="8a8c0-105">**\[**[**traitée**](/windows/desktop/Midl/handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="8a8c0-105">**\[**[**handle**](/windows/desktop/Midl/handle)**\]**</span></span>
-   <span data-ttu-id="8a8c0-106">**\[**[**handle de contexte \_**](/windows/desktop/Midl/context-handle)**\]**</span><span class="sxs-lookup"><span data-stu-id="8a8c0-106">**\[**[**context\_handle**](/windows/desktop/Midl/context-handle)**\]**</span></span>
-   <span data-ttu-id="8a8c0-107">**\[**[**type de commutateur \_**](/windows/desktop/Midl/switch-type)**\]**</span><span class="sxs-lookup"><span data-stu-id="8a8c0-107">**\[**[**switch\_type**](/windows/desktop/Midl/switch-type)**\]**</span></span>
-   [<span data-ttu-id="8a8c0-108">attributs de type pointeur</span><span class="sxs-lookup"><span data-stu-id="8a8c0-108">pointer type attributes</span></span>](three-pointer-types.md)

<span data-ttu-id="8a8c0-109">L’attribut **\[ \_ type \] de commutateur** désigne le type d’un discriminateur d’Union.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-109">The **\[switch\_type\]** attribute designates the type of a union discriminator.</span></span> <span data-ttu-id="8a8c0-110">Cet attribut s’applique uniquement à une Union qui n’est pas encapsulée.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-110">This attribute applies only to a nonencapsulated union.</span></span>

<span data-ttu-id="8a8c0-111">Un handle de contexte est un pointeur avec un attribut de **\[ \_ handle \] de contexte** .</span><span class="sxs-lookup"><span data-stu-id="8a8c0-111">A context handle is a pointer with a **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="8a8c0-112">L’attribut **\[ \_ handle \] de contexte** vous permet d’écrire des procédures qui maintiennent les informations d’État entre les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-112">The **\[context\_handle\]** attribute allows you to write procedures that maintain state information between remote procedure calls.</span></span> <span data-ttu-id="8a8c0-113">Un descripteur de contexte avec une valeur non null représente un contexte enregistré et remplit deux fonctions :</span><span class="sxs-lookup"><span data-stu-id="8a8c0-113">A context handle with a non-null value represents saved context and serves two purposes:</span></span>

-   <span data-ttu-id="8a8c0-114">Côté client, il contient les informations nécessaires à la bibliothèque Runtime RPC pour diriger l’appel au serveur.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-114">On the client side, it contains the information needed by the RPC run-time library to direct the call to the server.</span></span>
-   <span data-ttu-id="8a8c0-115">Côté serveur, il sert de descripteur sur le contexte actif.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-115">On the server side, it serves as a handle on active context.</span></span>

<span data-ttu-id="8a8c0-116">L' **\[** [](/windows/desktop/Midl/handle) **\]** attribut handle spécifie qu’un type peut se produire comme handle défini par l’utilisateur (Générique).</span><span class="sxs-lookup"><span data-stu-id="8a8c0-116">The **\[**[**handle**](/windows/desktop/Midl/handle)**\]** attribute specifies that a type can occur as a user-defined (generic) handle.</span></span> <span data-ttu-id="8a8c0-117">Cette fonctionnalité permet de concevoir des handles significatifs pour l’application.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-117">This feature permits the design of handles that are meaningful to the application.</span></span> <span data-ttu-id="8a8c0-118">L’utilisateur doit fournir des routines de liaison et d’annulation de liaison pour effectuer une conversion entre le type de handle défini par l’utilisateur et le type de handle de primitive RPC, **handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-118">The user must provide binding and unbinding routines to convert between the user-defined handle type and the RPC primitive handle type, **handle\_t**.</span></span> <span data-ttu-id="8a8c0-119">Un handle primitif contient des informations de destination significatives pour les bibliothèques Runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-119">A primitive handle contains destination information meaningful to the RPC run-time libraries.</span></span> <span data-ttu-id="8a8c0-120">Un descripteur défini par l’utilisateur ne peut être défini que dans une déclaration de type, et non dans une déclaration de fonction.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-120">A user-defined handle can only be defined in a type declaration, not in a function declaration.</span></span> <span data-ttu-id="8a8c0-121">Un paramètre avec l’attribut **\[ descripteur \]** a un double objectif.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-121">A parameter with the **\[handle\]** attribute has a double purpose.</span></span> <span data-ttu-id="8a8c0-122">Elle est utilisée pour déterminer la liaison pour l’appel et elle est transmise à la procédure appelée en tant que paramètre de données normal.</span><span class="sxs-lookup"><span data-stu-id="8a8c0-122">It is used to determine the binding for the call, and it is transmitted to the called procedure as a normal data parameter.</span></span>

 

 