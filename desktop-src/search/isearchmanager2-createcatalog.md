---
description: Crée un catalogue personnalisé dans l’indexeur de recherche Windows et retourne une référence à celui-ci.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2 :: CreateCatalog, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201288"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="151b1-103">ISearchManager2 :: CreateCatalog, méthode</span><span class="sxs-lookup"><span data-stu-id="151b1-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="151b1-104">Crée un catalogue personnalisé dans l’indexeur de recherche Windows et retourne une référence à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="151b1-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="151b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="151b1-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="151b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="151b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151b1-107">*pszCatalog* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="151b1-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151b1-108">Type : **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="151b1-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="151b1-109">Nom du catalogue à créer.</span><span class="sxs-lookup"><span data-stu-id="151b1-109">Name of catalog to create.</span></span> <span data-ttu-id="151b1-110">Peut être n’importe quel nom sélectionné par l’appelant, ne doit contenir que des caractères alphanumériques standard et des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="151b1-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="151b1-111">*ppCatalogManager* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="151b1-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="151b1-112">Type : **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="151b1-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="151b1-113">En cas de réussite, une référence au catalogue créé est retournée en tant que pointeur d’interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="151b1-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="151b1-114">La mise en sortie () doit être appelée sur cette interface une fois que l’application appelante a fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="151b1-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151b1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="151b1-115">Return value</span></span>

<span data-ttu-id="151b1-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="151b1-116">Type: **HRESULT**</span></span>

<span data-ttu-id="151b1-117">HRESULT indiquant l’état de l’opération :</span><span class="sxs-lookup"><span data-stu-id="151b1-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="151b1-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="151b1-118">Return code</span></span>                                                                             | <span data-ttu-id="151b1-119">Description</span><span class="sxs-lookup"><span data-stu-id="151b1-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="151b1-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="151b1-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="151b1-121">Le catalogue n’existait pas déjà et a été créé.</span><span class="sxs-lookup"><span data-stu-id="151b1-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="151b1-122">Référence au catalogue renvoyé.</span><span class="sxs-lookup"><span data-stu-id="151b1-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="151b1-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="151b1-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="151b1-124">Le catalogue existait précédemment, la référence au catalogue a été retournée.</span><span class="sxs-lookup"><span data-stu-id="151b1-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="151b1-125">ÉCHEC de HRESULT : échec de la création du catalogue ou des arguments non valides passés.</span><span class="sxs-lookup"><span data-stu-id="151b1-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="151b1-126">Notes</span><span class="sxs-lookup"><span data-stu-id="151b1-126">Remarks</span></span>

<span data-ttu-id="151b1-127">Appelé pour créer un nouveau catalogue dans l’indexeur de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="151b1-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="151b1-128">Après la création, les méthodes sur le gestionnaire de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) retourné peuvent être utilisées pour ajouter des emplacements à indexer, surveiller le processus d’indexation et construire des requêtes à envoyer à l’indexeur et obtenir des résultats.</span><span class="sxs-lookup"><span data-stu-id="151b1-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="151b1-129">Pour plus d’informations, consultez la documentation relative à la gestion de l’index : https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="151b1-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="151b1-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="151b1-130">Requirements</span></span>



| <span data-ttu-id="151b1-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="151b1-131">Requirement</span></span> | <span data-ttu-id="151b1-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="151b1-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="151b1-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="151b1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="151b1-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="151b1-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="151b1-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="151b1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="151b1-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="151b1-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="151b1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="151b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151b1-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="151b1-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
