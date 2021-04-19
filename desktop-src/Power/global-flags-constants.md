---
description: Les constantes d’indicateurs globales sont utilisées pour activer ou désactiver les options de stratégie d’alimentation utilisateur.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Constantes d’indicateurs globales (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529830"
---
# <a name="global-flags-constants"></a><span data-ttu-id="71990-103">Constantes d’indicateurs globaux</span><span class="sxs-lookup"><span data-stu-id="71990-103">Global Flags Constants</span></span>

<span data-ttu-id="71990-104">Les constantes d’indicateurs globales sont utilisées pour activer ou désactiver les options de stratégie d’alimentation utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71990-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="71990-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="71990-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="71990-106">Description</span><span class="sxs-lookup"><span data-stu-id="71990-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="71990-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="71990-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="71990-108">Active ou désactive l’affichage de plusieurs batteries dans le compteur d’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="71990-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="71990-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="71990-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="71990-110">Active ou désactive la connexion au mot de passe lorsque le système sort du mode veille ou veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="71990-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="71990-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="71990-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="71990-112">Active ou désactive l’icône compteur de batterie dans la barre d’état système.</span><span class="sxs-lookup"><span data-stu-id="71990-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="71990-113">Lorsque cet indicateur est désactivé, l’icône compteur de batterie ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="71990-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="71990-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="71990-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="71990-115">Active ou désactive la prise en charge de la mise en grisé de l’affichage vidéo lorsque le système passe d’une alimentation secteur à une batterie.</span><span class="sxs-lookup"><span data-stu-id="71990-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="71990-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="71990-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="71990-117">Active ou désactive la prise en charge de l’éveil par appel.</span><span class="sxs-lookup"><span data-stu-id="71990-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="71990-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71990-118">Requirements</span></span>



| <span data-ttu-id="71990-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71990-119">Requirement</span></span> | <span data-ttu-id="71990-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="71990-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71990-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71990-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71990-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71990-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="71990-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71990-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71990-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71990-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71990-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="71990-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="71990-126"><dt>PowrProf. h</dt></span><span class="sxs-lookup"><span data-stu-id="71990-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71990-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71990-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71990-128">**\_ \_ stratégie d’alimentation des utilisateurs globaux \_**</span><span class="sxs-lookup"><span data-stu-id="71990-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




