---
title: IAMWMBufferPassCallback méthode Notify
description: La méthode Notify est appelée par le code confidentiel pour chaque mémoire tampon qui est fournie pendant la diffusion en continu.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Méthode notifier le format Windows Media
- Méthode Notify Windows Media format, interface IAMWMBufferPassCallback
- Interface IAMWMBufferPassCallback Windows Media format, méthode Notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f362262b36dee0bfc9a18e57010d102b2fa2cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102144"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a><span data-ttu-id="8274a-106">IAMWMBufferPassCallback :: Notify, méthode</span><span class="sxs-lookup"><span data-stu-id="8274a-106">IAMWMBufferPassCallback::Notify method</span></span>

<span data-ttu-id="8274a-107">La méthode **Notify** est appelée par le code confidentiel pour chaque mémoire tampon qui est fournie pendant la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="8274a-107">The **Notify** method is called by the pin for each buffer that is delivered during streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="8274a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8274a-108">Syntax</span></span>


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="8274a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8274a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8274a-110">*pNSSBuffer3* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8274a-110">*pNSSBuffer3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8274a-111">Pointeur vers l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) exposée sur l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="8274a-111">Pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface exposed on the media sample.</span></span>

</dd> <dt>

<span data-ttu-id="8274a-112">*pPin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8274a-112">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8274a-113">Pointeur vers le code confidentiel associé au flux multimédia auquel l’exemple appartient.</span><span class="sxs-lookup"><span data-stu-id="8274a-113">Pointer to the pin associated with the media stream that the sample belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="8274a-114">*prtStart* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8274a-114">*prtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8274a-115">Heure de début de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="8274a-115">Start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="8274a-116">*prtEnd* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8274a-116">*prtEnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8274a-117">Heure de fin de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="8274a-117">End time of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8274a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8274a-118">Return value</span></span>

<span data-ttu-id="8274a-119">Aucune valeur de retour particulière n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8274a-119">No particular return value is specified.</span></span> <span data-ttu-id="8274a-120">Le code PIN appelant ignore le **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8274a-120">The calling pin ignores the **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8274a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8274a-121">Remarks</span></span>

<span data-ttu-id="8274a-122">Cette méthode permet à une application d’examiner et d’agir sur les informations de la mémoire tampon du média avant le traitement du contenu de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8274a-122">This method enables an application to examine and act on information in the media buffer before the buffer contents are processed.</span></span> <span data-ttu-id="8274a-123">L’application est chargée de connaître le type de média sur le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="8274a-123">The application is responsible for knowing the media type on the pin.</span></span> <span data-ttu-id="8274a-124">Ces informations peuvent être obtenues en obtenant d’abord les informations de flux à partir du profil, puis en appelant la méthode [**IConfigAsfWriter2 :: StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) pour déterminer quel pin est associé à chaque flux.</span><span class="sxs-lookup"><span data-stu-id="8274a-124">This information can be obtained by first getting the stream information from the profile and then calling [**IConfigAsfWriter2::StreamNumFromPin**](iconfigasfwriter2-streamnumfrompin.md) method to determine which pin is associated with each stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="8274a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8274a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8274a-126">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="8274a-126">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="8274a-127">**Interface IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="8274a-127">**IAMWMBufferPassCallback Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[<span data-ttu-id="8274a-128">**Interface INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="8274a-128">**INSSBuffer3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 