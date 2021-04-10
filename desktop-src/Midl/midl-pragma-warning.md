---
title: attribut midl_pragma Warning
description: Utilisez l' \_ option d’avertissement du pragma MIDL pour remplacer temporairement le comportement du message d’avertissement de MIDL au moment de la compilation.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma MIDL de l’attribut d’avertissement
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841109"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="f3115-104">MIDL \_ pragma warning (attribut)</span><span class="sxs-lookup"><span data-stu-id="f3115-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="f3115-105">Utilisez l’option d' **\_ Avertissement du pragma MIDL** pour remplacer temporairement le comportement du message d’avertissement de MIDL au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="f3115-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="f3115-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3115-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3115-107">*option d’avertissement \_*</span><span class="sxs-lookup"><span data-stu-id="f3115-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="f3115-108">L’option d’avertissement peut être l’une des suivantes : désactiver, activer, valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f3115-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="f3115-109">*Liste des messages \_*</span><span class="sxs-lookup"><span data-stu-id="f3115-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="f3115-110">Liste de numéros de message séparés par des espaces.</span><span class="sxs-lookup"><span data-stu-id="f3115-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3115-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3115-111">Remarks</span></span>

<span data-ttu-id="f3115-112">Le pragma peut être utilisé comme un pragma de compilateur C.</span><span class="sxs-lookup"><span data-stu-id="f3115-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="f3115-113">Autrement dit, il désactive, active ou retourne le comportement par défaut pour un avertissement MIDL donné.</span><span class="sxs-lookup"><span data-stu-id="f3115-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="f3115-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="f3115-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="f3115-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3115-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3115-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="f3115-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




