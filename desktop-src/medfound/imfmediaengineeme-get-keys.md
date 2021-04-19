---
description: Obtient l’objet de clés multimédia associé au moteur multimédia ou null s’il n’y a pas d’objet de clés multimédia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMFMediaEngineEME :: get_Keys, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524778"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="0f05f-103">IMFMediaEngineEME :: méthode d’extraction de \_ clés</span><span class="sxs-lookup"><span data-stu-id="0f05f-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="0f05f-104">Obtient l’objet de clés multimédia associé au moteur multimédia ou **null** s’il n’y a pas d’objet de clés multimédia.</span><span class="sxs-lookup"><span data-stu-id="0f05f-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f05f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f05f-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="0f05f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f05f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f05f-107">*légende*</span><span class="sxs-lookup"><span data-stu-id="0f05f-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05f-108">L’objet de clés multimédia associé au moteur multimédia ou **null** s’il n’existe pas d’objet de clés multimédia.</span><span class="sxs-lookup"><span data-stu-id="0f05f-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f05f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f05f-109">Return value</span></span>

<span data-ttu-id="0f05f-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f05f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f05f-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f05f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f05f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f05f-112">Requirements</span></span>



| <span data-ttu-id="0f05f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f05f-113">Requirement</span></span> | <span data-ttu-id="0f05f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f05f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f05f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f05f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0f05f-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f05f-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0f05f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f05f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0f05f-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f05f-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0f05f-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="0f05f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f05f-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f05f-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f05f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f05f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f05f-122">**IMFMediaEngineEME**</span><span class="sxs-lookup"><span data-stu-id="0f05f-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




