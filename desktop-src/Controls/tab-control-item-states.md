---
title: États des éléments de contrôle d’onglet (CommCtrl. h)
description: Les éléments de contrôle d’onglet prennent désormais en charge l’état d’un élément pour prendre en charge le \_ message DESELECTALL TCM. En outre, la structure TCITEM prend en charge les valeurs d’état des éléments.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537470"
---
# <a name="tab-control-item-states"></a><span data-ttu-id="ab9ac-104">États des éléments de contrôle d’onglet</span><span class="sxs-lookup"><span data-stu-id="ab9ac-104">Tab Control Item States</span></span>

<span data-ttu-id="ab9ac-105">Les éléments de contrôle d’onglet prennent désormais en charge l’état d’un élément pour prendre en charge le message [**\_ DESELECTALL TCM**](tcm-deselectall.md) .</span><span class="sxs-lookup"><span data-stu-id="ab9ac-105">Tab control items now support an item state to support the [**TCM\_DESELECTALL**](tcm-deselectall.md) message.</span></span> <span data-ttu-id="ab9ac-106">En outre, la structure [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) prend en charge les valeurs d’état des éléments.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-106">Additionally, the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure supports item state values.</span></span>



| <span data-ttu-id="ab9ac-107">Constante</span><span class="sxs-lookup"><span data-stu-id="ab9ac-107">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="ab9ac-108">Description</span><span class="sxs-lookup"><span data-stu-id="ab9ac-108">Description</span></span>                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <span data-ttu-id="ab9ac-109"><dt>**TCIS \_ BUTTONPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-109"><dt>**TCIS\_BUTTONPRESSED**</dt></span></span> </dl> | <span data-ttu-id="ab9ac-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ab9ac-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ab9ac-111">L’élément de contrôle onglet est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-111">The tab control item is selected.</span></span> <span data-ttu-id="ab9ac-112">Cet État est significatif uniquement si l’indicateur de style de [**\_ boutons TCS**](tab-control-styles.md) a été défini.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-112">This state is only meaningful if the [**TCS\_BUTTONS**](tab-control-styles.md) style flag has been set.</span></span><br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <span data-ttu-id="ab9ac-113"><dt>**TCIS \_ mis en surbrillance**</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-113"><dt>**TCIS\_HIGHLIGHTED**</dt></span></span> </dl>       | <span data-ttu-id="ab9ac-114">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ab9ac-114">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="ab9ac-115">L’élément de contrôle d’onglet est mis en surbrillance, et l’onglet et le texte sont dessinés à l’aide de la couleur de surbrillance actuelle.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-115">The tab control item is highlighted, and the tab and text are drawn using the current highlight color.</span></span> <span data-ttu-id="ab9ac-116">Si vous utilisez 65536 couleurs, il s’agit d’une véritable interpolation, et non d’une couleur dépendante.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-116">When using high-color, this will be a true interpolation, not a dithered color.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ab9ac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab9ac-117">Requirements</span></span>



| <span data-ttu-id="ab9ac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab9ac-118">Requirement</span></span> | <span data-ttu-id="ab9ac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab9ac-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9ac-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab9ac-120">Header</span></span><br/> | <dl> <span data-ttu-id="ab9ac-121"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-121"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





