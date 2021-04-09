---
title: cpp_quote (attribut)
description: Le \_ mot clé du guillemet CPP demande à MIDL d’émettre la chaîne spécifiée, sans les caractères guillemets, dans le fichier d’en-tête généré.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote MIDL de l’attribut
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030358"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="7691c-104">\_attribut de guillemets CPP</span><span class="sxs-lookup"><span data-stu-id="7691c-104">cpp\_quote attribute</span></span>

<span data-ttu-id="7691c-105">Le mot clé du **\_ guillemet CPP** demande à MIDL d’émettre la chaîne spécifiée, sans les caractères guillemets, dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="7691c-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="7691c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7691c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7691c-107">*string*</span><span class="sxs-lookup"><span data-stu-id="7691c-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="7691c-108">Spécifie une chaîne entre guillemets émise dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="7691c-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="7691c-109">La chaîne doit être placée entre guillemets pour empêcher l’extension par le préprocesseur C.</span><span class="sxs-lookup"><span data-stu-id="7691c-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7691c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7691c-110">Remarks</span></span>

<span data-ttu-id="7691c-111">Les directives de prétraitement du langage c qui s’affichent dans le fichier IDL sont traitées par le préprocesseur du compilateur C.</span><span class="sxs-lookup"><span data-stu-id="7691c-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="7691c-112">Les directives de **\# définition** dans le fichier IDL sont disponibles pendant la compilation MIDL, mais ne sont pas disponibles pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="7691c-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="7691c-113">Par exemple, quand le préprocesseur rencontre la directive « \# définir Windows 4 », le préprocesseur remplace toutes les occurrences de « Windows » dans le fichier IDL par « 4 ».</span><span class="sxs-lookup"><span data-stu-id="7691c-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="7691c-114">Le symbole « WINDOWS » n’est pas disponible lors de la compilation en langage C.</span><span class="sxs-lookup"><span data-stu-id="7691c-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="7691c-115">Pour permettre aux définitions de macros de préprocesseur C de passer par le compilateur MIDL au compilateur C, utilisez la directive **\# pragma MIDL \_ echo** ou le **\_ guillemet RPC** .</span><span class="sxs-lookup"><span data-stu-id="7691c-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="7691c-116">Ces directives indiquent au compilateur MIDL de générer un fichier d’en-tête qui contient la chaîne de paramètre avec les guillemets supprimés.</span><span class="sxs-lookup"><span data-stu-id="7691c-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="7691c-117">Les directives **\# pragma MIDL \_ echo** et **CPP des \_ guillemets** sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="7691c-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="7691c-118">Le compilateur MIDL place les chaînes spécifiées dans les directives de **\_ guillemet** et [**pragma**](pragma.md) cpp dans le fichier d’en-tête, dans l’ordre dans lequel elles sont spécifiées dans le fichier IDL, et par rapport à d’autres composants d’interface dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="7691c-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="7691c-119">Les chaînes doivent généralement apparaître dans la section corps de l’interface de fichier IDL après toutes les opérations d' [**importation**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="7691c-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="7691c-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="7691c-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="7691c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7691c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7691c-122">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7691c-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7691c-123">**port**</span><span class="sxs-lookup"><span data-stu-id="7691c-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="7691c-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="7691c-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




