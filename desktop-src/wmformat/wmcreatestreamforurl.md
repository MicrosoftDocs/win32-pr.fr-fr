---
title: WMCreateStreamForURL fonction)
description: La fonction WMCreateStreamForURL est implémentée par l’application pour créer un objet COM IStream pour une URL donnée.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- WMCreateStreamForURL fonction Windows Media format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380843"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="78fe2-104">WMCreateStreamForURL fonction)</span><span class="sxs-lookup"><span data-stu-id="78fe2-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="78fe2-105">La fonction **WMCreateStreamForURL** est implémentée par l’application pour créer un objet com **ISTREAM** pour une URL donnée.</span><span class="sxs-lookup"><span data-stu-id="78fe2-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fe2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78fe2-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="78fe2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78fe2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fe2-108">*pwszURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78fe2-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fe2-109">Pointeur vers une chaîne de caractères larges contenant l’URL.</span><span class="sxs-lookup"><span data-stu-id="78fe2-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="78fe2-110">*pfCorrectSource* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="78fe2-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78fe2-111">Pointeur vers un indicateur, true empêchera le kit de développement logiciel (SDK) d’essayer d’autres plug-ins sources pour cette URL.</span><span class="sxs-lookup"><span data-stu-id="78fe2-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="78fe2-112">*PPStream* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="78fe2-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78fe2-113">Pointeur vers un pointeur vers l’objet **IStream** créé par la méthode.</span><span class="sxs-lookup"><span data-stu-id="78fe2-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fe2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78fe2-114">Return value</span></span>

<span data-ttu-id="78fe2-115">Si la fonction est réussie, elle doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78fe2-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="78fe2-116">En cas d’échec, il doit retourner un code d’erreur **HRESULT** approprié, et \* *PPStream* doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="78fe2-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="78fe2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78fe2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fe2-118">**Plug-ins sources**</span><span class="sxs-lookup"><span data-stu-id="78fe2-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




