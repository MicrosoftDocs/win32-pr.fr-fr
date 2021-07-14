---
description: Spécifie le nom de la famille de packages d’application pour une application de configuration de caméra virtuelle.
title: Attribut MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME (Mfapi. h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691860"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a><span data-ttu-id="7c276-103">\_Attribut de \_ \_ nom de famille de package d’application VIRTUALCAMERA \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="7c276-103">MF\_VIRTUALCAMERA\_APP\_PACKAGE\_FAMILY\_NAME attribute</span></span>

<span data-ttu-id="7c276-104">Spécifie le nom de la famille de packages d’application pour une application de configuration de caméra virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7c276-104">Specifies the app package family name for a virtual camera configuration application.</span></span> <span data-ttu-id="7c276-105">lorsqu’il est fourni, le pipeline associe l’application de configuration à la caméra virtuelle et fournit un point de lancement dans la page de Paramètres de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="7c276-105">When provided, the pipeline will associate the configuration application with the virtual camera and provide a launch point within the Camera Settings page.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c276-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="7c276-106">Data type</span></span>

[<span data-ttu-id="7c276-107">MF_ATTRIBUTE_STRING</span><span class="sxs-lookup"><span data-stu-id="7c276-107">MF_ATTRIBUTE_STRING</span></span>](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a><span data-ttu-id="7c276-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c276-108">Remarks</span></span>

<span data-ttu-id="7c276-109">Cet attribut peut être exposé par la source de média personnalisée de la caméra virtuelle à partir du magasin d’attributs sources du média [IMFMediaSourceEx :: GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span><span class="sxs-lookup"><span data-stu-id="7c276-109">This attribute may be exposed by the virtual camera custom media source from the media source attribute store [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).</span></span>  

<span data-ttu-id="7c276-110">Si l’application de configuration n’est pas encore installée sur l’ordinateur, l’application du Windows Store est lancée et naviguée vers la page d’application spécifiée par le nom de la famille de packages.</span><span class="sxs-lookup"><span data-stu-id="7c276-110">If the configuration application is not yet installed on the machine, the Store application will be launched and navigated to the application page specified by the package family name.</span></span> <span data-ttu-id="7c276-111">Dans le cas contraire, l’application installée sera lancée pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c276-111">Otherwise, the installed application will be launched for the user.</span></span>


## <a name="requirements"></a><span data-ttu-id="7c276-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c276-112">Requirements</span></span>



| <span data-ttu-id="7c276-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c276-113">Requirement</span></span> | <span data-ttu-id="7c276-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c276-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c276-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c276-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7c276-116">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="7c276-116">Windows Build 22000</span></span><br/>                          |
| <span data-ttu-id="7c276-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c276-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7c276-118">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="7c276-118">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="7c276-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c276-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c276-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c276-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c276-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c276-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c276-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c276-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c276-123">**IMFAttributes :: GetString**</span><span class="sxs-lookup"><span data-stu-id="7c276-123">**IMFAttributes::GetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="7c276-124">**IMFAttributes :: SetString**</span><span class="sxs-lookup"><span data-stu-id="7c276-124">**IMFAttributes::SetString**</span></span>](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




