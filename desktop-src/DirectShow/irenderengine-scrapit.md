---
description: La méthode ScrapIt ignore le graphique de filtre du moteur de rendu et tous les objets associés.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'IRenderEngine :: ScrapIt, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533225"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="6fa61-103">IRenderEngine :: ScrapIt, méthode</span><span class="sxs-lookup"><span data-stu-id="6fa61-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="6fa61-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6fa61-104">\[Deprecated.</span></span> <span data-ttu-id="6fa61-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fa61-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fa61-106">La `ScrapIt` méthode ignore le graphique de filtre du moteur de rendu et tous les objets associés.</span><span class="sxs-lookup"><span data-stu-id="6fa61-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa61-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fa61-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="6fa61-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fa61-108">Parameters</span></span>

<span data-ttu-id="6fa61-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6fa61-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fa61-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fa61-110">Return value</span></span>

<span data-ttu-id="6fa61-111">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="6fa61-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="6fa61-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6fa61-112">Return code</span></span>                                                                                            | <span data-ttu-id="6fa61-113">Description</span><span class="sxs-lookup"><span data-stu-id="6fa61-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6fa61-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa61-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6fa61-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6fa61-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="6fa61-116"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa61-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="6fa61-117">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="6fa61-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6fa61-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6fa61-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fa61-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6fa61-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fa61-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fa61-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fa61-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6fa61-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fa61-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa61-122">Requirements</span></span>



| <span data-ttu-id="6fa61-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fa61-123">Requirement</span></span> | <span data-ttu-id="6fa61-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fa61-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa61-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fa61-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6fa61-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa61-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fa61-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6fa61-127">Library</span></span><br/> | <dl> <span data-ttu-id="6fa61-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fa61-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa61-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fa61-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa61-130">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="6fa61-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="6fa61-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="6fa61-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




