---
title: attribut notify_flag
description: L’attribut \ notification \_ Flag \ fournit une notification indiquant si une routine de serveur est appelée.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag MIDL de l’attribut
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030062"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="0f8c5-104">attribut notifier l' \_ indicateur</span><span class="sxs-lookup"><span data-stu-id="0f8c5-104">notify\_flag attribute</span></span>

<span data-ttu-id="0f8c5-105">L’attribut **\[ \_ indicateur \] Notify** fournit une notification indiquant si une routine serveur est appelée.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="0f8c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f8c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8c5-107">*nom de la procédure*</span><span class="sxs-lookup"><span data-stu-id="0f8c5-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0f8c5-108">Nom de la procédure distante à laquelle la procédure de l’indicateur de notification \_ est associée.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f8c5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0f8c5-109">Remarks</span></span>

<span data-ttu-id="0f8c5-110">L’attribut **\[ \_ indicateur \] Notify** est semblable à l’utilisation de l’attribut **\[ Notify \]** .</span><span class="sxs-lookup"><span data-stu-id="0f8c5-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="0f8c5-111">Le nom de la procédure d' **\[ \_ indicateur \] Notify** est le nom de la procédure distante suffixée par l' **\_ \_ indicateur Notify**.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="0f8c5-112">La procédure de **\_ notification d' \_ indicateur** ne nécessite aucun paramètre et ne retourne pas de résultat.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="0f8c5-113">Un prototype de cette procédure est également généré dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="0f8c5-114">Par exemple, si le fichier IDL contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0f8c5-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="0f8c5-115">Spécifiez ce qui suit dans le ACF pour MIDL afin de générer l’appel de **\_ notification \_ Flag** :</span><span class="sxs-lookup"><span data-stu-id="0f8c5-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="0f8c5-116">Le compilateur MIDL génère le code stub du serveur qui contient l’appel suivant à la procédure **\_ notification \_ Flag** :</span><span class="sxs-lookup"><span data-stu-id="0f8c5-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="0f8c5-117">Le fichier d’en-tête contiendra un prototype :</span><span class="sxs-lookup"><span data-stu-id="0f8c5-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="0f8c5-118">**\_ MIDL \_ NotifyFlag** a la **valeur true** si la routine de serveur est appelée.</span><span class="sxs-lookup"><span data-stu-id="0f8c5-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="0f8c5-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="0f8c5-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="0f8c5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f8c5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8c5-121">**indiquer**</span><span class="sxs-lookup"><span data-stu-id="0f8c5-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




