---
description: Les \_ constantes d’indicateur de bit LINESPECIALINFO décrivent des signaux d’information spéciaux que le réseau peut utiliser pour signaler diverses opérations de rapports et d’observation du réseau.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522791"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="64af2-103">\_Constantes LINESPECIALINFO</span><span class="sxs-lookup"><span data-stu-id="64af2-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="64af2-104">Les constantes d’indicateur de bit **LINESPECIALINFO \_** décrivent des signaux d’information spéciaux que le réseau peut utiliser pour signaler diverses opérations de rapports et d’observation du réseau.</span><span class="sxs-lookup"><span data-stu-id="64af2-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="64af2-105">Il s’agit de séquences de fréquences codées spéciales transmises au début des annonces enregistrées de l’avis réseau.</span><span class="sxs-lookup"><span data-stu-id="64af2-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="64af2-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**</span><span class="sxs-lookup"><span data-stu-id="64af2-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="64af2-107">Ce titre d’information spécial précède un nombre vacant, AIS, un changement de numéro Centrex et une station chômée, le code d’accès n’est pas composé ou composé d’erreurs ou le message d’opérateur d’interception manuelle (catégorie d’irrégularité du client).</span><span class="sxs-lookup"><span data-stu-id="64af2-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="64af2-108">LINESPECIALINFO \_ CUSTIRREG est également signalé lorsque les informations de facturation sont rejetées et lorsque l’adresse composed est bloquée au niveau du commutateur.</span><span class="sxs-lookup"><span data-stu-id="64af2-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64af2-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**</span><span class="sxs-lookup"><span data-stu-id="64af2-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="64af2-110">Ce titre d’information spécial précède un circuit non ou une annonce d’urgence (catégorie de blocage de troncation).</span><span class="sxs-lookup"><span data-stu-id="64af2-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64af2-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**réorganisation LINESPECIALINFO \_**</span><span class="sxs-lookup"><span data-stu-id="64af2-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="64af2-112">Ce titre d’information spécial précède une annonce de réorganisation (catégorie d’irrégularité d’équipement).</span><span class="sxs-lookup"><span data-stu-id="64af2-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="64af2-113">\_La réorganisation LINESPECIALINFO est également signalée lorsque le téléphone est maintenu offhook trop long.</span><span class="sxs-lookup"><span data-stu-id="64af2-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64af2-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="64af2-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="64af2-115">Les spécificités relatives à la tonalité des informations spéciales ne sont pas disponibles et ne seront pas connues.</span><span class="sxs-lookup"><span data-stu-id="64af2-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="64af2-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="64af2-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="64af2-117">Les spécificités relatives à la tonalité des informations spéciales sont actuellement inconnues, mais peuvent devenir connues plus tard.</span><span class="sxs-lookup"><span data-stu-id="64af2-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64af2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="64af2-118">Remarks</span></span>

<span data-ttu-id="64af2-119">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="64af2-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="64af2-120">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="64af2-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="64af2-121">Des tonalités spéciales sont définies pour les messages de notification et ne sont généralement pas utilisées à des fins de facturation ou de supervision.</span><span class="sxs-lookup"><span data-stu-id="64af2-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="64af2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64af2-122">Requirements</span></span>



| <span data-ttu-id="64af2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64af2-123">Requirement</span></span> | <span data-ttu-id="64af2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="64af2-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="64af2-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="64af2-125">TAPI version</span></span><br/> | <span data-ttu-id="64af2-126">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="64af2-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="64af2-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="64af2-127">Header</span></span><br/>       | <dl> <span data-ttu-id="64af2-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="64af2-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




