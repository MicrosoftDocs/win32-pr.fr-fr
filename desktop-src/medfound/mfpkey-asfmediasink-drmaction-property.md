---
description: Spécifie comment le récepteur de média ASF doit appliquer Windows Media DRM.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761479"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="0db21-103">MFPKEY \_ ASFMEDIASINK \_ DRMACTION, propriété</span><span class="sxs-lookup"><span data-stu-id="0db21-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="0db21-104">Spécifie comment le récepteur de média ASF doit appliquer Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="0db21-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="0db21-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0db21-105">Data type</span></span>

<span data-ttu-id="0db21-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0db21-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0db21-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0db21-107">PROPVARIANT member</span></span>

<span data-ttu-id="0db21-108">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="0db21-108">**ULONG**</span></span>

<span data-ttu-id="0db21-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="0db21-109">VT\_UI4</span></span>

<span data-ttu-id="0db21-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="0db21-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0db21-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0db21-111">Remarks</span></span>

<span data-ttu-id="0db21-112">La valeur de cette propriété est un membre de l’énumération [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .</span><span class="sxs-lookup"><span data-stu-id="0db21-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="0db21-113">Vous pouvez utiliser cet attribut pour configurer le récepteur multimédia ASF.</span><span class="sxs-lookup"><span data-stu-id="0db21-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="0db21-114">L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :</span><span class="sxs-lookup"><span data-stu-id="0db21-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="0db21-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): interroge le pointeur [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) récupéré pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="0db21-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="0db21-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) spécifié dans le paramètre *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="0db21-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db21-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0db21-117">Requirements</span></span>



| <span data-ttu-id="0db21-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0db21-118">Requirement</span></span> | <span data-ttu-id="0db21-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0db21-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0db21-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db21-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0db21-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0db21-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0db21-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db21-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0db21-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0db21-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0db21-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0db21-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db21-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db21-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db21-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0db21-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db21-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0db21-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
