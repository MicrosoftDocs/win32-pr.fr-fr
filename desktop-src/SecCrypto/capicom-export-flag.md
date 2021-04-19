---
description: Le \_ \_ type d’énumération de l’indicateur d’exportation CAPICOM définit si les erreurs d’exportation de clé privée sont ignorées.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Énumération CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542559"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="51acc-103">\_Énumération de l’indicateur d’exportation CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="51acc-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="51acc-104">Le type d’énumération de l' **\_ \_ indicateur d’exportation CAPICOM** définit si les erreurs d’exportation de clé privée sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="51acc-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="51acc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="51acc-105">Members</span></span>



| <span data-ttu-id="51acc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="51acc-106">Member</span></span>                                                            | <span data-ttu-id="51acc-107">Description</span><span class="sxs-lookup"><span data-stu-id="51acc-107">Description</span></span>                                               | <span data-ttu-id="51acc-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="51acc-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="51acc-109">**\_ \_ valeur par défaut d’exportation CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="51acc-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="51acc-110">Les erreurs d’exportation de clé privée ne sont pas ignorées.</span><span class="sxs-lookup"><span data-stu-id="51acc-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="51acc-111">0</span><span class="sxs-lookup"><span data-stu-id="51acc-111">0</span></span>     |
| <span data-ttu-id="51acc-112">**\_erreur Impossible d’exporter \_ la \_ \_ clé privée \_ \_ d’exportation \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="51acc-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="51acc-113">Toute erreur d’exportation de clé privée est ignorée.</span><span class="sxs-lookup"><span data-stu-id="51acc-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="51acc-114">1</span><span class="sxs-lookup"><span data-stu-id="51acc-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="51acc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="51acc-115">Remarks</span></span>

<span data-ttu-id="51acc-116">Le \_ \_ type d’énumération de l’indicateur d’exportation CAPICOM est utilisé par la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="51acc-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="51acc-117">**Certificats. Save**</span><span class="sxs-lookup"><span data-stu-id="51acc-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="51acc-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51acc-118">Requirements</span></span>



| <span data-ttu-id="51acc-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51acc-119">Requirement</span></span> | <span data-ttu-id="51acc-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51acc-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51acc-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="51acc-121">Redistributable</span></span><br/> | <span data-ttu-id="51acc-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="51acc-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="51acc-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="51acc-123">Header</span></span><br/>          | <dl> <span data-ttu-id="51acc-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="51acc-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




