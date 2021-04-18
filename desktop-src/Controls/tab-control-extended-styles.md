---
title: Styles étendus de contrôle onglet (CommCtrl. h)
description: Le contrôle onglet prend désormais en charge les styles étendus. Ces styles sont manipulés à l’aide des \_ messages TCM GETEXTENDEDSTYLE et TCM \_ SETEXTENDEDSTYLE et ne doivent pas être confondus avec les styles de fenêtre étendus passés à CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532848"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="135cd-104">Styles étendus de contrôle onglet</span><span class="sxs-lookup"><span data-stu-id="135cd-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="135cd-105">Le contrôle onglet prend désormais en charge les styles étendus.</span><span class="sxs-lookup"><span data-stu-id="135cd-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="135cd-106">Ces styles sont manipulés à l’aide des messages [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) et [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) et ne doivent pas être confondus avec les styles de fenêtre étendus passés à [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="135cd-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="135cd-107">Constante</span><span class="sxs-lookup"><span data-stu-id="135cd-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="135cd-108">Description</span><span class="sxs-lookup"><span data-stu-id="135cd-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="135cd-109"><dt>**TCS \_ ex \_ FLATSEPARATORS**</dt></span><span class="sxs-lookup"><span data-stu-id="135cd-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="135cd-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="135cd-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="135cd-111">Le contrôle onglet dessine des séparateurs entre les éléments d’onglet.</span><span class="sxs-lookup"><span data-stu-id="135cd-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="135cd-112">Ce style étendu affecte uniquement les contrôles d’onglet qui ont les [**\_ boutons TCS**](tab-control-styles.md) et les styles [**\_ FLATBUTTONS TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="135cd-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="135cd-113">Par défaut, la création du contrôle onglet avec le style **\_ FLATBUTTONS TCS** définit ce style étendu.</span><span class="sxs-lookup"><span data-stu-id="135cd-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="135cd-114">Si vous n’avez pas besoin de séparateurs, vous devez supprimer ce style étendu après avoir créé le contrôle.</span><span class="sxs-lookup"><span data-stu-id="135cd-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="135cd-115"><dt>**TCS \_ ex \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="135cd-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="135cd-116">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="135cd-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="135cd-117">Le contrôle onglet génère des codes de notification [TCN \_ GETOBJECT](tcn-getobject.md) pour demander un objet cible de dépôt lorsqu’un objet est glissé sur les éléments d’onglet dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="135cd-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="135cd-118">L’application doit appeler [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) avant de définir ce style.</span><span class="sxs-lookup"><span data-stu-id="135cd-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="135cd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="135cd-119">Requirements</span></span>



| <span data-ttu-id="135cd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="135cd-120">Requirement</span></span> | <span data-ttu-id="135cd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="135cd-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="135cd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="135cd-122">Header</span></span><br/> | <dl> <span data-ttu-id="135cd-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="135cd-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

