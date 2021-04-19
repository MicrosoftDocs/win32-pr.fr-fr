---
title: Méthode IMediaRenderer IsAudioSupported
description: Récupère une valeur qui indique si DMR peut lire du contenu audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API de diffusion multimédia en continu de méthode IsAudioSupported
- API de diffusion multimédia en continu de méthode IsAudioSupported, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511248"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="1d720-106">IMediaRenderer :: IsAudioSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="1d720-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="1d720-107">Récupère une valeur qui indique si DMR peut lire du contenu audio.</span><span class="sxs-lookup"><span data-stu-id="1d720-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d720-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d720-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1d720-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d720-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d720-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d720-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d720-111">Valeur booléenne qui est **true** si DMR est capable de diffuser du contenu audio et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="1d720-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d720-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d720-112">Return value</span></span>

<span data-ttu-id="1d720-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1d720-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1d720-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1d720-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1d720-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1d720-115">Return code</span></span>                                                                          | <span data-ttu-id="1d720-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d720-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1d720-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d720-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1d720-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d720-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1d720-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d720-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d720-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="1d720-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





