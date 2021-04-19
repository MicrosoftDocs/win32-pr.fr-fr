---
description: La méthode Connect de l’objet Merge connecte un module à une fonctionnalité supplémentaire. Le module doit avoir déjà été fusionné dans la base de données ou sera fusionné dans la base de données. La fonctionnalité doit exister avant d’appeler cette fonction.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Merge. Connect, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543796"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="5a764-105">Merge. Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="5a764-105">Merge.Connect method</span></span>

<span data-ttu-id="5a764-106">La méthode **Connect** de l’objet [**Merge**](merge-object.md) connecte un module à une fonctionnalité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5a764-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="5a764-107">Le module doit avoir déjà été fusionné dans la base de données ou sera fusionné dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a764-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="5a764-108">La fonctionnalité doit exister avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="5a764-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="5a764-109">Les modifications apportées à la base de données ne sont pas enregistrées sur le disque, sauf si la méthode [**FermerBase**](merge-closedatabase.md) est appelée avec *BCommit* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5a764-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a764-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a764-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="5a764-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a764-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a764-112">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="5a764-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="5a764-113">Nom d’une fonctionnalité déjà existante dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="5a764-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a764-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a764-114">Return value</span></span>

<span data-ttu-id="5a764-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5a764-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a764-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5a764-116">Remarks</span></span>

<span data-ttu-id="5a764-117">Les erreurs peuvent être récupérées par le biais de la propriété [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="5a764-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="5a764-118">Les erreurs et les messages d’information sont publiés dans le fichier journal actuel.</span><span class="sxs-lookup"><span data-stu-id="5a764-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="5a764-119">C++</span><span class="sxs-lookup"><span data-stu-id="5a764-119">C++</span></span>

<span data-ttu-id="5a764-120">Consultez [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) , fonction.</span><span class="sxs-lookup"><span data-stu-id="5a764-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a764-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a764-121">Requirements</span></span>



| <span data-ttu-id="5a764-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a764-122">Requirement</span></span> | <span data-ttu-id="5a764-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a764-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a764-124">Version</span><span class="sxs-lookup"><span data-stu-id="5a764-124">Version</span></span><br/> | <span data-ttu-id="5a764-125">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5a764-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5a764-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a764-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5a764-127"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a764-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a764-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5a764-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a764-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a764-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
