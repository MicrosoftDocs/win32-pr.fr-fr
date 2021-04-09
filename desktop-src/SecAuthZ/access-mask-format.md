---
description: Tous les objets sécurisables réorganisent leurs droits d’accès à l’aide du format de masque d’accès indiqué dans l’illustration suivante.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Format du masque d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866005"
---
# <a name="access-mask-format"></a><span data-ttu-id="ed779-103">Format du masque d’accès</span><span class="sxs-lookup"><span data-stu-id="ed779-103">Access Mask Format</span></span>

<span data-ttu-id="ed779-104">Tous les objets sécurisables réorganisent leurs droits d’accès à l’aide du format de [*masque d’accès*](/windows/desktop/SecGloss/a-gly) indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="ed779-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![format du masque d’accès](images/accctrl4.png)

<span data-ttu-id="ed779-106">Dans ce format, les 16 bits de poids faible sont pour les droits d’accès spécifiques aux objets, les 8 bits suivants sont pour les [droits d’accès standard](standard-access-rights.md), qui s’appliquent à la plupart des types d’objets, et les 4 bits de poids fort sont utilisés pour spécifier des [droits d’accès génériques](generic-access-rights.md) que chaque type d’objet peut mapper à un ensemble de droits standard et spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="ed779-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="ed779-107">Le \_ bit de \_ sécurité système Access correspond au [droit d’accéder à la liste SACL de l’objet](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="ed779-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
