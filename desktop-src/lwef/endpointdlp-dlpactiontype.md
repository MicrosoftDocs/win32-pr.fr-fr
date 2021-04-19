---
description: Spécifie le type d’action d’une opération de protection contre la perte de données (DLP) de point de terminaison.
title: Énumération DlpActionType (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495777"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="66326-103">Énumération DlpActionType</span><span class="sxs-lookup"><span data-stu-id="66326-103">DlpActionType enumeration</span></span>

<span data-ttu-id="66326-104">Spécifie le type d’action d’une opération de protection contre la perte de données (DLP) de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="66326-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="66326-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66326-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="66326-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="66326-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66326-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="66326-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="66326-108">Opération de copie sur un support amovible.</span><span class="sxs-lookup"><span data-stu-id="66326-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="66326-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="66326-110">Opération de copie dans un dossier réseau partagé.</span><span class="sxs-lookup"><span data-stu-id="66326-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="66326-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="66326-112">Opération de copie dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="66326-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="66326-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="66326-114">Une opération d’impression.</span><span class="sxs-lookup"><span data-stu-id="66326-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="66326-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="66326-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="66326-116">Opération de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="66326-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="66326-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="66326-118">Opération effectuée par une application non autorisée.</span><span class="sxs-lookup"><span data-stu-id="66326-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="66326-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="66326-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="66326-120">Opération ciblée vers un emplacement du Cloud.</span><span class="sxs-lookup"><span data-stu-id="66326-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="66326-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="66326-122">Opération qui comprend l’accès par une application Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="66326-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="66326-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="66326-124">Opération qui comprend l’accès par un bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="66326-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="66326-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="66326-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="66326-126">Valeur maximale de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="66326-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="66326-127">Notes</span><span class="sxs-lookup"><span data-stu-id="66326-127">Remarks</span></span>

<span data-ttu-id="66326-128">Les valeurs de cette énumération sont utilisées par la structure [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="66326-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="66326-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="66326-129">Requirements</span></span>



| <span data-ttu-id="66326-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66326-130">Requirement</span></span>          |    <span data-ttu-id="66326-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="66326-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66326-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66326-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66326-133">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="66326-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

