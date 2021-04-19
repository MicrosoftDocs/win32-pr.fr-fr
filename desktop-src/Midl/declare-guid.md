---
title: declare_guid, mot clé
description: Le \_ mot clé Declare GUID demande à MIDL d’émettre une variable GUID dans le fichier d’en-tête généré.
keywords:
- declare_guid mot clé MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106538248"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="ae871-104">\_mot clé Declare GUID</span><span class="sxs-lookup"><span data-stu-id="ae871-104">declare\_guid keyword</span></span>

<span data-ttu-id="ae871-105">Le mot clé **Declare \_ GUID** demande à MIDL d’émettre une variable GUID dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="ae871-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="ae871-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae871-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae871-107">*variable-nom*</span><span class="sxs-lookup"><span data-stu-id="ae871-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ae871-108">Spécifie un nom de variable pour l’identificateur dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="ae871-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="ae871-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="ae871-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="ae871-110">Spécifie le [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) qui s’appliquera au nom de la variable dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="ae871-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ae871-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="ae871-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="ae871-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ae871-112">Remarks</span></span>

<span data-ttu-id="ae871-113">L’utilisation de équivaut `declare_guid` à l’utilisation de `cpp_quote` pour générer un appel de la `EXTERN_GUID` macro.</span><span class="sxs-lookup"><span data-stu-id="ae871-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="ae871-114">L’exemple ci-dessus donne la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="ae871-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="ae871-115">L' `declare_guid` instruction est fournie à titre de commodité.</span><span class="sxs-lookup"><span data-stu-id="ae871-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="ae871-116">Elle présente l’avantage d’utiliser la même syntaxe de GUID que l' [ `uuid` attribut](uuid.md).</span><span class="sxs-lookup"><span data-stu-id="ae871-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae871-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae871-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae871-118">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="ae871-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="ae871-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="ae871-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="ae871-120">**uuid (attribut)**</span><span class="sxs-lookup"><span data-stu-id="ae871-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="ae871-121">**Structure GUID**</span><span class="sxs-lookup"><span data-stu-id="ae871-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
