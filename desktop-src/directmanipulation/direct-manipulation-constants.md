---
description: Cette section fournit les spécifications de référence pour les constantes de manipulation directe.
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: Constantes de manipulation directe
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5040191f22e92dcfb8c2ca26edd4080cd4cbb2be
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544547"
---
# <a name="direct-manipulation-constants"></a><span data-ttu-id="43b17-103">Constantes de manipulation directe</span><span class="sxs-lookup"><span data-stu-id="43b17-103">Direct Manipulation Constants</span></span>

<span data-ttu-id="43b17-104">Cette section fournit les spécifications de référence pour les constantes de [manipulation directe](direct-manipulation-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="43b17-104">This section provides the reference specifications for [Direct Manipulation](direct-manipulation-portal.md) constants.</span></span>

| <span data-ttu-id="43b17-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="43b17-105">Constant/value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="43b17-106">Description</span><span class="sxs-lookup"><span data-stu-id="43b17-106">Description</span></span>                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <span data-ttu-id="43b17-107"><dt>**DIRECTMANIPULATION \_ KEYBOARDFOCUS**</dt> <dt>0xfffffffe</dt></span><span class="sxs-lookup"><span data-stu-id="43b17-107"><dt>**DIRECTMANIPULATION\_KEYBOARDFOCUS**</dt> <dt>0xFFFFFFFE</dt></span></span> </dl> | <span data-ttu-id="43b17-108">Spécifie un ID de pointeur Psuedo pour émuler un contact tactile via une entrée au clavier.</span><span class="sxs-lookup"><span data-stu-id="43b17-108">Specifies a psuedo-pointer ID for emulating a touch contact through keyboard input.</span></span><br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <span data-ttu-id="43b17-109"><dt>**DIRECTMANIPULATION \_ MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt></span><span class="sxs-lookup"><span data-stu-id="43b17-109"><dt>**DIRECTMANIPULATION\_MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt></span></span> </dl>          | <span data-ttu-id="43b17-110">Spécifie un ID de pointeur Psuedo pour émuler un contact tactile via l’entrée de la souris.</span><span class="sxs-lookup"><span data-stu-id="43b17-110">Specifies a psuedo-pointer ID for emulating a touch contact through mouse input.</span></span><br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <span data-ttu-id="43b17-111"><dt>**DIRECTMANIPULATION \_ \_Zoom minimal**</dt> <dt>0,1</dt></span><span class="sxs-lookup"><span data-stu-id="43b17-111"><dt>**DIRECTMANIPULATION\_MINIMUM\_ZOOM**</dt> <dt>0.1</dt></span></span> </dl>          | <span data-ttu-id="43b17-112">Spécifie la limite de zoom minimale autorisée de 10%.</span><span class="sxs-lookup"><span data-stu-id="43b17-112">Specifies the minimum permitted zoom boundary of 10%.</span></span><br/>                               |

## <a name="requirements"></a><span data-ttu-id="43b17-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43b17-113">Requirements</span></span>

| <span data-ttu-id="43b17-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43b17-114">Requirement</span></span> | <span data-ttu-id="43b17-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="43b17-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b17-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43b17-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43b17-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="43b17-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43b17-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43b17-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="43b17-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="43b17-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43b17-121"><dt>DirectManipulation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43b17-121"><dt>DirectManipulation.idl</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="43b17-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b17-122">See also</span></span>

[<span data-ttu-id="43b17-123">Référence de manipulation directe</span><span class="sxs-lookup"><span data-stu-id="43b17-123">Direct Manipulation Reference</span></span>](direct-manipulation-reference.md)
