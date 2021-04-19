---
description: La propriété ModuleKeys en lecture seule de l’objet Error retourne un pointeur vers une collection de chaînes contenant les clés primaires de la ligne dans le module à l’origine de l’erreur, une clé par entrée dans la collection.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Erreur. ModuleKeys, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542519"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="1cc67-103">Error. ModuleKeys, propriété</span><span class="sxs-lookup"><span data-stu-id="1cc67-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="1cc67-104">La propriété **ModuleKeys** en lecture seule de l’objet [**Error**](error-object.md) retourne un pointeur vers une collection de chaînes contenant les clés primaires de la ligne dans le module à l’origine de l’erreur, une clé par entrée dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1cc67-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="1cc67-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1cc67-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc67-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cc67-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="1cc67-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1cc67-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc67-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1cc67-108">Remarks</span></span>

<span data-ttu-id="1cc67-109">Le client est responsable de la libération de la collection de chaînes lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1cc67-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="1cc67-110">La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1cc67-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="1cc67-111">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc67-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="1cc67-112">C++</span><span class="sxs-lookup"><span data-stu-id="1cc67-112">C++</span></span>

<span data-ttu-id="1cc67-113">Consultez la fonction [**obtenir \_ ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) .</span><span class="sxs-lookup"><span data-stu-id="1cc67-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc67-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc67-114">Requirements</span></span>



| <span data-ttu-id="1cc67-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc67-115">Requirement</span></span> | <span data-ttu-id="1cc67-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc67-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc67-117">Version</span><span class="sxs-lookup"><span data-stu-id="1cc67-117">Version</span></span><br/> | <span data-ttu-id="1cc67-118">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1cc67-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1cc67-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cc67-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1cc67-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc67-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cc67-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc67-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cc67-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc67-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

