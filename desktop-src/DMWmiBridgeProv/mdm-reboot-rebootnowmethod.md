---
title: Méthode RebootNowMethod de la classe MDM_Reboot
description: Cette méthode exécute un redémarrage de l’appareil.
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- Méthode RebootNowMethod
- Méthode RebootNowMethod, classe MDM_Reboot
- Classe MDM_Reboot, méthode RebootNowMethod
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102961"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="8e73f-106">Méthode RebootNowMethod de la \_ classe de redémarrage MDM</span><span class="sxs-lookup"><span data-stu-id="8e73f-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="8e73f-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8e73f-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8e73f-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8e73f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8e73f-109">Cette méthode exécute un redémarrage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8e73f-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="8e73f-110">Voir aussi [RebootNow](/windows/client-management/mdm/reboot-csp).</span><span class="sxs-lookup"><span data-stu-id="8e73f-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e73f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e73f-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="8e73f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e73f-112">Parameters</span></span>

<span data-ttu-id="8e73f-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8e73f-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e73f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e73f-114">Requirements</span></span>



| <span data-ttu-id="8e73f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e73f-115">Requirement</span></span> | <span data-ttu-id="8e73f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e73f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e73f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e73f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e73f-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e73f-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8e73f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e73f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e73f-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e73f-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8e73f-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8e73f-121">Namespace</span></span><br/>                | <span data-ttu-id="8e73f-122">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8e73f-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="8e73f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="8e73f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e73f-124"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e73f-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="8e73f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8e73f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e73f-126"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e73f-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e73f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e73f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e73f-128">**Redémarrage MDM \_**</span><span class="sxs-lookup"><span data-stu-id="8e73f-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 

