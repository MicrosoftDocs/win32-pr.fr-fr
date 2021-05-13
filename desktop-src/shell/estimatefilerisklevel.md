---
description: Estime le risque d’exécution de code inconnu lorsqu’un gestionnaire est appelé sur un fichier donné. Ce risque est basé sur une compréhension du gestionnaire et le contenu du code du fichier.
title: EstimateFileRiskLevel fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841430"
---
# <a name="estimatefilerisklevel-function"></a><span data-ttu-id="e3c4e-104">EstimateFileRiskLevel fonction)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-104">EstimateFileRiskLevel function</span></span>

<span data-ttu-id="e3c4e-105">\[Cette fonction est disponible sur Windows XP avec Service Pack 2 (SP2) par le biais de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-105">\[This function is available on Windows XP with Service Pack 2 (SP2) through Windows Vista.</span></span> <span data-ttu-id="e3c4e-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="e3c4e-107">À la place, les applications clientes doivent utiliser [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) pour présenter un environnement utilisateur qui permet de télécharger et d’échanger des fichiers en toute sécurité via des pièces jointes de messagerie électronique et de messagerie.\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-107">Client applications instead should use [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) to present a user environment that provides safe download and exchange of files through email and messaging attachments.\]</span></span>

<span data-ttu-id="e3c4e-108">Estime le risque d’exécution de code inconnu lorsqu’un gestionnaire est appelé sur un fichier donné.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-108">Estimates the risk of executing unknown code when a handler is called on a given file.</span></span> <span data-ttu-id="e3c4e-109">Ce risque est basé sur une compréhension du gestionnaire et le contenu du code du fichier.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-109">This risk is based on an understanding of the handler and the code content of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c4e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3c4e-110">Syntax</span></span>


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a><span data-ttu-id="e3c4e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3c4e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c4e-112">*pszFilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-112">*pszFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c4e-113">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e3c4e-113">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e3c4e-114">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès du fichier qui est vérifié par rapport au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-114">A pointer to a null-terminated string that contains the path of the file that is being checked against the handler.</span></span>

</dd> <dt>

<span data-ttu-id="e3c4e-115">*pszExt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-115">*pszExt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c4e-116">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e3c4e-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e3c4e-117">Pointeur vers une chaîne terminée par le caractère null qui contient l’extension du fichier qui est vérifié, avec ou sans son point de début.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-117">A pointer to a null-terminated string that contains the extension of the file that is being checked, either with or without its leading period.</span></span> <span data-ttu-id="e3c4e-118">Par exemple, « . txt » ou « txt ».</span><span class="sxs-lookup"><span data-stu-id="e3c4e-118">For instance, ".txt" or "txt".</span></span>

</dd> <dt>

<span data-ttu-id="e3c4e-119">*pszHandler* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-119">*pszHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c4e-120">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e3c4e-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e3c4e-121">Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès du gestionnaire pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-121">A pointer to a null-terminated string that contains the path of the handler for the file.</span></span>

</dd> <dt>

<span data-ttu-id="e3c4e-122">*pfrlEstimate* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-122">*pfrlEstimate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3c4e-123">Type : **fichier \_ \_ niveau \* de risque**</span><span class="sxs-lookup"><span data-stu-id="e3c4e-123">Type: **FILE\_RISK\_LEVEL\***</span></span>

<span data-ttu-id="e3c4e-124">Lorsque cette fonction est retournée avec succès, contient un pointeur vers l’une des valeurs suivantes qui indique le risque estimé.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-124">When this function returns successfully, contains a pointer to one of the following values that state the estimated risk.</span></span>

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span data-ttu-id="e3c4e-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ AUCUN \_ avis** (0)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-125"><span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL\_NO\_OPINION** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e3c4e-126">Le format du fichier n’est pas identifié ou le gestionnaire n’est pas identifié.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-126">The format of the file is not identified or the handler is not identified.</span></span> <span data-ttu-id="e3c4e-127">Informations insuffisantes pour obtenir une réponse pertinente.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-127">Insufficient information available for a meaningful answer.</span></span>

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span data-ttu-id="e3c4e-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ FAIBLE** (1)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-128"><span id="FRL_LOW"></span><span id="frl_low"></span>**FRL\_LOW** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e3c4e-129">Le format du fichier est entièrement compris, le gestionnaire est connu et il est très sûr qu’aucun code superflu ne soit exécuté.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-129">The format of the file is completely understood, the handler is known, and there is high confidence that no extraneous code will be executed.</span></span>

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span data-ttu-id="e3c4e-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODÉRÉ** (2)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-130"><span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL\_MODERATE** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3c4e-131">Le format du fichier est identifié, mais il n’est pas suffisamment compréhensible pour l’étiquetage comme un risque élevé ou faible.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-131">The format of the file is identified, but it is not sufficiently understood to label as either a high or low risk.</span></span>

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span data-ttu-id="e3c4e-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ÉLEVÉ** (3)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-132"><span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL\_HIGH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e3c4e-133">Le format de fichier est compris et les facteurs de risque élevés ont été identifiés.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-133">The file format is understood and elevated risk factors have been identified.</span></span>

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span data-ttu-id="e3c4e-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOC** (4)</span><span class="sxs-lookup"><span data-stu-id="e3c4e-134"><span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL\_BLOCK** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e3c4e-135">Le format de fichier est spécifiquement bloqué pour ce gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-135">The file format is specifically blocked for this handler.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c4e-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e3c4e-136">Return value</span></span>

<span data-ttu-id="e3c4e-137">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3c4e-137">Type: **HRESULT**</span></span>

<span data-ttu-id="e3c4e-138">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-138">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3c4e-139">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3c4e-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c4e-140">Notes</span><span class="sxs-lookup"><span data-stu-id="e3c4e-140">Remarks</span></span>

<span data-ttu-id="e3c4e-141">Cette fonction n’est pas déclarée dans un en-tête public ou incluse dans un fichier de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-141">This function is not declared in a public header or included in a library file.</span></span> <span data-ttu-id="e3c4e-142">Pour l’utiliser, vous devez la charger directement à partir de Winshfhc.dll par l’ordinal 101.</span><span class="sxs-lookup"><span data-stu-id="e3c4e-142">To use it you must load it directly from Winshfhc.dll by ordinal 101.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c4e-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3c4e-143">Requirements</span></span>



| <span data-ttu-id="e3c4e-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3c4e-144">Requirement</span></span> | <span data-ttu-id="e3c4e-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3c4e-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c4e-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3c4e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c4e-147">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3c4e-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3c4e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e3c4e-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3c4e-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3c4e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e3c4e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3c4e-151"><dt>Winshfhc.dll (version 5,1 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e3c4e-151"><dt>Winshfhc.dll (version 5.1 or later)</dt></span></span> </dl> |



 

 




