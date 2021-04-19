---
description: Spécifie la classe du service Planificateur de classes multimédias (MMCSS) pour le thread de décodage.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propriété AVDecMmcss (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544363"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="1ba9b-103">Propriété AVDecMmcss</span><span class="sxs-lookup"><span data-stu-id="1ba9b-103">AVDecMmcss property</span></span>

<span data-ttu-id="1ba9b-104">Spécifie la classe du service Planificateur de classes multimédias (MMCSS) pour le thread de décodage.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="1ba9b-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ba9b-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="1ba9b-106">Data type</span></span>

<span data-ttu-id="1ba9b-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="1ba9b-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1ba9b-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="1ba9b-108">Property GUID</span></span>

<span data-ttu-id="1ba9b-109">**CODECAPI \_ AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="1ba9b-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="1ba9b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1ba9b-110">Property value</span></span>

<span data-ttu-id="1ba9b-111">La valeur de cette propriété est le nom de la classe MMCSS.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba9b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1ba9b-112">Remarks</span></span>

<span data-ttu-id="1ba9b-113">MMCSS permet aux applications de s’assurer que le traitement qui respecte le temps a un accès prioritaire aux ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="1ba9b-114">Il fonctionne en élevant les threads inscrits sur des priorités de thread supérieures tout en diminuant régulièrement leurs priorités afin de transmettre du temps à d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="1ba9b-115">La valeur recommandée pour les décodeurs audio est « audio » et la valeur recommandée pour les décodeurs vidéo est « lecture ».</span><span class="sxs-lookup"><span data-stu-id="1ba9b-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="1ba9b-116">Si le service MMCSS n’est pas disponible ou si la classe MMCSS spécifiée n’existe pas, la définition de la propriété n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1ba9b-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba9b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ba9b-117">Requirements</span></span>



| <span data-ttu-id="1ba9b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ba9b-118">Requirement</span></span> | <span data-ttu-id="1ba9b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ba9b-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba9b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ba9b-120">Header</span></span><br/> | <dl> <span data-ttu-id="1ba9b-121"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba9b-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba9b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ba9b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba9b-123">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="1ba9b-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1ba9b-124">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="1ba9b-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




