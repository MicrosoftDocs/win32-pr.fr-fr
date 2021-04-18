---
description: Les valeurs définissent un type SAP spécifique.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520067"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="fc88e-103">\_type wlx \_ SAS \_ xxx</span><span class="sxs-lookup"><span data-stu-id="fc88e-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="fc88e-104">\[La constante WLX de \_ \_ type SAS \_ xxx n’est plus disponible pour une utilisation à partir de Windows Server 2008 et Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="fc88e-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="fc88e-105">Les valeurs de **\_ type SAS wlx \_ \_ xxx** définissent un type SAP spécifique.</span><span class="sxs-lookup"><span data-stu-id="fc88e-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="fc88e-106">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc88e-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="fc88e-107">Toutes les valeurs comprises entre zéro et 127 sont réservées pour les types définis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fc88e-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="fc88e-108">Les valeurs supérieures à 127 sont disponibles pour les types définis par le client.</span><span class="sxs-lookup"><span data-stu-id="fc88e-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="fc88e-109">Les types suivants sont passés aux fonctions qui ont un paramètre *dwSasType* .</span><span class="sxs-lookup"><span data-stu-id="fc88e-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="fc88e-110">Constante</span><span class="sxs-lookup"><span data-stu-id="fc88e-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="fc88e-111">Description</span><span class="sxs-lookup"><span data-stu-id="fc88e-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="fc88e-112"><dt>**WLX \_ \_ type SAS \_ CTRL \_ Alt \_ Suppr**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="fc88e-113">Indique qu’un utilisateur a tapé la combinaison de touches CTRL + ALT + SUPPR standard.</span><span class="sxs-lookup"><span data-stu-id="fc88e-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="fc88e-114"><dt>**WLX \_ de \_ type SAS \_ SC \_ Insert**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="fc88e-115">Indique qu’une [*carte à puce*](../secgloss/s-gly.md) a été insérée dans un appareil compatible.</span><span class="sxs-lookup"><span data-stu-id="fc88e-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="fc88e-116"><dt>**\_type SAS \_ wlx \_ SC \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="fc88e-117">Indique qu’une carte à puce a été supprimée d’un appareil compatible.</span><span class="sxs-lookup"><span data-stu-id="fc88e-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="fc88e-118"><dt>**\_ \_ activité SCRNSVR du type SAS \_ wlx \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="fc88e-119">Indique que l’activité du clavier ou de la souris s’est produite alors qu’un économiseur d’écran sécurisé était actif.</span><span class="sxs-lookup"><span data-stu-id="fc88e-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="fc88e-120"><dt>**\_ \_ \_ \_ délai d’expiration du type SAS wlx SCRNSVR**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="fc88e-121">Indique que l’activation de l’économiseur d’écran s’est produite en raison de l’inactivité du clavier et de la souris.</span><span class="sxs-lookup"><span data-stu-id="fc88e-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="fc88e-122"><dt>**\_ \_ \_ délai d’expiration du type SAS wlx**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="fc88e-123">Indique qu’aucune entrée utilisateur n’a été reçue dans le délai d’attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="fc88e-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="fc88e-124"><dt>**\_déconnexion \_ utilisateur du type SAS \_ wlx \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="fc88e-125">Indique que l’utilisateur est déconnecté du système.</span><span class="sxs-lookup"><span data-stu-id="fc88e-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="fc88e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc88e-126">Requirements</span></span>



| <span data-ttu-id="fc88e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc88e-127">Requirement</span></span> | <span data-ttu-id="fc88e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc88e-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc88e-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc88e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fc88e-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc88e-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc88e-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc88e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fc88e-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc88e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fc88e-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fc88e-133">End of client support</span></span><br/>    | <span data-ttu-id="fc88e-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc88e-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="fc88e-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fc88e-135">End of server support</span></span><br/>    | <span data-ttu-id="fc88e-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc88e-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="fc88e-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc88e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc88e-138"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc88e-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
