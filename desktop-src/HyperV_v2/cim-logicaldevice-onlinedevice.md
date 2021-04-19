---
description: La méthode OnlineDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Méthode OnlineDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536408"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="91de8-103">Méthode OnlineDevice de la \_ classe du LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="91de8-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="91de8-104">La méthode **OnlineDevice** a été dépréciée à la place de la méthode **RequestStateChange** plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="91de8-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91de8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91de8-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="91de8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91de8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91de8-107">*En ligne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91de8-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91de8-108">Si la **valeur est true**, mettre l’appareil en ligne, si la valeur est **false**, mettre l’appareil hors connexion.</span><span class="sxs-lookup"><span data-stu-id="91de8-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91de8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91de8-109">Return value</span></span>

<span data-ttu-id="91de8-110">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="91de8-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="91de8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91de8-111">Requirements</span></span>



| <span data-ttu-id="91de8-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91de8-112">Requirement</span></span> | <span data-ttu-id="91de8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="91de8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91de8-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91de8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="91de8-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="91de8-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="91de8-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91de8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="91de8-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="91de8-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="91de8-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91de8-118">Namespace</span></span><br/>                | <span data-ttu-id="91de8-119">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="91de8-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="91de8-120">MOF</span><span class="sxs-lookup"><span data-stu-id="91de8-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91de8-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91de8-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91de8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="91de8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91de8-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91de8-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="91de8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91de8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91de8-125">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="91de8-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




