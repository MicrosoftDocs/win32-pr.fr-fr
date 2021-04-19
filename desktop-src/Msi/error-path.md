---
description: Dans Windows Installer versions 1,0 et 1,1, la propriété Path est toujours la chaîne vide. Les versions ultérieures peuvent utiliser cette valeur pour retourner le chemin d’accès au fichier ou au répertoire qui n’a pas pu être créé.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Error. Path, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528684"
---
# <a name="errorpath-property"></a><span data-ttu-id="0db43-104">Error. Path, propriété</span><span class="sxs-lookup"><span data-stu-id="0db43-104">Error.Path property</span></span>

<span data-ttu-id="0db43-105">Dans Windows Installer versions 1,0 et 1,1, la propriété Path est toujours la chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="0db43-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="0db43-106">Les versions ultérieures peuvent utiliser cette valeur pour retourner le chemin d’accès au fichier ou au répertoire qui n’a pas pu être créé.</span><span class="sxs-lookup"><span data-stu-id="0db43-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="0db43-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0db43-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db43-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0db43-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="0db43-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0db43-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0db43-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0db43-110">Remarks</span></span>

<span data-ttu-id="0db43-111">Cette valeur est valide uniquement pour les erreurs de type msmErrorFileCreate ou msmErrorDirCreate.</span><span class="sxs-lookup"><span data-stu-id="0db43-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="0db43-112">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="0db43-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="0db43-113">C++</span><span class="sxs-lookup"><span data-stu-id="0db43-113">C++</span></span>

<span data-ttu-id="0db43-114">Consultez la fonction [**obtenir le \_ chemin**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) .</span><span class="sxs-lookup"><span data-stu-id="0db43-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db43-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0db43-115">Requirements</span></span>



| <span data-ttu-id="0db43-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0db43-116">Requirement</span></span> | <span data-ttu-id="0db43-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0db43-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db43-118">Version</span><span class="sxs-lookup"><span data-stu-id="0db43-118">Version</span></span><br/> | <span data-ttu-id="0db43-119">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0db43-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="0db43-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0db43-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0db43-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db43-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="0db43-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0db43-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0db43-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db43-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

