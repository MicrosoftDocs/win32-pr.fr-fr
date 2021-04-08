---
title: attribut Switch
description: Le mot clé Switch sélectionne le discriminante pour une Union encapsulée \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- MIDL d’attribut de commutateur
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940469"
---
# <a name="switch-attribute"></a><span data-ttu-id="ed8ad-104">attribut Switch</span><span class="sxs-lookup"><span data-stu-id="ed8ad-104">switch attribute</span></span>

<span data-ttu-id="ed8ad-105">Le mot clé **switch** sélectionne le discriminante pour une [**\_ Union encapsulée**](encapsulated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="ed8ad-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="ed8ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed8ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8ad-107">*type de commutateur*</span><span class="sxs-lookup"><span data-stu-id="ed8ad-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8ad-108">Spécifie un type [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) ou un identificateur qui correspond à l’un de ces types.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="ed8ad-109">*nom du commutateur*</span><span class="sxs-lookup"><span data-stu-id="ed8ad-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8ad-110">Spécifie le nom de la variable de type *switch-type* qui agit en tant que discriminante d’Union.</span><span class="sxs-lookup"><span data-stu-id="ed8ad-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ed8ad-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="ed8ad-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="ed8ad-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed8ad-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8ad-113">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ed8ad-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ed8ad-114">Unions qui ne sont pas encapsulées</span><span class="sxs-lookup"><span data-stu-id="ed8ad-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="ed8ad-115">**le commutateur \_ est**</span><span class="sxs-lookup"><span data-stu-id="ed8ad-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="ed8ad-116">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="ed8ad-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="ed8ad-117">**UE**</span><span class="sxs-lookup"><span data-stu-id="ed8ad-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




