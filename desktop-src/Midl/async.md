---
title: attribut Async
description: L’attribut \ Async \ ACF définit un appel de procédure distante en tant qu’opération asynchrone.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL, attribut Async
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940909"
---
# <a name="async-attribute"></a><span data-ttu-id="4fd02-104">attribut Async</span><span class="sxs-lookup"><span data-stu-id="4fd02-104">async attribute</span></span>

<span data-ttu-id="4fd02-105">L' \[  \] attribut Async ACF définit un appel de procédure distante en tant qu’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="4fd02-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="4fd02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fd02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd02-107">*opt-ACF-Attributes*</span><span class="sxs-lookup"><span data-stu-id="4fd02-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd02-108">Spécifie des attributs de configuration d’application facultatifs.</span><span class="sxs-lookup"><span data-stu-id="4fd02-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4fd02-109">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="4fd02-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd02-110">Spécifie le nom de la fonction dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="4fd02-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="4fd02-111">*Param-liste*</span><span class="sxs-lookup"><span data-stu-id="4fd02-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4fd02-112">Spécifie une liste de paramètres facultative.</span><span class="sxs-lookup"><span data-stu-id="4fd02-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fd02-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4fd02-113">Remarks</span></span>

<span data-ttu-id="4fd02-114">Cet attribut n’est pas applicable dans les interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="4fd02-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="4fd02-115">Pour déclarer une fonction RPC comme asynchrone, commencez par déclarer la fonction dans le cadre d’une définition d’interface dans un fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="4fd02-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="4fd02-116">Modifiez ensuite cette déclaration de fonction, dans le fichier de configuration de l’application (ACF), en appliquant l' \[  \] attribut Async.</span><span class="sxs-lookup"><span data-stu-id="4fd02-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="4fd02-117">Notez que la déclaration de fonction ne fait pas mention du handle asynchrone et que le handle de liaison est le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="4fd02-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="4fd02-118">L’application \[  \] de l’attribut Async dans le fichier ACF génère le code approprié afin que lorsque cette fonction est appelée, le serveur asynchrone s’attend à recevoir un handle asynchrone avant les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="4fd02-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="4fd02-119">L’attribut Async ne peut pas être utilisé avec le commutateur de ligne de commande [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd02-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4fd02-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="4fd02-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="4fd02-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fd02-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd02-122">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="4fd02-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="4fd02-123">RPC asynchrone</span><span class="sxs-lookup"><span data-stu-id="4fd02-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 