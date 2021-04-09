---
description: Spécifie si une Media Foundation transformation (MFT) est inscrite uniquement dans le processus d’application.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Attribut MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753941"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="7b92d-103">Attribut de l' \_ \_ attribut local du processus MFT \_</span><span class="sxs-lookup"><span data-stu-id="7b92d-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="7b92d-104">Spécifie si une Media Foundation transformation (MFT) est inscrite uniquement dans le processus de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b92d-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="7b92d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7b92d-105">Data type</span></span>

<span data-ttu-id="7b92d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7b92d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7b92d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7b92d-107">Get/set</span></span>

<span data-ttu-id="7b92d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7b92d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7b92d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7b92d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b92d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7b92d-110">Remarks</span></span>

<span data-ttu-id="7b92d-111">Cet attribut est utilisé comme suit :</span><span class="sxs-lookup"><span data-stu-id="7b92d-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="7b92d-112">L’application inscrit une table MFT locale en appelant la fonction [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="7b92d-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="7b92d-113">Ces fonctions inscrivent la table MFT dans le processus de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b92d-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="7b92d-114">La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) est appelée pour énumérer les MFTS qui correspondent à un ensemble de critères particulier.</span><span class="sxs-lookup"><span data-stu-id="7b92d-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="7b92d-115">L’application peut appeler la fonction **MFTEnumEx** directement, mais cette fonction est plus souvent appelée par le chargeur de topologie.</span><span class="sxs-lookup"><span data-stu-id="7b92d-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="7b92d-116">La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) récupère un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , chacun représentant un objet d’activation pour une table MFT.</span><span class="sxs-lookup"><span data-stu-id="7b92d-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="7b92d-117">Si une table MFT est inscrite localement, l’attribut de l' \_ attribut local de processus MFT a la valeur \_ \_ **true** sur l’objet d’activation correspondant.</span><span class="sxs-lookup"><span data-stu-id="7b92d-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="7b92d-118">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="7b92d-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="7b92d-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7b92d-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b92d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b92d-120">Requirements</span></span>



| <span data-ttu-id="7b92d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b92d-121">Requirement</span></span> | <span data-ttu-id="7b92d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b92d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b92d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b92d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7b92d-124">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b92d-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7b92d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b92d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7b92d-126">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b92d-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7b92d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b92d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b92d-128"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b92d-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b92d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b92d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b92d-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b92d-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7b92d-131">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="7b92d-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




