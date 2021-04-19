---
title: GetTSAudioEndpointEnumeratorForSession fonction de rappel
description: Retourne une référence à un énumérateur de point de terminaison audio pour l’ID de session spécifié.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction de rappel GetTSAudioEndpointEnumeratorForSession
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515083"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="d5d27-104">GetTSAudioEndpointEnumeratorForSession fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="d5d27-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="d5d27-105">Retourne une référence à un énumérateur de point de terminaison audio pour l’ID de session spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5d27-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="d5d27-106">Les consommateurs de cet énumérateur de point de terminaison audio, tels que MMDevAPI.dll, appellent cette fonction pour récupérer un énumérateur de point de terminaison audio dans une session Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d5d27-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d27-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d27-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="d5d27-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5d27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d27-109">*SessionID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5d27-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-110">Identificateur de la session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d5d27-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="d5d27-111">*ppEndpointEnumerator* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5d27-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d27-112">Adresse d’un pointeur vers une interface [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="d5d27-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d27-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5d27-113">Return value</span></span>

<span data-ttu-id="d5d27-114">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d5d27-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d27-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d5d27-115">Remarks</span></span>

<span data-ttu-id="d5d27-116">Cette fonction n’est pas définie dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d5d27-116">This function is not defined in a header file.</span></span> <span data-ttu-id="d5d27-117">Vous devez implémenter et exporter cette fonction dans votre énumérateur de point de terminaison personnalisé et utiliser la signature indiquée dans le bloc de syntaxe plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d5d27-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d27-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d27-118">Requirements</span></span>



| <span data-ttu-id="d5d27-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5d27-119">Requirement</span></span> | <span data-ttu-id="d5d27-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5d27-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="d5d27-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d27-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d27-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d27-122">None supported</span></span><br/>         |
| <span data-ttu-id="d5d27-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5d27-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d27-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d5d27-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5d27-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d27-126">Implémentation d’un énumérateur de point de terminaison audio personnalisé</span><span class="sxs-lookup"><span data-stu-id="d5d27-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="d5d27-127">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="d5d27-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

