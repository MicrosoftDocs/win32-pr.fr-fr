---
title: Decode, attribut
description: L’attribut \ Decode \ ACF spécifie qu’une procédure ou un type a besoin d’une prise en charge de la désérialisation.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decoded, attribut MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314904"
---
# <a name="decode-attribute"></a><span data-ttu-id="a948c-104">Decode, attribut</span><span class="sxs-lookup"><span data-stu-id="a948c-104">decode attribute</span></span>

<span data-ttu-id="a948c-105">L’attribut **\[ Decode \]** ACF spécifie qu’une procédure ou un type a besoin d’une prise en charge de la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="a948c-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="a948c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a948c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a948c-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="a948c-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-108">Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a948c-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-109">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="a948c-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-110">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a948c-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-111">*définition d’interface*</span><span class="sxs-lookup"><span data-stu-id="a948c-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-112">Spécifie les instructions IDL qui forment la définition de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a948c-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-113">*op-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="a948c-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-114">Spécifie d’autres attributs opérationnels qui s’appliquent à la procédure, tels que **\[** [**encode**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a948c-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-115">*nom de la procédure*</span><span class="sxs-lookup"><span data-stu-id="a948c-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-116">Spécifie le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="a948c-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-117">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="a948c-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-118">Spécifie d’autres attributs, tels que **\[** [**encode**](encode.md) **\]** et **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a948c-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a948c-119">*nom du type*</span><span class="sxs-lookup"><span data-stu-id="a948c-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a948c-120">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a948c-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a948c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="a948c-121">Remarks</span></span>

<span data-ttu-id="a948c-122">L’attribut **\[ Decode \]** fait en sorte que le compilateur MIDL génère du code qu’une application peut utiliser pour récupérer des données sérialisées à partir d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a948c-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="a948c-123">L' **\[** attribut [**encode**](encode.md) **\]** fournit la prise en charge de la sérialisation, en générant le code permettant de sérialiser les données dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a948c-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="a948c-124">Utilisez les **\[** [](encode.md) **\]** attributs encode et **\[ Decode \]** dans un CCP pour générer le code de sérialisation des procédures ou des types définis dans le fichier IDL d’une interface.</span><span class="sxs-lookup"><span data-stu-id="a948c-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="a948c-125">Lorsqu’il est utilisé comme attribut d’interface, **\[ Decode \]** s’applique à tous les types et procédures définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a948c-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="a948c-126">En cas d’utilisation comme attribut de type, **\[ Decode \]** s’applique uniquement au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="a948c-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="a948c-127">En cas d’utilisation comme attribut opérationnel, **\[ Decode \]** s’applique uniquement à cette procédure.</span><span class="sxs-lookup"><span data-stu-id="a948c-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="a948c-128">Pour plus d’informations sur l’utilisation de cette prise en charge de la sérialisation, consultez [services de sérialisation](/windows/desktop/Rpc/serialization-services) et **\[** [**encodage**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a948c-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a948c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a948c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a948c-130">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="a948c-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a948c-131">**lui**</span><span class="sxs-lookup"><span data-stu-id="a948c-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="a948c-132">**contraire**</span><span class="sxs-lookup"><span data-stu-id="a948c-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 