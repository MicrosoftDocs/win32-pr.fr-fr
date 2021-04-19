---
description: Crée un gestionnaire de flux d’octets pour la source média MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518560"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="3a295-103">MFCreateMP3ByteStreamPlugin fonction)</span><span class="sxs-lookup"><span data-stu-id="3a295-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="3a295-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="3a295-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="3a295-105">Au lieu de cela, les applications doivent utiliser le programme de [résolution source](source-resolver.md) pour créer la source de média MP3.\]</span><span class="sxs-lookup"><span data-stu-id="3a295-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="3a295-106">Crée un gestionnaire de flux d’octets pour la source média MP3.</span><span class="sxs-lookup"><span data-stu-id="3a295-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a295-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a295-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="3a295-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a295-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a295-109">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a295-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a295-110">Identificateur d'interface (IID) de l'interface demandée.</span><span class="sxs-lookup"><span data-stu-id="3a295-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="3a295-111">Affectez à ce paramètre la valeur **IID \_ IMFByteStreamHandler** pour recevoir un pointeur vers l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="3a295-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3a295-112">*ppvHandler* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3a295-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a295-113">Reçoit un pointeur vers l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a295-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="3a295-114">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="3a295-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a295-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a295-115">Return value</span></span>

<span data-ttu-id="3a295-116">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3a295-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a295-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a295-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a295-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3a295-118">Remarks</span></span>

<span data-ttu-id="3a295-119">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="3a295-119">This function has no associated import library.</span></span> <span data-ttu-id="3a295-120">Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à mf.dll.</span><span class="sxs-lookup"><span data-stu-id="3a295-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a295-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a295-121">Requirements</span></span>



| <span data-ttu-id="3a295-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a295-122">Requirement</span></span> | <span data-ttu-id="3a295-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a295-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a295-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a295-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a295-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a295-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a295-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a295-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a295-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a295-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3a295-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3a295-128">End of client support</span></span><br/>    | <span data-ttu-id="3a295-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a295-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="3a295-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3a295-130">End of server support</span></span><br/>    | <span data-ttu-id="3a295-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a295-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3a295-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a295-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a295-133">Fonctions Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a295-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="3a295-134">Gestionnaires de schémas et gestionnaires de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="3a295-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="3a295-135">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="3a295-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
