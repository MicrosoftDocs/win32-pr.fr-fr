---
description: Cet attribut ajoute l’icône d’élévation du contrôle de compte d’utilisateur (icône bouclier) au contrôle PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Attribut ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115674"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="677a0-103">Attribut ElevationShield</span><span class="sxs-lookup"><span data-stu-id="677a0-103">ElevationShield Attribute</span></span>

<span data-ttu-id="677a0-104">Cet attribut ajoute l’icône d’élévation du [*contrôle de compte d’utilisateur*](u-gly.md) (icône bouclier) au [contrôle PUSHBUTTON](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="677a0-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="677a0-105">Si ce bit est défini et que l’installation n’est pas encore en cours d’exécution avec des privilèges [*élevés*](e-gly.md) , le contrôle PUSHBUTTON est créé à l’aide de l’icône d’élévation du [*contrôle de compte d’utilisateur*](u-gly.md) (icône bouclier).</span><span class="sxs-lookup"><span data-stu-id="677a0-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="677a0-106">Si ce bit est défini et que l’installation est déjà en cours d’exécution avec des privilèges [*élevés*](e-gly.md) , le contrôle PUSHBUTTON est créé à l’aide des autres attributs d’icône.</span><span class="sxs-lookup"><span data-stu-id="677a0-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="677a0-107">Si ce bit n’est pas défini, le contrôle PUSHBUTTON est créé à l’aide des autres attributs d’icône.</span><span class="sxs-lookup"><span data-stu-id="677a0-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="677a0-108">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="677a0-108">Valid Controls</span></span>

[<span data-ttu-id="677a0-109">Boutons</span><span class="sxs-lookup"><span data-stu-id="677a0-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="677a0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="677a0-110">Value</span></span>



| <span data-ttu-id="677a0-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="677a0-111">Decimal</span></span> | <span data-ttu-id="677a0-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="677a0-112">Hexadecimal</span></span> | <span data-ttu-id="677a0-113">Constante</span><span class="sxs-lookup"><span data-stu-id="677a0-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="677a0-114">8388608</span><span class="sxs-lookup"><span data-stu-id="677a0-114">8388608</span></span> | <span data-ttu-id="677a0-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="677a0-115">0x00800000</span></span>  | <span data-ttu-id="677a0-116">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="677a0-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



