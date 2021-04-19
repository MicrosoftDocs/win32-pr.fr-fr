---
description: La méthode FermerBase de l’objet Merge ferme la base de données Windows Installer actuellement ouverte.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. FermerBase, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523009"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="bdb2a-103">Merge. FermerBase, méthode</span><span class="sxs-lookup"><span data-stu-id="bdb2a-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="bdb2a-104">La méthode **FermerBase** de l’objet [**Merge**](merge-object.md) ferme la base de données Windows Installer actuellement ouverte.</span><span class="sxs-lookup"><span data-stu-id="bdb2a-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb2a-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="bdb2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb2a-107">*bCommit*</span><span class="sxs-lookup"><span data-stu-id="bdb2a-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb2a-108">**True** si les modifications doivent être enregistrées ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="bdb2a-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb2a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdb2a-109">Return value</span></span>

<span data-ttu-id="bdb2a-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bdb2a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb2a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb2a-111">Remarks</span></span>

<span data-ttu-id="bdb2a-112">La fermeture d’une base de données efface toutes les informations de dépendance, mais n’affecte pas les erreurs qui n’ont pas été récupérées.</span><span class="sxs-lookup"><span data-stu-id="bdb2a-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="bdb2a-113">C++</span><span class="sxs-lookup"><span data-stu-id="bdb2a-113">C++</span></span>

<span data-ttu-id="bdb2a-114">Consultez la fonction [**FermerBase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="bdb2a-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb2a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdb2a-115">Requirements</span></span>



| <span data-ttu-id="bdb2a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdb2a-116">Requirement</span></span> | <span data-ttu-id="bdb2a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdb2a-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb2a-118">Version</span><span class="sxs-lookup"><span data-stu-id="bdb2a-118">Version</span></span><br/> | <span data-ttu-id="bdb2a-119">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="bdb2a-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="bdb2a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdb2a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bdb2a-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb2a-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdb2a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bdb2a-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bdb2a-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb2a-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
