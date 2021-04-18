---
title: attribut explicit_handle
description: L’attribut \ \_ CCP handle \ ACF spécifie que chaque procédure a, comme premier paramètre, un handle primitif, tel qu’un type de handle \_ t.
ms.assetid: c95d005e-dcc7-4d83-885d-91c0773c0ed8
keywords:
- explicit_handle MIDL de l’attribut
topic_type:
- apiref
api_name:
- explicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4fa677f1bb5a3414e6cf6dc761b83414c2d68b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509226"
---
# <a name="explicit_handle-attribute"></a><span data-ttu-id="9ff18-104">\_attribut handle explicite</span><span class="sxs-lookup"><span data-stu-id="9ff18-104">explicit\_handle attribute</span></span>

<span data-ttu-id="9ff18-105">L' \[ attribut CCP de **\_ handle explicite** \] spécifie que chaque procédure a, en tant que premier paramètre, un handle primitif, tel qu’un type de [**handle \_ t**](handle-t.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff18-105">The \[**explicit\_handle**\] ACF attribute specifies that each procedure has, as its first parameter, a primitive handle, such as a [**handle\_t**](handle-t.md) type.</span></span>

``` syntax
[
    explicit_handle
] 
interface interface-name
{
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="9ff18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ff18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff18-107">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="9ff18-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff18-108">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="9ff18-108">Specifies the name of the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ff18-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ff18-109">Remarks</span></span>

<span data-ttu-id="9ff18-110">Lorsque vous utilisez l’attribut **\[ \_ handle \] explicite** , chaque procédure a un handle primitif comme premier paramètre, même si le fichier IDL ne contient pas ce handle dans sa liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="9ff18-110">When you use the **\[explicit\_handle\]** attribute, each procedure has a primitive handle as its first parameter even if the IDL file does not contain this handle in its parameter list.</span></span> <span data-ttu-id="9ff18-111">Les prototypes émis dans le fichier d’en-tête et les routines stub contiennent le paramètre supplémentaire, et ce paramètre est utilisé comme handle pour diriger l’appel distant.</span><span class="sxs-lookup"><span data-stu-id="9ff18-111">The prototypes emitted to the header file and stub routines contain the additional parameter, and that parameter is used as the handle for directing the remote call.</span></span>

<span data-ttu-id="9ff18-112">L’attribut **\[ \_ handle \] explicite** affecte les procédures distantes et les procédures de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="9ff18-112">The **\[explicit\_handle\]** attribute affects both remote procedures and serialization procedures.</span></span> <span data-ttu-id="9ff18-113">Pour la sérialisation de type, les routines de prise en charge sont générées avec le paramètre initial en tant que handle explicite (sérialisation).</span><span class="sxs-lookup"><span data-stu-id="9ff18-113">For type serialization, the support routines are generated with the initial parameter as an explicit (serialization) handle.</span></span> <span data-ttu-id="9ff18-114">Si l’attribut **\[ \_ handle \] explicite** n’est pas utilisé, l’application peut toujours spécifier qu’une opération a un handle explicite (liaison ou sérialisation) dirigeant l’appel.</span><span class="sxs-lookup"><span data-stu-id="9ff18-114">If the **\[explicit\_handle\]** attribute is not used, the application can still specify that an operation have an explicit handle (binding or serialization) directing the call.</span></span> <span data-ttu-id="9ff18-115">Pour ce faire, un prototype avec un argument contenant un type de handle est fourni au fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="9ff18-115">To do this, a prototype with an argument containing a handle type is supplied to the IDL file.</span></span> <span data-ttu-id="9ff18-116">Notez que, en mode par défaut, un argument qui n’apparaît pas en premier peut également être utilisé comme un handle dirigeant l’appel.</span><span class="sxs-lookup"><span data-stu-id="9ff18-116">Note that in default mode, an argument that does not appear first can also be used as a handle directing the call.</span></span>

<span data-ttu-id="9ff18-117">Par conséquent, si l’attribut **\[ \_ handle \] explicite** est un moyen de donner au prototype IDL un attribut de **\[ \_ handle \] explicite** primitif, il ne nécessite pas nécessairement une modification du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="9ff18-117">Therefore, while the **\[explicit\_handle\]** attribute is a way of giving the IDL prototype a primitive **\[explicit\_handle\]** attribute, it does not necessarily require a change to the IDL file.</span></span> <span data-ttu-id="9ff18-118">En mode [**/OSF**](-osf.md) , seul le premier argument peut être utilisé comme type de handle explicite.</span><span class="sxs-lookup"><span data-stu-id="9ff18-118">In [**/osf**](-osf.md) mode only the first argument can be used as an explicit handle type.</span></span>

<span data-ttu-id="9ff18-119">L’attribut **\[ \_ handle \] explicite** peut être utilisé en tant qu’attribut d’interface ou en tant qu’attribut d’opération.</span><span class="sxs-lookup"><span data-stu-id="9ff18-119">The **\[explicit\_handle\]** attribute can be used as either an interface attribute or an operation attribute.</span></span> <span data-ttu-id="9ff18-120">En tant qu’attribut d’interface, il affecte toutes les opérations dans l’interface et tous les types qui requièrent la prise en charge de la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="9ff18-120">As an interface attribute, it affects all the operations in the interface and all the types that require serialization support.</span></span> <span data-ttu-id="9ff18-121">Toutefois, si elle est utilisée en tant qu’attribut d’opération, elle affecte uniquement cette opération particulière.</span><span class="sxs-lookup"><span data-stu-id="9ff18-121">If, however, it is used as an operation attribute, it affects only that particular operation.</span></span> <span data-ttu-id="9ff18-122">Si une méthode contient un ou plusieurs \[ \] Handles de contexte, le plus \[ à gauche dans le \] handle de contexte est utilisé comme handle de liaison, et aucun handle explicite supplémentaire n’est créé.</span><span class="sxs-lookup"><span data-stu-id="9ff18-122">If a method contains one or more \[in\] context handles, the left most \[in\] context handle is used as the binding handle, and no additional explicit handle is created.</span></span>

## <a name="examples"></a><span data-ttu-id="9ff18-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ff18-123">Examples</span></span>

``` syntax
/* ACF File */ 
[
    explicit_handle
] 
interface iface
{ 
    // Interface definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="9ff18-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff18-125">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="9ff18-125">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="9ff18-126">**\_handle automatique**</span><span class="sxs-lookup"><span data-stu-id="9ff18-126">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="9ff18-127">**handle implicite \_**</span><span class="sxs-lookup"><span data-stu-id="9ff18-127">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="9ff18-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="9ff18-128">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




