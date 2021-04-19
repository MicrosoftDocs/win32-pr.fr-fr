---
title: attribut d’octet
description: Le mot clé Byte spécifie un élément de données de 8 bits.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- MIDL d’attribut d’octet
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511660"
---
# <a name="byte-attribute"></a><span data-ttu-id="165e9-104">attribut d’octet</span><span class="sxs-lookup"><span data-stu-id="165e9-104">byte attribute</span></span>

<span data-ttu-id="165e9-105">Le mot clé **Byte** spécifie un élément de données de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="165e9-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="165e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="165e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165e9-107">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="165e9-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="165e9-108">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="165e9-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="165e9-109">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="165e9-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="165e9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="165e9-110">Remarks</span></span>

<span data-ttu-id="165e9-111">Un élément de données **Byte** ne subit pas de conversion pour la transmission sur le réseau en tant que type [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="165e9-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="165e9-112">Le type **Byte** est l’un des types de base du langage IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="165e9-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="165e9-113">Le type d' **octet** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et en tant que spécificateur de type paramètre).</span><span class="sxs-lookup"><span data-stu-id="165e9-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="165e9-114">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="165e9-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="165e9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="165e9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165e9-116">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="165e9-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="165e9-117">**Char**</span><span class="sxs-lookup"><span data-stu-id="165e9-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="165e9-118">**const**</span><span class="sxs-lookup"><span data-stu-id="165e9-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="165e9-119">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="165e9-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="165e9-120">**typedef**</span><span class="sxs-lookup"><span data-stu-id="165e9-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




