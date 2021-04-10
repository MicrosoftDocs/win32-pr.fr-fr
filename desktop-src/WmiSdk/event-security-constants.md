---
description: L’exemple suivant montre les constantes de sécurité WMI utilisées pour les événements. Ils sont utilisés pour définir des entrées de contrôle d’accès (ACE) dans les descripteurs de sécurité utilisés pour les événements ou les récepteurs.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Constantes de sécurité d’événement (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115039"
---
# <a name="event-security-constants"></a><span data-ttu-id="3e9b3-104">Constantes de sécurité d’événement</span><span class="sxs-lookup"><span data-stu-id="3e9b3-104">Event Security Constants</span></span>

<span data-ttu-id="3e9b3-105">L’exemple suivant montre les constantes de sécurité WMI utilisées pour les événements.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="3e9b3-106">Ils sont utilisés pour définir des entrées de contrôle d’accès (ACE) dans les descripteurs de sécurité utilisés pour les événements ou les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="3e9b3-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publication WBEM Right \_**</span><span class="sxs-lookup"><span data-stu-id="3e9b3-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b3-108">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="3e9b3-109">Spécifie que le compte peut publier des événements sur l’instance de [**\_ \_ EventFilter**](--eventfilter.md) qui définit le filtre d’événement pour un consommateur permanent.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="3e9b3-110">Disponible dans wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e9b3-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_ \_ s’abonner directement à WBEM**</span><span class="sxs-lookup"><span data-stu-id="3e9b3-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b3-112">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="3e9b3-113">Spécifie qu’un consommateur peut s’abonner aux événements remis à un récepteur.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="3e9b3-114">Utilisé dans [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span><span class="sxs-lookup"><span data-stu-id="3e9b3-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="3e9b3-115">Disponible dans wbemcli. h.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3e9b3-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**les \_ S WBEM sont \_ soumises \_ à \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="3e9b3-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9b3-117">274435 (0x43003)</span><span class="sxs-lookup"><span data-stu-id="3e9b3-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="3e9b3-118">Fournisseur d’événements indique que WMI vérifie la propriété du **\_ descripteur de sécurité** dans chaque événement (hérité de l' [**\_ \_ événement**](--event.md)) et envoie uniquement des événements aux consommateurs avec les autorisations d’accès appropriées.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="3e9b3-119">Disponible dans wbemprov. h.</span><span class="sxs-lookup"><span data-stu-id="3e9b3-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e9b3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e9b3-120">Requirements</span></span>



| <span data-ttu-id="3e9b3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e9b3-121">Requirement</span></span> | <span data-ttu-id="3e9b3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e9b3-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9b3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e9b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9b3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e9b3-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="3e9b3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e9b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9b3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e9b3-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="3e9b3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e9b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e9b3-128"><dt>Wbemcli. h ; </dt> <dt>Wbemprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e9b3-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9b3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e9b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9b3-130">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="3e9b3-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="3e9b3-131">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="3e9b3-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="3e9b3-132">Sécurisation des événements WMI</span><span class="sxs-lookup"><span data-stu-id="3e9b3-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




