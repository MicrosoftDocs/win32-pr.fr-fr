---
description: Envoyé par le filtre de lecteur ASF WM lorsqu’il lit des fichiers ASF protégés par la gestion des droits numériques (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540356"
---
# <a name="ec_wmt_event-dshowh"></a><span data-ttu-id="3d06c-103">EC_WMT_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="3d06c-103">EC_WMT_EVENT (Dshow.h)</span></span>

<span data-ttu-id="3d06c-104">Envoyé par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) lorsqu’il lit des fichiers ASF protégés par la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="3d06c-104">Sent by the [WM ASF Reader](wm-asf-reader-filter.md) filter when it reads ASF files protected by digital rights management (DRM).</span></span>

## <a name="parameters"></a><span data-ttu-id="3d06c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d06c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d06c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3d06c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3d06c-107">Une des valeurs d' **\_ État WMT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d06c-107">One of the following **WMT\_STATUS** values:</span></span>



| <span data-ttu-id="3d06c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d06c-108">Value</span></span>                         | <span data-ttu-id="3d06c-109">Description</span><span class="sxs-lookup"><span data-stu-id="3d06c-109">Description</span></span>                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d06c-110">\_licence d’acquisition WMT \_</span><span class="sxs-lookup"><span data-stu-id="3d06c-110">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="3d06c-111">Envoyé lorsque le composant DRM a terminé le processus d’acquisition de licence, soit avec succès, soit sans succès.</span><span class="sxs-lookup"><span data-stu-id="3d06c-111">Sent when the DRM component has completed the license acquisition process, either successfully or unsuccessfully.</span></span> |
| <span data-ttu-id="3d06c-112">\_personnalisable WMT</span><span class="sxs-lookup"><span data-stu-id="3d06c-112">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="3d06c-113">Le processus de mise à niveau de sécurité est terminé, soit avec succès, soit sans succès.</span><span class="sxs-lookup"><span data-stu-id="3d06c-113">The security upgrade process has completed, either successfully or unsuccessfully.</span></span>                                |
| <span data-ttu-id="3d06c-114">WMT \_ a besoin d’une \_ individualisation</span><span class="sxs-lookup"><span data-stu-id="3d06c-114">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="3d06c-115">Le fichier requiert qu’une application reçoive une mise à niveau de sécurité avant d’effectuer l’action demandée.</span><span class="sxs-lookup"><span data-stu-id="3d06c-115">The file requires that an application receive a security upgrade before performing the requested action.</span></span>          |
| <span data-ttu-id="3d06c-116">WMT \_ aucun \_ droit</span><span class="sxs-lookup"><span data-stu-id="3d06c-116">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="3d06c-117">L’application ne dispose pas des droits nécessaires pour exécuter l’action demandée sur un fichier protégé par DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="3d06c-117">The application has no rights to perform he requested action on a file protected by DRM version 1.</span></span>                |
| <span data-ttu-id="3d06c-118">WMT \_ aucun \_ droit \_ ex</span><span class="sxs-lookup"><span data-stu-id="3d06c-118">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="3d06c-119">L’application ne dispose pas des droits nécessaires pour exécuter l’action demandée sur un fichier protégé par DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="3d06c-119">The application has no rights to perform he requested action on a file protected by DRM version 7.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="3d06c-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3d06c-120"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3d06c-121">Pointeur vers une structure de [**\_ données d' \_ événement \_ « am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) » qui contient des informations sur l’événement ou la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3d06c-121">Pointer to an [**AM\_WMT\_EVENT\_DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) structure that contains information about the event, or **NULL**.</span></span> <span data-ttu-id="3d06c-122">Le membre **pData** de cette structure pointe vers des données supplémentaires, dont le type dépend de la valeur de **lParam1**, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3d06c-122">The **pData** member of this structure points to additional data, whose type depends on the value of **lParam1**, as shown in the following table.</span></span>



| <span data-ttu-id="3d06c-123">lParam1</span><span class="sxs-lookup"><span data-stu-id="3d06c-123">lParam1</span></span>                       | <span data-ttu-id="3d06c-124">\_Données d' \_ événement WMT am \_ . pdata</span><span class="sxs-lookup"><span data-stu-id="3d06c-124">AM\_WMT\_EVENT\_DATA.pData</span></span>                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d06c-125">\_licence d’acquisition WMT \_</span><span class="sxs-lookup"><span data-stu-id="3d06c-125">WMT\_ACQUIRE\_LICENSE</span></span>         | <span data-ttu-id="3d06c-126">Pointeur vers une structure de [**\_ \_ \_ données de licence WM**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="3d06c-126">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span> <span data-ttu-id="3d06c-127">Cette structure est documentée dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3d06c-127">This structure is documented in the Windows Media Format SDK.</span></span> |
| <span data-ttu-id="3d06c-128">\_personnalisable WMT</span><span class="sxs-lookup"><span data-stu-id="3d06c-128">WMT\_INDIVIDUALIZE</span></span>            | <span data-ttu-id="3d06c-129">Pointeur désignant une structure d’état de l' [**\_ \_ individualisation WM**](/windows/desktop/wmformat/wm-individualize-status) .</span><span class="sxs-lookup"><span data-stu-id="3d06c-129">Pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](/windows/desktop/wmformat/wm-individualize-status) structure.</span></span>                                                        |
| <span data-ttu-id="3d06c-130">WMT \_ a besoin d’une \_ individualisation</span><span class="sxs-lookup"><span data-stu-id="3d06c-130">WMT\_NEEDS\_INDIVIDUALIZATION</span></span> | <span data-ttu-id="3d06c-131">**Valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3d06c-131">**NULL**.</span></span>                                                                                                                                        |
| <span data-ttu-id="3d06c-132">WMT \_ aucun \_ droit</span><span class="sxs-lookup"><span data-stu-id="3d06c-132">WMT\_NO\_RIGHTS</span></span>               | <span data-ttu-id="3d06c-133">Pointeur vers une chaîne de caractères larges contenant une URL de Challenge.</span><span class="sxs-lookup"><span data-stu-id="3d06c-133">Pointer to a wide-character string containing a challenge URL.</span></span>                                                                                   |
| <span data-ttu-id="3d06c-134">WMT \_ aucun \_ droit \_ ex</span><span class="sxs-lookup"><span data-stu-id="3d06c-134">WMT\_NO\_RIGHTS\_EX</span></span>           | <span data-ttu-id="3d06c-135">Pointeur vers une structure de [**\_ \_ \_ données de licence WM**](/windows/desktop/wmformat/wm-get-license-data) .</span><span class="sxs-lookup"><span data-stu-id="3d06c-135">Pointer to a [**WM\_GET\_LICENSE\_DATA**](/windows/desktop/wmformat/wm-get-license-data) structure.</span></span>                                                               |



 

<span data-ttu-id="3d06c-136">La valeur de *lParam2* peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="3d06c-136">The value of *lParam2* might be **NULL**.</span></span> <span data-ttu-id="3d06c-137">Vérifiez la valeur avant de déréférencer le pointeur.</span><span class="sxs-lookup"><span data-stu-id="3d06c-137">Check the value before dereferencing the pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d06c-138">Notes</span><span class="sxs-lookup"><span data-stu-id="3d06c-138">Remarks</span></span>

<span data-ttu-id="3d06c-139">Pour plus d’informations sur l’activation de la lecture de fichiers protégés par DRM, consultez la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="3d06c-139">See the Windows Media Format SDK documentation for more information on enabling playback of DRM-protected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d06c-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d06c-140">Requirements</span></span>



| <span data-ttu-id="3d06c-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d06c-141">Requirement</span></span> | <span data-ttu-id="3d06c-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d06c-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d06c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d06c-143">Header</span></span><br/> | <dl> <span data-ttu-id="3d06c-144"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d06c-144"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d06c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d06c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d06c-146">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="3d06c-146">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3d06c-147">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d06c-147">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

