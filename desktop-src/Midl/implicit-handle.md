---
title: attribut implicit_handle
description: L’attribut \ CCP (handle implicite) \_ \ ACF spécifie le descripteur utilisé pour les fonctions qui n’incluent pas de handle explicite en tant que paramètre de procédure.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841113"
---
# <a name="implicit_handle-attribute"></a><span data-ttu-id="e07c6-104">attribut de handle implicite \_</span><span class="sxs-lookup"><span data-stu-id="e07c6-104">implicit\_handle attribute</span></span>

<span data-ttu-id="e07c6-105">L’attribut CCP de **\[ \_ handle \] implicite** spécifie le descripteur utilisé pour les fonctions qui n’incluent pas de handle explicite en tant que paramètre de procédure.</span><span class="sxs-lookup"><span data-stu-id="e07c6-105">The **\[implicit\_handle\]** ACF attribute specifies the handle used for functions that do not include an explicit handle as a procedure parameter.</span></span>

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a><span data-ttu-id="e07c6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e07c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07c6-107">*handle-type*</span><span class="sxs-lookup"><span data-stu-id="e07c6-107">*handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="e07c6-108">Spécifie le type de données handle, tel que le type de base [**handle \_ t**](handle-t.md) ou un type de handle défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e07c6-108">Specifies the handle data type, such as the base type [**handle\_t**](handle-t.md) or a user-defined handle type.</span></span>

</dd> <dt>

<span data-ttu-id="e07c6-109">*handle-nom*</span><span class="sxs-lookup"><span data-stu-id="e07c6-109">*handle-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e07c6-110">Spécifie le nom du descripteur.</span><span class="sxs-lookup"><span data-stu-id="e07c6-110">Specifies the name of the handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e07c6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e07c6-111">Remarks</span></span>

<span data-ttu-id="e07c6-112">Le descripteur spécifié par l’attribut de **\[ \_ handle \] implicite** est utilisé de différentes façons en fonction de la nature de la procédure.</span><span class="sxs-lookup"><span data-stu-id="e07c6-112">The handle specified by the **\[implicit\_handle\]** attribute is used in different ways depending on the nature of the procedure.</span></span> <span data-ttu-id="e07c6-113">Si la procédure est distante, le handle sera utilisé comme handle de liaison pour l’appel distant.</span><span class="sxs-lookup"><span data-stu-id="e07c6-113">If the procedure is remote, the handle will be used as the binding handle for the remote call.</span></span> <span data-ttu-id="e07c6-114">Le handle implicite peut également être utilisé pour établir une liaison initiale pour une fonction qui utilise un handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="e07c6-114">The implicit handle may also be used to establish an initial binding for a function that uses a context handle.</span></span> <span data-ttu-id="e07c6-115">Si la procédure est une procédure de sérialisation, le handle est utilisé comme handle de sérialisation contrôlant l’opération.</span><span class="sxs-lookup"><span data-stu-id="e07c6-115">If the procedure is a serializing procedure, the handle is used as a serializing handle controlling the operation.</span></span> <span data-ttu-id="e07c6-116">Dans le cas de la sérialisation de type, le handle est utilisé comme handle de sérialisation pour tous les types sérialisés.</span><span class="sxs-lookup"><span data-stu-id="e07c6-116">In the case of type serialization, the handle is used as the serialization handle for all the serialized types.</span></span>

<span data-ttu-id="e07c6-117">L’attribut **\[ \_ handle \] implicite** spécifie une variable globale qui contient un handle utilisé par n’importe quelle fonction nécessitant des handles implicites.</span><span class="sxs-lookup"><span data-stu-id="e07c6-117">The **\[implicit\_handle\]** attribute specifies a global variable that contains a handle used by any function needing implicit handles.</span></span>

<span data-ttu-id="e07c6-118">Le type de handle de liaison implicite doit être [**handle \_ t**](handle-t.md) (ou un type basé sur **handle \_ t**) ou un type de handle défini par l’utilisateur spécifié avec l’attribut [**descripteur**](handle.md) .</span><span class="sxs-lookup"><span data-stu-id="e07c6-118">The implicit binding handle type must be either [**handle\_t**](handle-t.md) (or a type based on **handle\_t**) or a user-defined handle type specified with the [**handle**](handle.md) attribute.</span></span> <span data-ttu-id="e07c6-119">Le handle de sérialisation implicite doit être un type basé sur le **handle \_ t**.</span><span class="sxs-lookup"><span data-stu-id="e07c6-119">The implicit serializing handle must be a type based on **handle\_t**.</span></span>

<span data-ttu-id="e07c6-120">Si le type de handle implicite n’est pas défini dans le fichier IDL ou dans tous les fichiers inclus et importés par le fichier IDL pour l’ordinateur MIDL, vous devez fournir le fichier contenant la définition de type handle-type lors de la compilation des stubs.</span><span class="sxs-lookup"><span data-stu-id="e07c6-120">If the implicit handle type is not defined in the IDL file or in any files included and imported by the IDL file for the MIDL computer, you must supply the file containing the handle-type definition when you compile the stubs.</span></span> <span data-ttu-id="e07c6-121">Utilisez l’instruction CCP [**include**](include.md) pour inclure le fichier contenant la définition handle-type.</span><span class="sxs-lookup"><span data-stu-id="e07c6-121">Use the ACF [**include**](include.md) statement to include the file containing the handle-type definition.</span></span>

<span data-ttu-id="e07c6-122">L’attribut de **\[ \_ handle \] implicite** peut se produire une seule fois, au plus.</span><span class="sxs-lookup"><span data-stu-id="e07c6-122">The **\[implicit\_handle\]** attribute can occur once, at most.</span></span> <span data-ttu-id="e07c6-123">L’attribut **\[ \_ handle \] implicite** peut se produire uniquement si les attributs [**\[ \_ handle \] automatique**](auto-handle.md) et [**\[ \_ handle \] explicite**](explicit-handle.md) ne se produisent pas.</span><span class="sxs-lookup"><span data-stu-id="e07c6-123">The **\[implicit\_handle\]** attribute can occur only if the [**\[auto\_handle\]**](auto-handle.md) and [**\[explicit\_handle\]**](explicit-handle.md) attributes do not occur.</span></span>

## <a name="examples"></a><span data-ttu-id="e07c6-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="e07c6-124">Examples</span></span>

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a><span data-ttu-id="e07c6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e07c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07c6-126">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="e07c6-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="e07c6-127">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="e07c6-127">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="e07c6-128">**\_handle explicite**</span><span class="sxs-lookup"><span data-stu-id="e07c6-128">**explicit\_handle**</span></span>](explicit-handle.md)
</dt> <dt>

[<span data-ttu-id="e07c6-129">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="e07c6-129">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="e07c6-130">**inclusion**</span><span class="sxs-lookup"><span data-stu-id="e07c6-130">**include**</span></span>](include.md)
</dt> </dl>

 

 




