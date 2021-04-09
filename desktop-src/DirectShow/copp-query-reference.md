---
description: Informations de référence sur les requêtes COPP
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: Informations de référence sur les requêtes COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033557"
---
# <a name="copp-query-reference"></a><span data-ttu-id="e5eaa-103">Informations de référence sur les requêtes COPP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-103">COPP Query Reference</span></span>

<span data-ttu-id="e5eaa-104">Cette section décrit les requêtes d’État prises en charge par le protocole COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="e5eaa-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="e5eaa-105">Pour chaque requête, le GUID qui définit la requête est listé, avec les données d’entrée et les données de retour.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="e5eaa-106">Requête</span><span class="sxs-lookup"><span data-stu-id="e5eaa-106">Query</span></span>                   | <span data-ttu-id="e5eaa-107">GUID</span><span class="sxs-lookup"><span data-stu-id="e5eaa-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="e5eaa-108">Données de bus</span><span class="sxs-lookup"><span data-stu-id="e5eaa-108">Bus Data</span></span>                | <span data-ttu-id="e5eaa-109">**\_COPPQUERYBUSDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="e5eaa-110">Type de connecteur</span><span class="sxs-lookup"><span data-stu-id="e5eaa-110">Connector Type</span></span>          | <span data-ttu-id="e5eaa-111">**\_COPPQUERYCONNECTORTYPE DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="e5eaa-112">Afficher les données</span><span class="sxs-lookup"><span data-stu-id="e5eaa-112">Display Data</span></span>            | <span data-ttu-id="e5eaa-113">**\_COPPQUERYDISPLAYDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="e5eaa-114">Données de clé HDCP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-114">HDCP Key Data</span></span>           | <span data-ttu-id="e5eaa-115">**\_COPPQUERYHDCPKEYDATA DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="e5eaa-116">Niveau de protection global</span><span class="sxs-lookup"><span data-stu-id="e5eaa-116">Global Protection Level</span></span> | <span data-ttu-id="e5eaa-117">**\_COPPQUERYGLOBALPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="e5eaa-118">Niveau de protection local</span><span class="sxs-lookup"><span data-stu-id="e5eaa-118">Local Protection Level</span></span>  | <span data-ttu-id="e5eaa-119">**\_COPPQUERYLOCALPROTECTIONLEVEL DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="e5eaa-120">Type de protection</span><span class="sxs-lookup"><span data-stu-id="e5eaa-120">Protection Type</span></span>         | <span data-ttu-id="e5eaa-121">**\_COPPQUERYPROTECTIONTYPE DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="e5eaa-122">Signalisation</span><span class="sxs-lookup"><span data-stu-id="e5eaa-122">Signaling</span></span>               | <span data-ttu-id="e5eaa-123">**\_COPPQUERYSIGNALING DXVA**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="e5eaa-124">Requête de données de bus</span><span class="sxs-lookup"><span data-stu-id="e5eaa-124">Bus Data Query</span></span>

<span data-ttu-id="e5eaa-125">Retourne le type de bus d’e/s utilisé par la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="e5eaa-126">**GUID**: DXVA \_ COPPQueryBusData</span><span class="sxs-lookup"><span data-stu-id="e5eaa-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="e5eaa-127">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-127">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-128">**Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="e5eaa-129">Le type de bus est retourné dans le membre **dwData** en tant qu’indicateur de l’énumération [**Copp \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="e5eaa-130">Requête de type de connecteur</span><span class="sxs-lookup"><span data-stu-id="e5eaa-130">Connector Type Query</span></span>

<span data-ttu-id="e5eaa-131">Retourne le type de connecteur physique.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="e5eaa-132">**GUID**: DXVA \_ COPPQueryConnectorType</span><span class="sxs-lookup"><span data-stu-id="e5eaa-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="e5eaa-133">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-133">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-134">**Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="e5eaa-135">Le type de connecteur est retourné dans le membre **dwData** en tant qu’indicateur de l’énumération [**Copp \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="e5eaa-136">Afficher la requête de données</span><span class="sxs-lookup"><span data-stu-id="e5eaa-136">Display Data Query</span></span>

<span data-ttu-id="e5eaa-137">Retourne une description du signal vidéo qui est transmis sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="e5eaa-138">Le signal vidéo transmis sur le connecteur n’a pas nécessairement le même format que le mode d’affichage du bureau.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="e5eaa-139">Par exemple, le mode d’affichage du Bureau peut être de 1024 x 768 pixels à 85 Hz, tandis que le connecteur peut être un connecteur S-Video qui transmet un signal vidéo à 720 x 480 pixels, 60/1.01 Hz entrelacé.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="e5eaa-140">Dans ce cas, le pilote retourne la résolution du signal S-Video, et non la résolution du bureau.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="e5eaa-141">**GUID**: DXVA \_ COPPQueryDisplayData</span><span class="sxs-lookup"><span data-stu-id="e5eaa-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="e5eaa-142">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-142">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-143">**Return Data**: retourne une structure [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="e5eaa-144">Requête de données de clé HDCP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-144">HDCP Key Data Query</span></span>

<span data-ttu-id="e5eaa-145">Retourne le vecteur de sélection de clé HDCP de l’appareil (B-KSV).</span><span class="sxs-lookup"><span data-stu-id="e5eaa-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="e5eaa-146">KSV est un identificateur fourni au fabricant de l’appareil et est utilisé dans le processus d’authentification et d’installation HDCP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="e5eaa-147">L’application doit vérifier cette valeur par rapport à la liste des KSVs révoqués.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="e5eaa-148">Le mécanisme d’obtention de la liste de révocation KSV est en dehors de l’étendue du protocole COPP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="e5eaa-149">Pour plus d’informations, consultez la spécification HDCP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="e5eaa-150">Cette requête détermine également si l’appareil HDCP connecté est une analyse ou un répéteur HDCP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="e5eaa-151">L’application ne doit pas lire de contenu protégé si l’appareil HDCP est un répétiteur HDCP, car ceux-ci ne sont pas pris en charge par COPP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="e5eaa-152">**GUID**: DXVA \_ COPPQueryHDCPKeyData</span><span class="sxs-lookup"><span data-stu-id="e5eaa-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="e5eaa-153">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-153">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-154">**Return Data**: retourne une structure [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="e5eaa-155">Requête de niveau de protection global</span><span class="sxs-lookup"><span data-stu-id="e5eaa-155">Global Protection Level Query</span></span>

<span data-ttu-id="e5eaa-156">Retourne le niveau de protection global pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="e5eaa-157">Le niveau de protection global est le niveau de protection en cours d’application sur le connecteur, quelle que soit la façon dont le pilote Graphics a été invité à appliquer la protection.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="e5eaa-158">Par exemple, une application peut définir le niveau de protection ACP en appelant la fonction **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="e5eaa-159">Dans ce cas, le niveau de protection global reflète ce paramètre, même s’il n’a pas été demandé via COPP.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="e5eaa-160">**GUID**: DXVA \_ COPPQueryGlobalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="e5eaa-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="e5eaa-161">**Données d’entrée**: mécanisme de protection à interroger, spécifié sous la forme d’un entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="e5eaa-162">Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e5eaa-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="e5eaa-163">**Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="e5eaa-164">Le niveau de protection actuel est retourné dans le membre **dwData** .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="e5eaa-165">La signification de cette valeur dépend du mécanisme de protection qui est interrogé.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="e5eaa-166">Pour chaque mécanisme de protection, la valeur du membre **dwData** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="e5eaa-167">Mécanisme de protection</span><span class="sxs-lookup"><span data-stu-id="e5eaa-167">Protection mechanism</span></span> | <span data-ttu-id="e5eaa-168">Énumération</span><span class="sxs-lookup"><span data-stu-id="e5eaa-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="e5eaa-169">ACP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-169">ACP</span></span>                  | [<span data-ttu-id="e5eaa-170">**Niveau de protection de l’ACP de COPP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="e5eaa-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="e5eaa-171">CGMS-A</span></span>               | [<span data-ttu-id="e5eaa-172">**\_Niveau de \_ protection \_ CGMSA de Copp**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="e5eaa-173">HDCP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-173">HDCP</span></span>                 | [<span data-ttu-id="e5eaa-174">**\_Niveau de \_ protection du HDCP Copp \_**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="e5eaa-175">Requête de niveau de protection local</span><span class="sxs-lookup"><span data-stu-id="e5eaa-175">Local Protection Level Query</span></span>

<span data-ttu-id="e5eaa-176">Retourne le niveau de protection local pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="e5eaa-177">Le niveau de protection local est le niveau de protection qui a été demandé via la session COPP actuelle.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="e5eaa-178">Le pilote peut définir un niveau de protection supérieur.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="e5eaa-179">**GUID**: DXVA \_ COPPQueryLocalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="e5eaa-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="e5eaa-180">**Données d’entrée**: mécanisme de protection à interroger, en tant qu’entier 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="e5eaa-181">Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e5eaa-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="e5eaa-182">**Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="e5eaa-183">Le niveau de protection actuel est retourné dans le membre **dwData** .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="e5eaa-184">La signification de cette valeur dépend du mécanisme de protection qui est interrogé.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="e5eaa-185">Pour chaque mécanisme de protection, la valeur du membre **dwData** est un indicateur d’une énumération différente, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="e5eaa-186">Mécanisme de protection</span><span class="sxs-lookup"><span data-stu-id="e5eaa-186">Protection mechanism</span></span> | <span data-ttu-id="e5eaa-187">Énumération</span><span class="sxs-lookup"><span data-stu-id="e5eaa-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="e5eaa-188">ACP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-188">ACP</span></span>                  | [<span data-ttu-id="e5eaa-189">**Niveau de protection de l’ACP de COPP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="e5eaa-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="e5eaa-190">CGMS-A</span></span>               | [<span data-ttu-id="e5eaa-191">**\_Niveau de \_ protection \_ CGMSA de Copp**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="e5eaa-192">HDCP</span><span class="sxs-lookup"><span data-stu-id="e5eaa-192">HDCP</span></span>                 | [<span data-ttu-id="e5eaa-193">**\_Niveau de \_ protection du HDCP Copp \_**</span><span class="sxs-lookup"><span data-stu-id="e5eaa-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="e5eaa-194">Requête de type de protection</span><span class="sxs-lookup"><span data-stu-id="e5eaa-194">Protection Type Query</span></span>

<span data-ttu-id="e5eaa-195">Retourne les mécanismes de protection disponibles pour le connecteur.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="e5eaa-196">**GUID**: DXVA \_ COPPQueryProtectionType</span><span class="sxs-lookup"><span data-stu-id="e5eaa-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="e5eaa-197">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-197">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-198">**Return Data**: retourne une structure [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="e5eaa-199">Les mécanismes de protection sont retournés dans le membre **dwData** comme une combinaison de zéro ou plusieurs indicateurs.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="e5eaa-200">Voir [indicateurs de type de protection Copp](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e5eaa-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="e5eaa-201">Si plusieurs mécanismes de protection sont disponibles, les indicateurs sont combinés avec **une opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="e5eaa-202">Requête de signalisation</span><span class="sxs-lookup"><span data-stu-id="e5eaa-202">Signaling Query</span></span>

<span data-ttu-id="e5eaa-203">Retourne une liste de toutes les normes de protection prises en charge par le pilote, la norme actuellement active et les proportions actuelles ou autres données de signalisation.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="e5eaa-204">**GUID**: DXVA \_ COPPQuerySignaling</span><span class="sxs-lookup"><span data-stu-id="e5eaa-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="e5eaa-205">**Données d’entrée**: aucune.</span><span class="sxs-lookup"><span data-stu-id="e5eaa-205">**Input data**: None.</span></span>
-   <span data-ttu-id="e5eaa-206">**Return Data**: retourne une structure [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) .</span><span class="sxs-lookup"><span data-stu-id="e5eaa-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5eaa-207">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5eaa-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5eaa-208">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="e5eaa-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



