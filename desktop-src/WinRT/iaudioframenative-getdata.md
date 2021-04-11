---
description: Cette méthode retourne une interface qui fournit l’accès aux données audio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'IAudioFrameNative :: GetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113122"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="9ab76-103">IAudioFrameNative :: GetData, méthode</span><span class="sxs-lookup"><span data-stu-id="9ab76-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="9ab76-104">Cette méthode retourne une interface qui fournit l’accès aux données audio.</span><span class="sxs-lookup"><span data-stu-id="9ab76-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab76-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ab76-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="9ab76-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ab76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab76-107">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ab76-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab76-108">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="9ab76-108">Type: **REFIID**</span></span>

<span data-ttu-id="9ab76-109">IID de l’interface à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9ab76-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9ab76-110">*PPV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9ab76-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ab76-111">Tapez : \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="9ab76-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="9ab76-112">Lorsque cette méthode est retournée avec succès, contient le pointeur d’interface demandé dans _riid paramètre.</span><span class="sxs-lookup"><span data-stu-id="9ab76-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab76-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ab76-113">Return value</span></span>

<span data-ttu-id="9ab76-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ab76-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ab76-115">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9ab76-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="9ab76-116">Retourne E \_ nointerface si l’interface demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9ab76-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ab76-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ab76-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab76-118">**IAudioFrameNative**</span><span class="sxs-lookup"><span data-stu-id="9ab76-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



