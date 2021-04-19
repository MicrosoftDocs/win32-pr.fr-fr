---
description: La propriété Language en lecture seule de l’objet Error retourne l’ID de langue de l’erreur actuelle.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propriété Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541384"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="26e98-103">Error. Language, propriété</span><span class="sxs-lookup"><span data-stu-id="26e98-103">Error.Language property</span></span>

<span data-ttu-id="26e98-104">La propriété **Language** en lecture seule de l’objet [**Error**](error-object.md) retourne l' **ID de langue** de l’erreur actuelle.</span><span class="sxs-lookup"><span data-stu-id="26e98-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="26e98-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="26e98-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e98-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26e98-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="26e98-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="26e98-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="26e98-108">Notes</span><span class="sxs-lookup"><span data-stu-id="26e98-108">Remarks</span></span>

<span data-ttu-id="26e98-109">La valeur de la propriété **Language** est-1, sauf si l’erreur est de type MsmErrorLanguageUnsupported ou msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="26e98-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="26e98-110">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="26e98-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="26e98-111">C++</span><span class="sxs-lookup"><span data-stu-id="26e98-111">C++</span></span>

<span data-ttu-id="26e98-112">Consultez [**obtenir une \_ fonction de langage (objet d’erreur)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="26e98-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="26e98-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26e98-113">Requirements</span></span>



| <span data-ttu-id="26e98-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26e98-114">Requirement</span></span> | <span data-ttu-id="26e98-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="26e98-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e98-116">Version</span><span class="sxs-lookup"><span data-stu-id="26e98-116">Version</span></span><br/> | <span data-ttu-id="26e98-117">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="26e98-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="26e98-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="26e98-118">Header</span></span><br/>  | <dl> <span data-ttu-id="26e98-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e98-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="26e98-120">DLL</span><span class="sxs-lookup"><span data-stu-id="26e98-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="26e98-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e98-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

