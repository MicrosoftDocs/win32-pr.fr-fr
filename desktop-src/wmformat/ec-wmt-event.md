---
title: EC_WMT_EVENT (kit de développement logiciel (SDK) Windows Media format 11)
description: '\_événement EC WMT \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Kit de développement logiciel (SDK) Windows Media format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- gestion des droits numériques (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
- ASF (format avancé des systèmes), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464067"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a><span data-ttu-id="1e666-110">EC_WMT_EVENT (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="1e666-110">EC_WMT_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="1e666-111">Envoyé par le kit de développement logiciel (SDK) de format Windows Media lorsqu’une application utilise le filtre de lecteur ASF pour lire des fichiers ASF protégés par la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="1e666-111">Sent by the Windows Media Format SDK when an application uses the ASF Reader filter to play ASF files protected by digital rights management (DRM).</span></span>

<span data-ttu-id="1e666-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e666-112">Parameters</span></span>

<span data-ttu-id="1e666-113">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1e666-113">*lParam1*</span></span>

<span data-ttu-id="1e666-114">Il peut s’agir de l’une des valeurs d’État WMT suivantes \_ .</span><span class="sxs-lookup"><span data-stu-id="1e666-114">Can be one of the following WMT\_STATUS values.</span></span>



| <span data-ttu-id="1e666-115">\_Message d’État WMT</span><span class="sxs-lookup"><span data-stu-id="1e666-115">WMT\_STATUS Message</span></span>           | <span data-ttu-id="1e666-116">Description</span><span class="sxs-lookup"><span data-stu-id="1e666-116">Description</span></span>                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e666-117">WMT \_ aucun \_ droit</span><span class="sxs-lookup"><span data-stu-id="1e666-117">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="1e666-118">Le fichier est protégé par la version 1 de DRM et l’application n’a aucun droit pour effectuer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="1e666-118">The file is protected with DRM version 1 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="1e666-119">\_licence d’acquisition WMT \_</span><span class="sxs-lookup"><span data-stu-id="1e666-119">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="1e666-120">Le processus d’acquisition de licence est terminé.</span><span class="sxs-lookup"><span data-stu-id="1e666-120">The license acquisition process has been completed.</span></span> <span data-ttu-id="1e666-121">(Cela ne signifie pas nécessairement qu’une licence a été acquise avec succès.)</span><span class="sxs-lookup"><span data-stu-id="1e666-121">(This does not necessarily mean that a license was successfully acquired.)</span></span> |
| <span data-ttu-id="1e666-122">WMT \_ aucun \_ droit \_ ex</span><span class="sxs-lookup"><span data-stu-id="1e666-122">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="1e666-123">Le fichier est protégé par la version 7 de DRM et l’application ne dispose pas des droits nécessaires pour exécuter l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="1e666-123">The file is protected with DRM version 7 and the application has no rights to perform the requested action.</span></span>                    |
| <span data-ttu-id="1e666-124">WMT \_ a besoin d’une \_ individualisation</span><span class="sxs-lookup"><span data-stu-id="1e666-124">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="1e666-125">La licence autorise uniquement les applications individuelles à exécuter l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="1e666-125">The license allows only individualized applications to perform the requested action.</span></span>                                           |
| <span data-ttu-id="1e666-126">\_personnalisable WMT</span><span class="sxs-lookup"><span data-stu-id="1e666-126">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="1e666-127">Le processus d’individualisation est en cours d’exécution ou terminé.</span><span class="sxs-lookup"><span data-stu-id="1e666-127">The individualization process is now being performed or has been completed.</span></span>                                                    |



 

<span data-ttu-id="1e666-128">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1e666-128">*lParam2*</span></span>

<span data-ttu-id="1e666-129">Pointeur vers une structure de **données d’événement « am \_ \_ \_ WMT** » qui contient des informations sur l’événement dans le pointeur de membre **pData** , ainsi qu’un code d’état **HRESULT** envoyé par le kit de développement logiciel (SDK) de format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1e666-129">Pointer to an **AM\_WMT\_EVENT\_DATA** structure that contains information about the event in the **pData** member pointer, as well as an **HRESULT** status code sent by the Windows Media Format SDK.</span></span> <span data-ttu-id="1e666-130">La valeur de *lParam2* dépend de la valeur de *lParam1*, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1e666-130">The value of *lParam2* depends on the value of *lParam1*, as described in the following table.</span></span> <span data-ttu-id="1e666-131">(Les structures « WM \_ » sont définies dans le kit de développement logiciel (SDK) du format Windows Media.)</span><span class="sxs-lookup"><span data-stu-id="1e666-131">(The "WM\_" structures are defined in the Windows Media Format SDK.)</span></span>



| <span data-ttu-id="1e666-132">Si lParam1 est...</span><span class="sxs-lookup"><span data-stu-id="1e666-132">If lParam1 is...</span></span>              | <span data-ttu-id="1e666-133">\_Données d' \_ événement WMT am \_ . pdata est...</span><span class="sxs-lookup"><span data-stu-id="1e666-133">AM\_WMT\_EVENT\_DATA.pData is...</span></span>                            |
|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="1e666-134">WMT \_ aucun \_ droit</span><span class="sxs-lookup"><span data-stu-id="1e666-134">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="1e666-135">Pointeur vers une chaîne **WCHAR** contenant une URL de Challenge.</span><span class="sxs-lookup"><span data-stu-id="1e666-135">A pointer to a **WCHAR** string containing a challenge URL.</span></span> |
| <span data-ttu-id="1e666-136">\_licence d’acquisition WMT \_</span><span class="sxs-lookup"><span data-stu-id="1e666-136">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="1e666-137">Pointeur vers une structure **de \_ \_ \_ données de licence WM** .</span><span class="sxs-lookup"><span data-stu-id="1e666-137">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="1e666-138">WMT \_ aucun \_ droit \_ ex</span><span class="sxs-lookup"><span data-stu-id="1e666-138">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="1e666-139">Pointeur vers une structure **de \_ \_ \_ données de licence WM** .</span><span class="sxs-lookup"><span data-stu-id="1e666-139">A pointer to a **WM\_GET\_LICENSE\_DATA** structure.</span></span>        |
| <span data-ttu-id="1e666-140">WMT \_ a besoin d’une \_ individualisation</span><span class="sxs-lookup"><span data-stu-id="1e666-140">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="1e666-141">NULL.</span><span class="sxs-lookup"><span data-stu-id="1e666-141">NULL.</span></span>                                                       |
| <span data-ttu-id="1e666-142">\_personnalisable WMT</span><span class="sxs-lookup"><span data-stu-id="1e666-142">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="1e666-143">Pointeur vers une structure d’état de l' **\_ \_ individualisation WM** .</span><span class="sxs-lookup"><span data-stu-id="1e666-143">A pointer to a **WM\_INDIVIDUALIZE\_STATUS** structure.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="1e666-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e666-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e666-145">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="1e666-145">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1e666-146">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="1e666-146">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="1e666-147">**Activation de la prise en charge de DRM**</span><span class="sxs-lookup"><span data-stu-id="1e666-147">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




