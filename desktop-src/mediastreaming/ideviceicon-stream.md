---
title: IDeviceIcon, méthode de flux
description: Récupère l’icône sous la forme d’un flux.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- API de diffusion multimédia en continu de méthode de flux
- API de diffusion multimédia en continu de méthode de flux, interface IDeviceIcon
- API de diffusion multimédia en continu de l’interface IDeviceIcon, méthode Stream
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315084"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="c9479-106">IDeviceIcon :: Stream, méthode</span><span class="sxs-lookup"><span data-stu-id="c9479-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="c9479-107">Récupère l’icône sous la forme d’un flux.</span><span class="sxs-lookup"><span data-stu-id="c9479-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9479-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9479-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="c9479-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9479-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9479-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9479-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9479-111">Reçoit une référence à un [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) qui peut être utilisé pour récupérer les données d’image.</span><span class="sxs-lookup"><span data-stu-id="c9479-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9479-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9479-112">Return value</span></span>

<span data-ttu-id="c9479-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9479-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9479-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9479-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9479-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c9479-115">Return code</span></span>                                                                          | <span data-ttu-id="c9479-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9479-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9479-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9479-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9479-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9479-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c9479-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9479-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9479-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="c9479-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

