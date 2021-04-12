---
description: Obtient les statistiques du récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Attribut MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528257"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="b507d-103">Attribut des statistiques de \_ MP2DLNA MF \_</span><span class="sxs-lookup"><span data-stu-id="b507d-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="b507d-104">Obtient les statistiques du récepteur multimédia DLNA (Digital vivant Network Alliance).</span><span class="sxs-lookup"><span data-stu-id="b507d-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="b507d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b507d-105">Data type</span></span>

<span data-ttu-id="b507d-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stocké en tant qu' **octet \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b507d-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="b507d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="b507d-107">Get/set</span></span>

<span data-ttu-id="b507d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="b507d-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="b507d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b507d-109">Remarks</span></span>

<span data-ttu-id="b507d-110">Pendant la diffusion en continu, le récepteur multimédia DLNA met à jour cet attribut avec des statistiques sur l’encodage et le multiplexage des flux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="b507d-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="b507d-111">L’application peut interroger cet attribut à tout moment pour obtenir les valeurs les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="b507d-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="b507d-112">La définition de cet attribut sur le récepteur multimédia DLNA n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="b507d-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b507d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b507d-113">Requirements</span></span>



| <span data-ttu-id="b507d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b507d-114">Requirement</span></span> | <span data-ttu-id="b507d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b507d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b507d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b507d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b507d-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b507d-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b507d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b507d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b507d-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b507d-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b507d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b507d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b507d-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="b507d-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b507d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b507d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b507d-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b507d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




