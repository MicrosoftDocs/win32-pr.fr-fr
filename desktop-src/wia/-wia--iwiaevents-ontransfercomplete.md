---
description: Événement qui se produit lorsqu’un transfert de données est effectué avec succès.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Événement WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202897"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="da913-103">Événement WIA. OnTransferComplete</span><span class="sxs-lookup"><span data-stu-id="da913-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="da913-104">Événement qui se produit lorsqu’un transfert de données est effectué avec succès.</span><span class="sxs-lookup"><span data-stu-id="da913-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="da913-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da913-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="da913-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da913-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da913-107">*Item*</span><span class="sxs-lookup"><span data-stu-id="da913-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="da913-108">Objet [**Item**](-wia-item.md) transféré.</span><span class="sxs-lookup"><span data-stu-id="da913-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="da913-109">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="da913-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="da913-110">Chemin d’accès et nom de fichier de l’image transférée.</span><span class="sxs-lookup"><span data-stu-id="da913-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da913-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da913-111">Return value</span></span>

<span data-ttu-id="da913-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="da913-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da913-113">Notes</span><span class="sxs-lookup"><span data-stu-id="da913-113">Remarks</span></span>

<span data-ttu-id="da913-114">WIA notifie le script ou l’application lorsqu’un transfert de données, une image ou un son se termine correctement.</span><span class="sxs-lookup"><span data-stu-id="da913-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="da913-115">Implémentez la sous-routine **objWia** \_ **OnTransferComplete ()** pour autoriser votre script ou votre application à répondre à l’achèvement du transfert de données.</span><span class="sxs-lookup"><span data-stu-id="da913-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="da913-116">Par exemple, vous souhaiterez peut-être qu’un script affiche une image après son transfert.</span><span class="sxs-lookup"><span data-stu-id="da913-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="da913-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da913-117">Requirements</span></span>



| <span data-ttu-id="da913-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da913-118">Requirement</span></span> | <span data-ttu-id="da913-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="da913-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da913-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da913-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da913-121">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da913-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da913-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da913-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da913-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da913-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="da913-124">DLL</span><span class="sxs-lookup"><span data-stu-id="da913-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da913-125"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="da913-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




