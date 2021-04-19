---
description: Crée un objet de session de clé multimédia à l’aide des données d’initialisation et des données personnalisées spécifiées. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMFMediaKeys :: CreateSession, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531254"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="ca3a6-104">IMFMediaKeys :: CreateSession, méthode</span><span class="sxs-lookup"><span data-stu-id="ca3a6-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="ca3a6-105">Crée un objet de session de clé multimédia à l’aide des données d’initialisation et des données personnalisées spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="ca3a6-106">.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca3a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca3a6-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="ca3a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca3a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca3a6-109">*mimeType*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-110">Type MIME du conteneur multimédia utilisé pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-112">Données d’initialisation du système de clés.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-113">*libéré*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-114">Nombre, en octets, *initData*.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-115">*customData*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-116">Données personnalisées envoyées au système de clés.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-117">*cbCustomData*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-118">Nombre, en octets, de *cbCustomData*.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-119">*indiquer*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-120">indiquer</span><span class="sxs-lookup"><span data-stu-id="ca3a6-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="ca3a6-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="ca3a6-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="ca3a6-122">Session de la clé du média.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca3a6-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca3a6-123">Return value</span></span>

<span data-ttu-id="ca3a6-124">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ca3a6-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ca3a6-125">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca3a6-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca3a6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca3a6-126">Requirements</span></span>



| <span data-ttu-id="ca3a6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca3a6-127">Requirement</span></span> | <span data-ttu-id="ca3a6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca3a6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca3a6-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca3a6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ca3a6-130">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca3a6-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca3a6-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca3a6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ca3a6-132">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca3a6-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ca3a6-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="ca3a6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca3a6-134"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca3a6-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca3a6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca3a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca3a6-136">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="ca3a6-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




