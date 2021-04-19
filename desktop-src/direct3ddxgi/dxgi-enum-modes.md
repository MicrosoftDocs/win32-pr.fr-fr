---
description: Options pour énumérer les modes d’affichage.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106544400"
---
# <a name="dxgi_enum_modes"></a><span data-ttu-id="ada8a-103">\_modes d’énumération dxgi \_</span><span class="sxs-lookup"><span data-stu-id="ada8a-103">DXGI\_ENUM\_MODES</span></span>

<span data-ttu-id="ada8a-104">Options pour énumérer les modes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ada8a-104">Options for enumerating display modes.</span></span>



| <span data-ttu-id="ada8a-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="ada8a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="ada8a-106">Description</span><span class="sxs-lookup"><span data-stu-id="ada8a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <span data-ttu-id="ada8a-107"><dt>**Dxgi \_ MODES ENUM 1UL \_ \_ entrelacés**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ada8a-107"><dt>**DXGI\_ENUM\_MODES\_INTERLACED**</dt> <dt>1UL</dt></span></span> </dl>                 | <span data-ttu-id="ada8a-108">Inclut les modes entrelacés.</span><span class="sxs-lookup"><span data-stu-id="ada8a-108">Include interlaced modes.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <span data-ttu-id="ada8a-109"><dt>**Dxgi \_ MODES ENUM pour la \_ \_ mise à l’échelle**</dt> de <dt>2UL</dt></span><span class="sxs-lookup"><span data-stu-id="ada8a-109"><dt>**DXGI\_ENUM\_MODES\_SCALING**</dt> <dt>2UL</dt></span></span> </dl>                          | <span data-ttu-id="ada8a-110">Inclut les modes de mise à l’échelle étirée.</span><span class="sxs-lookup"><span data-stu-id="ada8a-110">Include stretched-scaling modes.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <span data-ttu-id="ada8a-111"><dt>**Dxgi \_ MODES d’ÉNUMÉRation \_ \_ stéréo**</dt> <dt>4UL</dt></span><span class="sxs-lookup"><span data-stu-id="ada8a-111"><dt>**DXGI\_ENUM\_MODES\_STEREO**</dt> <dt>4UL</dt></span></span> </dl>                             | <span data-ttu-id="ada8a-112">Inclut les modes stéréo.</span><span class="sxs-lookup"><span data-stu-id="ada8a-112">Include stereo modes.</span></span><br/> <span data-ttu-id="ada8a-113">**Direct3D 11 :** Cette valeur d’énumération est prise en charge à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ada8a-113">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <span data-ttu-id="ada8a-114"><dt>**Dxgi \_ \_Modes enum \_ désactivés \_ stéréo**</dt> <dt>8UL</dt></span><span class="sxs-lookup"><span data-stu-id="ada8a-114"><dt>**DXGI\_ENUM\_MODES\_DISABLED\_STEREO**</dt> <dt>8UL</dt></span></span> </dl> | <span data-ttu-id="ada8a-115">Inclut les modes stéréo qui sont masqués, car l’utilisateur a désactivé la stéréo.</span><span class="sxs-lookup"><span data-stu-id="ada8a-115">Include stereo modes that are hidden because the user has disabled stereo.</span></span> <span data-ttu-id="ada8a-116">Les applications du panneau de configuration peuvent utiliser cette option pour afficher les fonctionnalités stéréo qui ont été désactivées dans le cadre d’une interface utilisateur qui active et désactive la fonction stéréo.</span><span class="sxs-lookup"><span data-stu-id="ada8a-116">Control panel applications can use this option to show stereo capabilities that have been disabled as part of a user interface that enables and disables stereo.</span></span><br/> <span data-ttu-id="ada8a-117">**Direct3D 11 :** Cette valeur d’énumération est prise en charge à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ada8a-117">**Direct3D 11:** This enumeration value is supported starting with Windows 8.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ada8a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ada8a-118">Remarks</span></span>

<span data-ttu-id="ada8a-119">Ces options d’indicateur sont utilisées dans [**IDXGIOutput :: GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) pour énumérer les modes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ada8a-119">These flag options are used in [**IDXGIOutput::GetDisplayModeList**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) to enumerate display modes.</span></span>

<span data-ttu-id="ada8a-120">Ces options d’indicateur sont également utilisées dans [**IDXGIOutput1 :: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) pour énumérer les modes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ada8a-120">These flag options are also used in [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) to enumerate display modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada8a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ada8a-121">Requirements</span></span>



| <span data-ttu-id="ada8a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ada8a-122">Requirement</span></span> | <span data-ttu-id="ada8a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ada8a-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ada8a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ada8a-124">Header</span></span><br/> | <dl> <span data-ttu-id="ada8a-125"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada8a-125"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ada8a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ada8a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada8a-127">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="ada8a-127">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




