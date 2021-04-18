---
title: Structure WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: La \_ structure d’état de l’individualisation WM \_ contient des informations sur un processus d’individualisation en attente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Structure WM_INDIVIDUALIZE_STATUS format Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533071"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a><span data-ttu-id="17230-104">Structure WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="17230-104">WM_INDIVIDUALIZE_STATUS structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="17230-105">La structure d’état de l' **\_ \_ individualisation WM** contient des informations sur un processus d’individualisation en attente.</span><span class="sxs-lookup"><span data-stu-id="17230-105">The **WM\_INDIVIDUALIZE\_STATUS** structure holds information about a pending individualization process.</span></span>

## <a name="syntax"></a><span data-ttu-id="17230-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17230-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="17230-107">Membres</span><span class="sxs-lookup"><span data-stu-id="17230-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="17230-108">**heure(s)**</span><span class="sxs-lookup"><span data-stu-id="17230-108">**hr**</span></span>
</dt> <dd>

<span data-ttu-id="17230-109">Code de retour **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17230-109">**HRESULT** return code.</span></span>

</dd> <dt>

<span data-ttu-id="17230-110">**enIndiStatus**</span><span class="sxs-lookup"><span data-stu-id="17230-110">**enIndiStatus**</span></span>
</dt> <dd>

<span data-ttu-id="17230-111">Valeur du type d’énumération de l’état de l' [**\_ \_ individualisation DRM**](drmdrm-individualization-status.md) qui indique l’état actuel du processus d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="17230-111">Value from the [**DRM\_INDIVIDUALIZATION\_STATUS**](drmdrm-individualization-status.md) enumeration type that indicates the current status of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="17230-112">**pszIndiRespUrl**</span><span class="sxs-lookup"><span data-stu-id="17230-112">**pszIndiRespUrl**</span></span>
</dt> <dd>

<span data-ttu-id="17230-113">Pointeur vers une chaîne se terminant par un caractère NULL contenant l’URL de réponse d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="17230-113">Pointer to a null-terminated string containing the individualization response URL.</span></span>

</dd> <dt>

<span data-ttu-id="17230-114">**dwHTTPRequest**</span><span class="sxs-lookup"><span data-stu-id="17230-114">**dwHTTPRequest**</span></span>
</dt> <dd>

<span data-ttu-id="17230-115">Nombre d’allers-retours HTTP vers le service d’individualisation qui ont été effectués.</span><span class="sxs-lookup"><span data-stu-id="17230-115">The number of HTTP round trips to the individualization service that have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="17230-116">**enHTTPStatus**</span><span class="sxs-lookup"><span data-stu-id="17230-116">**enHTTPStatus**</span></span>
</dt> <dd>

<span data-ttu-id="17230-117">Valeur du type d’énumération de l' [**\_ \_ État http DRM**](drmdrm-http-status.md) .</span><span class="sxs-lookup"><span data-stu-id="17230-117">Value from the [**DRM\_HTTP\_STATUS**](drmdrm-http-status.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="17230-118">**dwHTTPReadProgress**</span><span class="sxs-lookup"><span data-stu-id="17230-118">**dwHTTPReadProgress**</span></span>
</dt> <dd>

<span data-ttu-id="17230-119">Nombre d’octets téléchargés.</span><span class="sxs-lookup"><span data-stu-id="17230-119">The number of bytes downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="17230-120">**dwHTTPReadTotal**</span><span class="sxs-lookup"><span data-stu-id="17230-120">**dwHTTPReadTotal**</span></span>
</dt> <dd>

<span data-ttu-id="17230-121">Nombre total d’octets à télécharger.</span><span class="sxs-lookup"><span data-stu-id="17230-121">The total number of bytes to be downloaded.</span></span> <span data-ttu-id="17230-122">Vous pouvez utiliser cette valeur et **dwHTTPReadProgress** pour afficher une interface utilisateur indiquant la quantité de téléchargement terminée et la quantité restante à effectuer.</span><span class="sxs-lookup"><span data-stu-id="17230-122">You can use this value and **dwHTTPReadProgress** to display a user interface indicating how much of the download has completed and how much remains to be done.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17230-123">Notes</span><span class="sxs-lookup"><span data-stu-id="17230-123">Remarks</span></span>

<span data-ttu-id="17230-124">Cette structure est reçue lorsque vous appelez la méthode [**IWMDRMIndividualizationStatus :: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="17230-124">This structure is received when you call the [**IWMDRMIndividualizationStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md) method.</span></span> <span data-ttu-id="17230-125">Elle contient l’état du processus d’individualisation en attente au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="17230-125">It contains the status of the pending individualization process at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="17230-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17230-126">Requirements</span></span>



| <span data-ttu-id="17230-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17230-127">Requirement</span></span> | <span data-ttu-id="17230-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="17230-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17230-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="17230-129">Header</span></span><br/> | <dl> <span data-ttu-id="17230-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="17230-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17230-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17230-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17230-132">**Structures**</span><span class="sxs-lookup"><span data-stu-id="17230-132">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





