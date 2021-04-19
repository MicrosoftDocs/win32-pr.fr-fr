---
description: Transmet une valeur de clé avec toutes les données associées requises par le module de déchiffrement du contenu pour le système de clé donné.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'IMFMediaKeySession :: Update, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538263"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="fc2ae-103">IMFMediaKeySession :: Update, méthode</span><span class="sxs-lookup"><span data-stu-id="fc2ae-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="fc2ae-104">Transmet une valeur de clé avec toutes les données associées requises par le module de déchiffrement du contenu pour le système de clé donné.</span><span class="sxs-lookup"><span data-stu-id="fc2ae-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc2ae-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="fc2ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc2ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2ae-107">*key*</span><span class="sxs-lookup"><span data-stu-id="fc2ae-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="fc2ae-108">*libéré*</span><span class="sxs-lookup"><span data-stu-id="fc2ae-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2ae-109">Nombre, en octets, de la *clé*.</span><span class="sxs-lookup"><span data-stu-id="fc2ae-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2ae-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc2ae-110">Return value</span></span>

<span data-ttu-id="fc2ae-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fc2ae-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc2ae-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fc2ae-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2ae-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc2ae-113">Requirements</span></span>



| <span data-ttu-id="fc2ae-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc2ae-114">Requirement</span></span> | <span data-ttu-id="fc2ae-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2ae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2ae-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2ae-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2ae-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc2ae-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc2ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2ae-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc2ae-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fc2ae-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="fc2ae-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc2ae-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ae-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2ae-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc2ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2ae-123">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="fc2ae-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




