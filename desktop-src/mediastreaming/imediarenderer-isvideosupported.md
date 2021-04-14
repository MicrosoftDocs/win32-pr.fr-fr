---
title: Méthode IMediaRenderer IsVideoSupported
description: Récupère une valeur qui indique si DMR peut lire du contenu vidéo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API de diffusion multimédia en continu de méthode IsVideoSupported
- API de diffusion multimédia en continu de méthode IsVideoSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313000"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="64654-106">IMediaRenderer :: IsVideoSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="64654-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="64654-107">Récupère une valeur qui indique si DMR peut lire du contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="64654-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="64654-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64654-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="64654-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64654-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="64654-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64654-111">Valeur booléenne qui est **true** si DMR est capable de visionner du contenu vidéo et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="64654-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64654-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64654-112">Return value</span></span>

<span data-ttu-id="64654-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="64654-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64654-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64654-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64654-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64654-115">Return code</span></span>                                                                          | <span data-ttu-id="64654-116">Description</span><span class="sxs-lookup"><span data-stu-id="64654-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="64654-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64654-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="64654-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="64654-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="64654-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64654-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64654-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="64654-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





