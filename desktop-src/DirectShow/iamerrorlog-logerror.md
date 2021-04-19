---
description: La méthode LogError journalise une erreur. Les applications n’ont pas besoin d’appeler cette méthode. Elle est appelée en interne en réponse à des erreurs de rendu.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'IAMErrorLog :: LogError, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525208"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="37493-105">IAMErrorLog :: LogError, méthode</span><span class="sxs-lookup"><span data-stu-id="37493-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="37493-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="37493-106">\[Deprecated.</span></span> <span data-ttu-id="37493-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37493-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="37493-108">La méthode **LogError** journalise une erreur.</span><span class="sxs-lookup"><span data-stu-id="37493-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="37493-109">Les applications n’ont pas besoin d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="37493-109">Applications do not need to call this method.</span></span> <span data-ttu-id="37493-110">Elle est appelée en interne en réponse à des erreurs de rendu.</span><span class="sxs-lookup"><span data-stu-id="37493-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="37493-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37493-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="37493-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37493-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37493-113">*Niveau de gravité*</span><span class="sxs-lookup"><span data-stu-id="37493-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="37493-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="37493-114">Reserved.</span></span> <span data-ttu-id="37493-115">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="37493-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="37493-116">*Telle*</span><span class="sxs-lookup"><span data-stu-id="37493-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="37493-117">Valeur de chaîne contenant le texte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="37493-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="37493-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="37493-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="37493-119">Code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="37493-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="37493-120">*signé*</span><span class="sxs-lookup"><span data-stu-id="37493-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="37493-121">Valeur HRESULT qui a été retournée par l’appel de méthode à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="37493-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="37493-122">*pExtraInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37493-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37493-123">Pointeur vers un VARIANT qui contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="37493-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37493-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37493-124">Return value</span></span>

<span data-ttu-id="37493-125">Retourne la valeur du paramètre *HRESULT* .</span><span class="sxs-lookup"><span data-stu-id="37493-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="37493-126">Notes</span><span class="sxs-lookup"><span data-stu-id="37493-126">Remarks</span></span>

<span data-ttu-id="37493-127">Dans cette méthode, ne libérez pas la **variante** vers laquelle pointe *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="37493-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="37493-128">En outre, la **variante** devient non valide après le retour de la méthode, donc n’essayez pas de la référencer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="37493-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="37493-129">Implémentez cette méthode pour retourner le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="37493-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="37493-130">N’effectuez pas d’appels de fonction à l’intérieur de cette méthode qui peut bloquer l’exécution du programme.</span><span class="sxs-lookup"><span data-stu-id="37493-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="37493-131">Par exemple, n’appelez pas les fonctions qui envoient des messages de fenêtre, bloquent les événements ou peuvent bloquer l’exécution.</span><span class="sxs-lookup"><span data-stu-id="37493-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="37493-132">Cela peut entraîner le blocage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="37493-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="37493-133">Pour obtenir la liste des erreurs définies par DES, ainsi que la signification et le type de données de la **variante** vers laquelle pointe *PExtraInfo*, consultez [Erreurs de rendu](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="37493-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="37493-134">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="37493-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="37493-135">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="37493-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="37493-136">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="37493-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37493-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37493-137">Requirements</span></span>



| <span data-ttu-id="37493-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37493-138">Requirement</span></span> | <span data-ttu-id="37493-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="37493-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37493-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="37493-140">Header</span></span><br/>  | <dl> <span data-ttu-id="37493-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="37493-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="37493-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37493-142">Library</span></span><br/> | <dl> <span data-ttu-id="37493-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37493-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37493-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37493-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37493-145">**Interface IAMErrorLog**</span><span class="sxs-lookup"><span data-stu-id="37493-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="37493-146">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="37493-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




