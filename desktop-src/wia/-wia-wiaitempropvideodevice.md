---
description: Le pilote vidéo d’acquisition d’images Windows (WIA) standard (wiavusd.dll) prend en charge les propriétés suivantes pour la diffusion en continu de périphériques vidéo.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propriété d’appareil vidéo WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113259"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="a78c0-103">Constantes de propriété d’appareil vidéo WIA</span><span class="sxs-lookup"><span data-stu-id="a78c0-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="a78c0-104">Le pilote vidéo d’acquisition d’images Windows (WIA) standard (wiavusd.dll) prend en charge les propriétés suivantes pour la diffusion en continu de périphériques vidéo.</span><span class="sxs-lookup"><span data-stu-id="a78c0-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="a78c0-105">WIA ne prend pas en charge les périphériques vidéo dans Windows Server 2003, Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a78c0-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="a78c0-106">Pour ces versions de Windows, utilisez [DirectShow](/previous-versions//ms783323(v=vs.85)) pour acquérir des images à partir d’une vidéo.</span><span class="sxs-lookup"><span data-stu-id="a78c0-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="a78c0-107">Le préfixe « WIA \_ DPV \_ » indique une propriété d’appareil pour les périphériques vidéo et est la Convention d’affectation de noms utilisée dans C/C++.</span><span class="sxs-lookup"><span data-stu-id="a78c0-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="a78c0-108">À des fins de script, ces constantes utilisent le préfixe « VideoDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="a78c0-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="a78c0-109">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a78c0-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="a78c0-110">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="a78c0-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="a78c0-111">Description</span><span class="sxs-lookup"><span data-stu-id="a78c0-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="a78c0-112"><dt>**WIA \_ \_Dernière \_ image \_**</dt> de la DPV <dt>VideoDeviceLastPictureTaken</dt></span><span class="sxs-lookup"><span data-stu-id="a78c0-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="a78c0-113">Cette propriété est utilisée pour informer le pilote WIA qu’une nouvelle image a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="a78c0-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="a78c0-114">Les applications doivent définir la valeur de cette propriété sur le nom du fichier image créé à la suite d’un appel réussi à la méthode [**IWiaVideo :: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) .</span><span class="sxs-lookup"><span data-stu-id="a78c0-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="a78c0-115">Type : VT \_ BSTR, Access : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a78c0-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="a78c0-116"><dt>**WIA \_ \_ \_ Répertoire d’images de DPV**</dt> <dt>VideoDeviceImagesDirectory</dt></span><span class="sxs-lookup"><span data-stu-id="a78c0-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="a78c0-117">Cette propriété est exposée par le pilote en mode utilisateur vidéo WIA standard (wiavusd.dll).</span><span class="sxs-lookup"><span data-stu-id="a78c0-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="a78c0-118">La valeur de cette propriété est le chemin d’accès complet du répertoire dans lequel le pilote vidéo WIA place les images par défaut.</span><span class="sxs-lookup"><span data-stu-id="a78c0-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="a78c0-119">Les applications doivent définir la propriété [**IWiaVideo :: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) sur cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a78c0-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="a78c0-120">Type : VT \_ BSTR, Access : lecture seule</span><span class="sxs-lookup"><span data-stu-id="a78c0-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="a78c0-121"><dt>**WIA \_ \_ \_ \_ Chemin de l’appareil DPV DShow**</dt> <dt>VideoDeviceDShowDevicePath</dt></span><span class="sxs-lookup"><span data-stu-id="a78c0-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="a78c0-122">Chemin d’accès complet de l’appareil DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a78c0-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="a78c0-123">Type : VT \_ BSTR, Access : lecture seule</span><span class="sxs-lookup"><span data-stu-id="a78c0-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="a78c0-124"><dt>**WIA \_ \_ \_ Point de montage DPF**</dt> <dt>FileDeviceMountPoint</dt></span><span class="sxs-lookup"><span data-stu-id="a78c0-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="a78c0-125">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="a78c0-125">Not implemented.</span></span> <br/> <span data-ttu-id="a78c0-126">Type : **VT \_ I4**, accès : lecture seule, valeurs valides : [WIA \_ prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="a78c0-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="a78c0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a78c0-127">Requirements</span></span>



| <span data-ttu-id="a78c0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a78c0-128">Requirement</span></span> | <span data-ttu-id="a78c0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a78c0-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a78c0-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78c0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a78c0-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a78c0-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a78c0-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78c0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a78c0-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a78c0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a78c0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a78c0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a78c0-135"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a78c0-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
