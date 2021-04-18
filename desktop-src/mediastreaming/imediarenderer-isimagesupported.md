---
title: Méthode IMediaRenderer IsImageSupported
description: Récupère une valeur qui indique si DMR est capable d’afficher des images.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API de diffusion multimédia en continu de méthode IsImageSupported
- API de diffusion multimédia en continu de méthode IsImageSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509628"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="962ea-106">IMediaRenderer :: IsImageSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="962ea-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="962ea-107">Récupère une valeur qui indique si DMR est capable d’afficher des images.</span><span class="sxs-lookup"><span data-stu-id="962ea-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="962ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="962ea-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="962ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="962ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962ea-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="962ea-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="962ea-111">Valeur booléenne qui est **true** si DMR est capable d’afficher des images et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="962ea-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="962ea-112">Return value</span></span>

<span data-ttu-id="962ea-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="962ea-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="962ea-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="962ea-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="962ea-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="962ea-115">Return code</span></span>                                                                          | <span data-ttu-id="962ea-116">Description</span><span class="sxs-lookup"><span data-stu-id="962ea-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="962ea-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="962ea-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="962ea-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="962ea-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="962ea-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="962ea-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962ea-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="962ea-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





