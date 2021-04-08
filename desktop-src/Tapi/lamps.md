---
description: Les lampes sur un appareil téléphonique peuvent être allumées dans divers modes d’éclairage différents.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lampes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035042"
---
# <a name="lamps"></a><span data-ttu-id="b9003-103">Lampes</span><span class="sxs-lookup"><span data-stu-id="b9003-103">Lamps</span></span>

<span data-ttu-id="b9003-104">Les lampes sur un appareil téléphonique peuvent être allumées dans divers modes d’éclairage différents.</span><span class="sxs-lookup"><span data-stu-id="b9003-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="b9003-105">Contrairement aux modèles de sonnerie, les modes de lampe sont plus uniformes pour les différents groupes de téléphones de différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b9003-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="b9003-106">Un ensemble commun de modes de lampe est défini par l’API.</span><span class="sxs-lookup"><span data-stu-id="b9003-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="b9003-107">Une lampe identifiée par son identificateur de bouton de lampe peut être allumée dans un mode de lampe donné.</span><span class="sxs-lookup"><span data-stu-id="b9003-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="b9003-108">Une lampe peut également être interrogée pour son mode de lampe actuel.</span><span class="sxs-lookup"><span data-stu-id="b9003-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="b9003-109">Les fonctions TAPI utilisées pour les lampes sont [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), qui illumine une lampe sur un appareil téléphonique ouvert spécifié dans un mode d’éclairage de lampe donné et [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), qui retourne le mode de lampe actuel de la lampe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b9003-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="b9003-110">Quand une lampe d’appareil téléphonique est modifiée, un message [**d' \_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État.</span><span class="sxs-lookup"><span data-stu-id="b9003-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="b9003-111">Les paramètres de ce message fournissent une indication de la modification.</span><span class="sxs-lookup"><span data-stu-id="b9003-111">Parameters to this message provide an indication of the change.</span></span>

 

 



