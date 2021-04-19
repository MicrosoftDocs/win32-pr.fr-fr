---
description: Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne. L’utilisateur peut ignorer le message, entrer le débogueur ou quitter l’application. Ignoré dans les builds de vente au détail.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: DbgBreak macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527334"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="51ae5-105">DbgBreak macro)</span><span class="sxs-lookup"><span data-stu-id="51ae5-105">DbgBreak macro</span></span>

<span data-ttu-id="51ae5-106">Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne.</span><span class="sxs-lookup"><span data-stu-id="51ae5-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="51ae5-107">L’utilisateur peut ignorer le message, entrer le débogueur ou quitter l’application.</span><span class="sxs-lookup"><span data-stu-id="51ae5-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="51ae5-108">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="51ae5-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ae5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51ae5-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="51ae5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51ae5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ae5-111">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="51ae5-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="51ae5-112">Chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="51ae5-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ae5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51ae5-113">Return value</span></span>

<span data-ttu-id="51ae5-114">Cette macro ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="51ae5-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="51ae5-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="51ae5-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="51ae5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51ae5-116">Requirements</span></span>



| <span data-ttu-id="51ae5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51ae5-117">Requirement</span></span> | <span data-ttu-id="51ae5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="51ae5-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51ae5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="51ae5-119">Header</span></span><br/> | <dl> <span data-ttu-id="51ae5-120"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51ae5-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ae5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51ae5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ae5-122">Macros Assert et Breakpoint</span><span class="sxs-lookup"><span data-stu-id="51ae5-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




