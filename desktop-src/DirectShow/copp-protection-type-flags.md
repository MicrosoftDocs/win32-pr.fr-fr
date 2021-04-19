---
description: Les constantes suivies sont utilisées avec le protocole de protection de sortie certifié (COPP) sur des mécanismes de protection de sortie spécifiques.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Indicateurs de type de protection COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541773"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="e009e-103">Indicateurs de type de protection COPP</span><span class="sxs-lookup"><span data-stu-id="e009e-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="e009e-104">Les constantes suivies sont utilisées avec le protocole de protection de sortie certifié (COPP) sur des mécanismes de protection de sortie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e009e-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="e009e-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e009e-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="e009e-106">Description</span><span class="sxs-lookup"><span data-stu-id="e009e-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="e009e-107"><dt>**Copp \_ ProtectionType \_ inconnu**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="e009e-108">Mécanisme de protection inconnu.</span><span class="sxs-lookup"><span data-stu-id="e009e-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="e009e-109"><dt>**Copp \_ ProtectionType \_ aucun**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="e009e-110">Aucun mécanisme de protection.</span><span class="sxs-lookup"><span data-stu-id="e009e-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="e009e-111"><dt>**Copp \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="e009e-112">High-Bandwidth protection du contenu numérique (HDCP).</span><span class="sxs-lookup"><span data-stu-id="e009e-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="e009e-113"><dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="e009e-114">Protection contre la copie analogique (ACP).</span><span class="sxs-lookup"><span data-stu-id="e009e-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="e009e-115"><dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="e009e-116">Version analogique du système de gestion de la génération de copie (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="e009e-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="e009e-117"><dt>**Copp \_ ProtectionType \_ masque**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="e009e-118">Masque de masque pour isoler les indicateurs valides.</span><span class="sxs-lookup"><span data-stu-id="e009e-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="e009e-119"><dt>**Copp \_ ProtectionType \_ réservé**</dt> <dt>0x7FFFFFF8</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="e009e-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e009e-120">Reserved.</span></span> <span data-ttu-id="e009e-121">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e009e-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="e009e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e009e-122">Remarks</span></span>

<span data-ttu-id="e009e-123">Certaines méthodes retournent un seul indicateur à partir de ce type d’énumération, et certaines méthodes retournent une opération or au niveau du bit d' **un ou plusieurs** indicateurs.</span><span class="sxs-lookup"><span data-stu-id="e009e-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="e009e-124">Ces indicateurs sont utilisés dans les requêtes et les commandes COPP suivantes.</span><span class="sxs-lookup"><span data-stu-id="e009e-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="e009e-125">Niveau de protection global</span><span class="sxs-lookup"><span data-stu-id="e009e-125">Global Protection Level</span></span>
-   <span data-ttu-id="e009e-126">Niveau de protection local</span><span class="sxs-lookup"><span data-stu-id="e009e-126">Local Protection Level</span></span>
-   <span data-ttu-id="e009e-127">Type de protection</span><span class="sxs-lookup"><span data-stu-id="e009e-127">Protection Type</span></span>
-   <span data-ttu-id="e009e-128">Définir le niveau de protection</span><span class="sxs-lookup"><span data-stu-id="e009e-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="e009e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e009e-129">Requirements</span></span>



| <span data-ttu-id="e009e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e009e-130">Requirement</span></span> | <span data-ttu-id="e009e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e009e-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e009e-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e009e-132">Header</span></span><br/> | <dl> <span data-ttu-id="e009e-133"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e009e-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e009e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e009e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e009e-135">Constantes et GUID</span><span class="sxs-lookup"><span data-stu-id="e009e-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="e009e-136">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="e009e-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




