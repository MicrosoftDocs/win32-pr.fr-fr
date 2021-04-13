---
title: attribut booléen
description: Le mot clé Boolean indique que l’expression ou l’expression constante associée à l’identificateur accepte uniquement les valeurs TRUE et FALSe.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- attribut booléen MIDL
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380857"
---
# <a name="boolean-attribute"></a><span data-ttu-id="45d4b-104">attribut booléen</span><span class="sxs-lookup"><span data-stu-id="45d4b-104">boolean attribute</span></span>

<span data-ttu-id="45d4b-105">Le mot clé **Boolean** indique que l’expression ou l’expression constante associée à l’identificateur accepte uniquement les valeurs **true** et **false**.</span><span class="sxs-lookup"><span data-stu-id="45d4b-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="45d4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d4b-107">*identificateur-nom*</span><span class="sxs-lookup"><span data-stu-id="45d4b-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="45d4b-108">Spécifie un identificateur MIDL valide.</span><span class="sxs-lookup"><span data-stu-id="45d4b-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="45d4b-109">Les identificateurs MIDL valides se composent de 31 caractères alphanumériques et/ou de traits de soulignement, et doivent commencer par un caractère alphabétique ou un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="45d4b-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d4b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="45d4b-110">Remarks</span></span>

<span data-ttu-id="45d4b-111">Le type **booléen** est l’un des types de base du langage IDL.</span><span class="sxs-lookup"><span data-stu-id="45d4b-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="45d4b-112">Le type **booléen** peut apparaître comme un spécificateur de type dans les déclarations [**const**](const.md) , les déclarations [**typedef**](typedef.md) , les déclarations générales et les déclarateurs de fonction (en tant que spécificateur de type fonction-retour et en tant que spécificateur de type de paramètre).</span><span class="sxs-lookup"><span data-stu-id="45d4b-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="45d4b-113">Pour le contexte dans lequel les spécificateurs de type s’affichent, consultez [fichier de définition d’interface (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="45d4b-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="45d4b-114">Le type de base **booléen** n’est pas compatible avec l’attribut [**oleautomation**](oleautomation.md) .</span><span class="sxs-lookup"><span data-stu-id="45d4b-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="45d4b-115">Utilisez \_ la variante booléenne dans vos interfaces compatibles Automation.</span><span class="sxs-lookup"><span data-stu-id="45d4b-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="45d4b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45d4b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d4b-117">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="45d4b-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="45d4b-118">**const**</span><span class="sxs-lookup"><span data-stu-id="45d4b-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="45d4b-119">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="45d4b-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="45d4b-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="45d4b-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="45d4b-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="45d4b-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




