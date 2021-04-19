---
title: void (attribut)
description: Le type de base void indique une procédure sans argument ou une procédure qui ne retourne pas de valeur de résultat.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- MIDL d’attribut void
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510239"
---
# <a name="void-attribute"></a><span data-ttu-id="a8d0d-104">void (attribut)</span><span class="sxs-lookup"><span data-stu-id="a8d0d-104">void attribute</span></span>

<span data-ttu-id="a8d0d-105">Le type de base **void** indique une procédure sans argument ou une procédure qui ne retourne pas de valeur de résultat.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-105">The base type **void** indicates a procedure with no arguments or a procedure that does not return a result value.</span></span>

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="a8d0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8d0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d0d-107">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="a8d0d-107">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d0d-108">Spécifie le nom de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-108">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a8d0d-109">*parameter-list*</span><span class="sxs-lookup"><span data-stu-id="a8d0d-109">*parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d0d-110">Spécifie la liste des paramètres passés à la fonction, ainsi que les types de paramètres et attributs de paramètre associés.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-110">Specifies the list of parameters passed to the function along with the associated parameter types and parameter attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a8d0d-111">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="a8d0d-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d0d-112">Spécifie le nom du type retourné par la fonction.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-112">Specifies the name of the type returned by the function.</span></span>

</dd> <dt>

<span data-ttu-id="a8d0d-113">*Context-handle-type*</span><span class="sxs-lookup"><span data-stu-id="a8d0d-113">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d0d-114">Spécifie le nom du type qui prend l' **\[** attribut de [**\_ handle de contexte**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a8d0d-114">Specifies the name of the type that takes the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8d0d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a8d0d-115">Remarks</span></span>

<span data-ttu-id="a8d0d-116">Le type de **pointeur \* void**, qui en C décrit un pointeur générique qui peut être casté pour représenter un type pointeur, est limité en MIDL avec le mot clé de **\[ \_ handle \] de contexte** .</span><span class="sxs-lookup"><span data-stu-id="a8d0d-116">The pointer type **void \***, which in C describes a generic pointer that can be cast to represent any pointer type, is limited in MIDL to its use with the **\[context\_handle\]** keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="a8d0d-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a8d0d-117">Examples</span></span>

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a><span data-ttu-id="a8d0d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8d0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d0d-119">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="a8d0d-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a8d0d-120">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="a8d0d-120">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a8d0d-121">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a8d0d-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




