---
description: La méthode OpenLog de l’objet Merge ouvre un fichier journal qui reçoit les messages de progression et d’erreur. Si le fichier journal existe déjà, le programme d’installation ajoute de nouveaux messages. Si le fichier journal n’existe pas, le programme d’installation crée un fichier journal.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Merge. OpenLog, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540111"
---
# <a name="mergeopenlog-method"></a><span data-ttu-id="96d1c-105">Merge. OpenLog, méthode</span><span class="sxs-lookup"><span data-stu-id="96d1c-105">Merge.OpenLog method</span></span>

<span data-ttu-id="96d1c-106">La méthode **OpenLog** de l’objet [**Merge**](merge-object.md) ouvre un fichier journal qui reçoit les messages de progression et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="96d1c-106">The **OpenLog** method of the [**Merge**](merge-object.md) object opens a log file that receives progress and error messages.</span></span> <span data-ttu-id="96d1c-107">Si le fichier journal existe déjà, le programme d’installation ajoute de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="96d1c-107">If the log file already exists, the installer appends new messages.</span></span> <span data-ttu-id="96d1c-108">Si le fichier journal n’existe pas, le programme d’installation crée un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="96d1c-108">If the log file does not exist, the installer creates a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d1c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96d1c-109">Syntax</span></span>


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a><span data-ttu-id="96d1c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96d1c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d1c-111">*Nom du fichier*</span><span class="sxs-lookup"><span data-stu-id="96d1c-111">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="96d1c-112">Nom de fichier complet pointant vers un fichier à ouvrir ou à créer.</span><span class="sxs-lookup"><span data-stu-id="96d1c-112">Fully qualified file name pointing to a file to open or create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d1c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96d1c-113">Return value</span></span>

<span data-ttu-id="96d1c-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="96d1c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d1c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="96d1c-115">Remarks</span></span>

<span data-ttu-id="96d1c-116">Les clients peuvent envoyer leurs propres messages à ce fichier journal par le biais de la méthode [**log**](merge-log.md) .</span><span class="sxs-lookup"><span data-stu-id="96d1c-116">Clients may send their own messages to this log file through the [**Log**](merge-log.md) method.</span></span>

### <a name="c"></a><span data-ttu-id="96d1c-117">C++</span><span class="sxs-lookup"><span data-stu-id="96d1c-117">C++</span></span>

<span data-ttu-id="96d1c-118">Consultez fonction [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .</span><span class="sxs-lookup"><span data-stu-id="96d1c-118">See [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d1c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96d1c-119">Requirements</span></span>



| <span data-ttu-id="96d1c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96d1c-120">Requirement</span></span> | <span data-ttu-id="96d1c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="96d1c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96d1c-122">Version</span><span class="sxs-lookup"><span data-stu-id="96d1c-122">Version</span></span><br/> | <span data-ttu-id="96d1c-123">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="96d1c-123">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="96d1c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="96d1c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="96d1c-125"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d1c-125"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="96d1c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="96d1c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="96d1c-127"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96d1c-127"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
