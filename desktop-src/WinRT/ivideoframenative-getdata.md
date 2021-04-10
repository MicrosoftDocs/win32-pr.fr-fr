---
description: Cette méthode retourne une interface qui fournit l’accès aux données vidéo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'IVideoFrameNative :: GetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951181"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="6b365-103">IVideoFrameNative :: GetData, méthode</span><span class="sxs-lookup"><span data-stu-id="6b365-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="6b365-104">Cette méthode retourne une interface qui fournit l’accès aux données vidéo.</span><span class="sxs-lookup"><span data-stu-id="6b365-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b365-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b365-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="6b365-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b365-107">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b365-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b365-108">IID de l’interface à récupérer.</span><span class="sxs-lookup"><span data-stu-id="6b365-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6b365-109">*PPV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b365-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b365-110">Lorsque cette méthode est retournée avec succès, contient le pointeur d’interface demandé dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="6b365-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b365-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b365-111">Return value</span></span>

<span data-ttu-id="6b365-112">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="6b365-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="6b365-113">Retourne E \_ nointerface si l’interface demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6b365-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b365-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b365-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b365-115">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="6b365-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



