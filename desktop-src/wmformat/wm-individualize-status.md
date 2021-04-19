---
title: Structure WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: La \_ \_ structure d’état de l’individualisation WM enregistre l’état du processus d’individualisation.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Structure WM_INDIVIDUALIZE_STATUS format Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510552"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a><span data-ttu-id="804c0-104">Structure WM_INDIVIDUALIZE_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="804c0-104">WM_INDIVIDUALIZE_STATUS structure (Drmexternals.h)</span></span>

<span data-ttu-id="804c0-105">La structure d’état de l' **\_ individualisation \_ WM** enregistre l’état du processus d' [*individualisation*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="804c0-105">The **WM\_INDIVIDUALIZE\_STATUS** structure records the status of the [*individualization*](wmformat-glossary.md) process.</span></span>

## <a name="syntax"></a><span data-ttu-id="804c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="804c0-106">Syntax</span></span>


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a><span data-ttu-id="804c0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="804c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="804c0-108">**heure(s)**</span><span class="sxs-lookup"><span data-stu-id="804c0-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-109">Code de retour **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="804c0-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="804c0-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="804c0-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-111">Valeur du type d’énumération de l’état de l' [**\_ \_ individualisation DRM**](drm-individualization-status.md) .</span><span class="sxs-lookup"><span data-stu-id="804c0-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drm-individualization-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="804c0-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="804c0-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-113">Pointeur vers une chaîne se terminant par un caractère NULL contenant l’URL de réponse d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="804c0-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="804c0-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="804c0-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-115">**Valeur DWORD** qui indique le nombre d’allers-retours http vers le service d’individualisation qui ont été effectués..</span><span class="sxs-lookup"><span data-stu-id="804c0-115">**DWORD** that indicates the number of HTTP round trips to the individualization service that have been completed..</span></span>

</dd> <dt>

<span data-ttu-id="804c0-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="804c0-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-117">Valeur du type d’énumération de l' [**\_ \_ État http DRM**](drm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="804c0-117">Value from the [**DRM\_HTTP\_STATUS**](drm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="804c0-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="804c0-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-119">**Valeur DWORD** contenant le nombre d’octets téléchargés jusqu’à présent..</span><span class="sxs-lookup"><span data-stu-id="804c0-119">**DWORD** containing the number of bytes downloaded until now..</span></span>

</dd> <dt>

<span data-ttu-id="804c0-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="804c0-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="804c0-121">**Valeur DWORD** contenant le nombre total d’octets à télécharger.</span><span class="sxs-lookup"><span data-stu-id="804c0-121">**DWORD** containing the total number of bytes to be downloaded.</span></span> <span data-ttu-id="804c0-122">Utilisez cette valeur et **dwHTTPReadProgress** pour afficher une interface utilisateur indiquant la quantité de téléchargement terminée et la quantité restante à effectuer.</span><span class="sxs-lookup"><span data-stu-id="804c0-122">Use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="804c0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="804c0-123">Remarks</span></span>

<span data-ttu-id="804c0-124">Cette structure est remplie par les composants d’exécution DRM et est envoyée aux applications dans le paramètre *pValue* de la méthode applications [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) lorsque l’événement est égal à WMT \_ Individual.</span><span class="sxs-lookup"><span data-stu-id="804c0-124">This structure is filled in by the DRM run-time components and is sent to applications in the *pValue* parameter of the applications [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method when the event equals WMT\_INDIVIDUALIZE.</span></span> <span data-ttu-id="804c0-125">L’application reçoit cet événement plusieurs fois pendant le processus de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="804c0-125">The application receives this event multiple times during the download process.</span></span>

## <a name="requirements"></a><span data-ttu-id="804c0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="804c0-126">Requirements</span></span>



| <span data-ttu-id="804c0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="804c0-127">Requirement</span></span> | <span data-ttu-id="804c0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="804c0-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="804c0-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804c0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="804c0-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="804c0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="804c0-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="804c0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="804c0-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="804c0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="804c0-133">Version</span><span class="sxs-lookup"><span data-stu-id="804c0-133">Version</span></span><br/>                  | <span data-ttu-id="804c0-134">SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="804c0-134">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="804c0-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="804c0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="804c0-136"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="804c0-136"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804c0-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="804c0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804c0-138">**\_État http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="804c0-138">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="804c0-139">**Structures**</span><span class="sxs-lookup"><span data-stu-id="804c0-139">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





