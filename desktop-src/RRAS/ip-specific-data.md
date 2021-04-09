---
title: Structure de IP_SPECIFIC_DATA (RTM. h)
description: La \_ structure de données spécifique à l’adresse IP contient des données spécifiques à IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- IP_SPECIFIC_DATA de la structure RAS
- Point d’accès RAS du pointeur de structure PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104677"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="bcc35-105">\_Structure de données spécifique à IP \_</span><span class="sxs-lookup"><span data-stu-id="bcc35-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="bcc35-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bcc35-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bcc35-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="bcc35-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bcc35-108">La structure de **\_ données spécifique à l’adresse IP** contient des données spécifiques à IP.</span><span class="sxs-lookup"><span data-stu-id="bcc35-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcc35-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcc35-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="bcc35-110">Membres</span><span class="sxs-lookup"><span data-stu-id="bcc35-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="bcc35-111">**\_Type FSD**</span><span class="sxs-lookup"><span data-stu-id="bcc35-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-112">Spécifie le type de routage tel que défini dans la [norme RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="bcc35-113">Le tableau suivant indique les valeurs possibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="bcc35-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="bcc35-114">Membre</span><span class="sxs-lookup"><span data-stu-id="bcc35-114">Member</span></span>                                                                                               | <span data-ttu-id="bcc35-115">Signification</span><span class="sxs-lookup"><span data-stu-id="bcc35-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="bcc35-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="bcc35-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="bcc35-117">Le type d’itinéraire n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcc35-117">The route type is not specified.</span></span> <span data-ttu-id="bcc35-118">Le type est différent de ceux répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="bcc35-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="bcc35-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="bcc35-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="bcc35-120">L’itinéraire n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bcc35-120">The route is invalid.</span></span> <span data-ttu-id="bcc35-121">Normalement, cette valeur est utilisée pour invalider un itinéraire.</span><span class="sxs-lookup"><span data-stu-id="bcc35-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="bcc35-122">Toutefois, étant donné que l’invalidation n’est pas prise en charge par le gestionnaire de tables de routage, l’itinéraire est toujours pris en compte dans les calculs les mieux routés.</span><span class="sxs-lookup"><span data-stu-id="bcc35-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="bcc35-123">Par conséquent, les protocoles de routage ne doivent pas utiliser cette valeur.</span><span class="sxs-lookup"><span data-stu-id="bcc35-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="bcc35-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="bcc35-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="bcc35-125">L’itinéraire est un itinéraire local, autrement dit, le tronçon suivant est la destination finale.</span><span class="sxs-lookup"><span data-stu-id="bcc35-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="bcc35-126"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="bcc35-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="bcc35-127">L’itinéraire est un itinéraire distant, autrement dit, le tronçon suivant n’est pas la destination finale.</span><span class="sxs-lookup"><span data-stu-id="bcc35-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="bcc35-128">**\_Stratégie FSD**</span><span class="sxs-lookup"><span data-stu-id="bcc35-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-129">Spécifie l’ensemble de conditions qui provoquerait la sélection d’un itinéraire à plusieurs chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="bcc35-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="bcc35-130">Ce membre est généralement au format TOS IP.</span><span class="sxs-lookup"><span data-stu-id="bcc35-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="bcc35-131">Pour plus d’informations, consultez la [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-132">**FSD \_ NextHopAS**</span><span class="sxs-lookup"><span data-stu-id="bcc35-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-133">Spécifie le numéro de système autonome du tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="bcc35-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-134">**\_Priorité FSD**</span><span class="sxs-lookup"><span data-stu-id="bcc35-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-135">Spécifie une valeur métrique.</span><span class="sxs-lookup"><span data-stu-id="bcc35-135">Specifies a metric value.</span></span> <span data-ttu-id="bcc35-136">Le gestionnaire de tables de routage utilise cette valeur pour comparer cette entrée d’itinéraire aux entrées de routage obtenues à partir d’autres protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="bcc35-137">La valeur de ce membre est définie par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-138">**\_Métrique FSD**</span><span class="sxs-lookup"><span data-stu-id="bcc35-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-139">Spécifie une valeur métrique.</span><span class="sxs-lookup"><span data-stu-id="bcc35-139">Specifies a metric value.</span></span> <span data-ttu-id="bcc35-140">Le gestionnaire de tables de routage utilise cette valeur pour comparer cette entrée d’itinéraire à d’autres entrées de routage obtenues à partir du même protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="bcc35-141">La valeur de ce membre est définie par le protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-142">**FSD \_ Metric1**</span><span class="sxs-lookup"><span data-stu-id="bcc35-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-143">Spécifie une valeur métrique spécifique au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="bcc35-144">Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-145">**FSD \_ Metric2**</span><span class="sxs-lookup"><span data-stu-id="bcc35-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-146">Spécifie une valeur métrique spécifique au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="bcc35-147">Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-148">**FSD \_ Metric3**</span><span class="sxs-lookup"><span data-stu-id="bcc35-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-149">Spécifie une valeur métrique spécifique au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="bcc35-150">Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-151">**FSD \_ Metric4**</span><span class="sxs-lookup"><span data-stu-id="bcc35-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-152">Spécifie une valeur métrique spécifique au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="bcc35-153">Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-154">**FSD \_ metric5)**</span><span class="sxs-lookup"><span data-stu-id="bcc35-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-155">Spécifie une valeur métrique spécifique au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="bcc35-156">Cette valeur de métrique est documentée dans le document [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="bcc35-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcc35-157">**\_Indicateurs FSD**</span><span class="sxs-lookup"><span data-stu-id="bcc35-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="bcc35-158">Spécifie si l’itinéraire est valide.</span><span class="sxs-lookup"><span data-stu-id="bcc35-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="bcc35-159">Le protocole de routage doit d’abord effacer ces indicateurs, puis définir l’itinéraire comme étant valide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="bcc35-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="bcc35-160">Le protocole de routage doit utiliser les macros **ClearRouteFlags ()**, **SetRouteValid ()** et **ClearRouteValid ()** pour effectuer ces opérations.</span><span class="sxs-lookup"><span data-stu-id="bcc35-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="bcc35-161">Ces macros sont définies dans RTM. h.</span><span class="sxs-lookup"><span data-stu-id="bcc35-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcc35-162">Notes</span><span class="sxs-lookup"><span data-stu-id="bcc35-162">Remarks</span></span>

<span data-ttu-id="bcc35-163">Le gestionnaire de tables de routage utilise les membres **de \_ métriques** **FSD \_** et FSD pour calculer le meilleur itinéraire vers un réseau de destination particulier.</span><span class="sxs-lookup"><span data-stu-id="bcc35-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="bcc35-164">Les membres de la **\_ mesure FSD \[ 1-5 \]** sont conformes à la conformité MIB II.</span><span class="sxs-lookup"><span data-stu-id="bcc35-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="bcc35-165">Les agents MIB II affichent uniquement ces valeurs de métriques.</span><span class="sxs-lookup"><span data-stu-id="bcc35-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="bcc35-166">Ils n’affichent pas la valeur métrique de la **\_ mesure FSD** .</span><span class="sxs-lookup"><span data-stu-id="bcc35-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="bcc35-167">Pour que la **\_ métrique FSD** soit affichée, le protocole de routage doit également stocker la valeur dans l’un des membres de la **\_ métrique FSD \[ 1-5 \]** .</span><span class="sxs-lookup"><span data-stu-id="bcc35-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="bcc35-168">Le gestionnaire de table de routage n’utilise pas les valeurs de métriques dans les membres de la **\_ mesure FSD \[ 1-5 \]** lors du calcul du meilleur itinéraire vers un réseau de destination.</span><span class="sxs-lookup"><span data-stu-id="bcc35-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="bcc35-169">Par conséquent, le protocole de routage doit s’assurer que le membre de **\_ mesure FSD** a une valeur de métrique appropriée.</span><span class="sxs-lookup"><span data-stu-id="bcc35-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="bcc35-170">Un protocole de routage peut utiliser **les \_ indicateurs FSD** pour marquer un itinéraire comme étant non valide, si l’itinéraire ne doit pas être utilisé par d’autres protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="bcc35-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc35-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcc35-171">Requirements</span></span>



| <span data-ttu-id="bcc35-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcc35-172">Requirement</span></span> | <span data-ttu-id="bcc35-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcc35-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bcc35-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcc35-174">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc35-175">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcc35-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="bcc35-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcc35-176">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc35-177">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcc35-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bcc35-178">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bcc35-178">End of server support</span></span><br/>    | <span data-ttu-id="bcc35-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bcc35-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="bcc35-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcc35-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc35-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc35-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc35-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcc35-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc35-183">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="bcc35-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bcc35-184">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="bcc35-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="bcc35-185">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="bcc35-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





