---
title: Objet de transcrypteur DRM
description: Objet de transcrypteur DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- Kit de développement logiciel (SDK) Windows Media format, objets de transchiffrement DRM
- ASF (Advanced Systems Format), objets de transchiffrement DRM
- ASF (format des systèmes avancés), objets de transchiffrement DRM
- objets, objets de transcrypteur DRM
- Objets de transcrypteur DRM
- Windows Media Format SDK, transcryptor Objects
- ASF (Advanced Systems Format), objets de transcrypteur
- ASF (format des systèmes avancés), objets de transchiffreur
- objets, transchiffrer des objets
- objets de transchiffreur
- gestion des droits numériques (DRM), objets de transchiffreur
- DRM (gestion des droits numériques), objets de transchiffreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46213dd7ebfbe48ff22039c201dbff3aab462f5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101269"
---
# <a name="drm-transcryptor-object"></a><span data-ttu-id="b3d5f-115">Objet de transcrypteur DRM</span><span class="sxs-lookup"><span data-stu-id="b3d5f-115">DRM Transcryptor Object</span></span>

<span data-ttu-id="b3d5f-116">L’objet de conversion DRM convertit les fichiers ASF protégés par DRM en flux de données prêts à être envoyés aux périphériques réseau qui utilisent Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="b3d5f-116">The DRM transcryptor object converts DRM-protected ASF files into data streams ready to be sent to network devices that use Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="b3d5f-117">L’objet de transcrypteur DRM est créé par la fonction [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) , qui définit un pointeur vers l’interface [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) .</span><span class="sxs-lookup"><span data-stu-id="b3d5f-117">The DRM transcryptor object is created by the [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) function, which sets a pointer to the [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) interface.</span></span> <span data-ttu-id="b3d5f-118">**IUnknown** et **IWMDRMTranscryptor** sont les seules interfaces prises en charge par cet objet.</span><span class="sxs-lookup"><span data-stu-id="b3d5f-118">**IUnknown** and **IWMDRMTranscryptor** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3d5f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3d5f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3d5f-120">**Objets**</span><span class="sxs-lookup"><span data-stu-id="b3d5f-120">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




