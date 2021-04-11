---
title: Attributs de pointeur appliqués au paramètre
description: Chaque attribut de pointeur (\ Ref \, \ unique \ et \ PTR \) a des caractéristiques qui affectent l’allocation de mémoire. Le tableau suivant récapitule ces caractéristiques.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031687"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="b8ff7-104">Attributs de pointeur appliqués au paramètre</span><span class="sxs-lookup"><span data-stu-id="b8ff7-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="b8ff7-105">Chaque attribut de pointeur ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [unique](/windows/desktop/Midl/unique) \] et \[ [ptr](/windows/desktop/Midl/ptr) \] ) a des caractéristiques qui affectent l’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="b8ff7-106">Le tableau suivant récapitule ces caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="b8ff7-107">Attribut de pointeur</span><span class="sxs-lookup"><span data-stu-id="b8ff7-107">Pointer attribute</span></span>       | <span data-ttu-id="b8ff7-108">Client</span><span class="sxs-lookup"><span data-stu-id="b8ff7-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="b8ff7-109">Serveur</span><span class="sxs-lookup"><span data-stu-id="b8ff7-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b8ff7-110">Référence ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="b8ff7-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="b8ff7-111">L’application cliente doit allouer.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="b8ff7-112">Gestion spéciale nécessaire pour les pointeurs de niveau nontop en **\[ sortie \]** seule.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="b8ff7-113">Unique ( \[ **unique** \] )</span><span class="sxs-lookup"><span data-stu-id="b8ff7-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="b8ff7-114">Si un paramètre est, l’application cliente doit allouer ; s’il est incorporé, peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="b8ff7-115">Si vous remplacez la valeur NULL par une valeur non null, le stub client est alloué. le passage de la valeur non null à la valeur NULL peut entraîner l’orphelin.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="b8ff7-116">Full ( \[ **ptr** \] )</span><span class="sxs-lookup"><span data-stu-id="b8ff7-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="b8ff7-117">Si un paramètre est, l’application cliente doit allouer ; s’il est incorporé, peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="b8ff7-118">Si vous remplacez la valeur NULL par une valeur non null, le stub client est alloué. le passage de la valeur non null à la valeur NULL peut entraîner l’orphelin.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="b8ff7-119">L’attribut **\[ Ref \]** indique que le pointeur pointe vers une mémoire valide.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="b8ff7-120">Par définition, l’application cliente doit allouer toute la mémoire requise par les pointeurs de référence.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="b8ff7-121">Le pointeur unique peut passer de la valeur null à la valeur non null.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="b8ff7-122">Si le pointeur unique passe de null à non null, une nouvelle mémoire est allouée sur le client.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="b8ff7-123">Si le pointeur unique passe de non null à null, l’orphelin peut en résulter.</span><span class="sxs-lookup"><span data-stu-id="b8ff7-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="b8ff7-124">Pour plus d’informations, consultez [orphelins de mémoire](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="b8ff7-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

