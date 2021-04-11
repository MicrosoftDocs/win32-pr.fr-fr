---
description: La propriété de manifeste est utilisée pour définir ou récupérer le contexte d’activation actif.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx. manifest, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951097"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="a6271-103">ActCtx. manifest, propriété</span><span class="sxs-lookup"><span data-stu-id="a6271-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="a6271-104">La propriété de **manifeste** est utilisée pour définir ou récupérer le contexte d’activation actif.</span><span class="sxs-lookup"><span data-stu-id="a6271-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="a6271-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a6271-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6271-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6271-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="a6271-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6271-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a6271-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a6271-108">Remarks</span></span>

<span data-ttu-id="a6271-109">Si un contexte d’activation peut être créé avec le fichier manifeste fourni, le script suivant définit la propriété de manifeste et active la constante d’activation spécifiée par le manifeste.</span><span class="sxs-lookup"><span data-stu-id="a6271-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="a6271-110">Si un contexte d’activation ne peut pas être créé à partir du manifeste, le contexte d’activation reste défini sur le contexte d’activation actuellement actif.</span><span class="sxs-lookup"><span data-stu-id="a6271-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="a6271-111">ActCtxObj. manifest = "<*nom du fichier manifeste*>";</span><span class="sxs-lookup"><span data-stu-id="a6271-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="a6271-112">Si un contexte d’activation a déjà été créé ou activé, le script suivant définit la propriété de **manifeste** sur le contexte d’activation actuel.</span><span class="sxs-lookup"><span data-stu-id="a6271-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="a6271-113">Si un contexte d’activation n’a pas été créé ou activé précédemment, définit la propriété de **manifeste** sur une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="a6271-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="a6271-114">« BSTR bstrManifest = ActCtxObj. manifest »</span><span class="sxs-lookup"><span data-stu-id="a6271-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="a6271-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6271-115">Requirements</span></span>



| <span data-ttu-id="a6271-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6271-116">Requirement</span></span> | <span data-ttu-id="a6271-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6271-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6271-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6271-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6271-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6271-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6271-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6271-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6271-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6271-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6271-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a6271-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6271-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6271-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6271-124">IID</span><span class="sxs-lookup"><span data-stu-id="a6271-124">IID</span></span><br/>                      | <span data-ttu-id="a6271-125">IID \_ IActCtx est défini en tant que 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="a6271-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




