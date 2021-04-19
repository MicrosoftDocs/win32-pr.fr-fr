---
description: La méthode ActivateButton active le bouton de menu sélectionné.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Méthode ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517161"
---
# <a name="activatebutton-method"></a><span data-ttu-id="27306-103">Méthode ActivateButton</span><span class="sxs-lookup"><span data-stu-id="27306-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="27306-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="27306-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="27306-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="27306-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="27306-106">La méthode ActivateButton active le bouton de menu sélectionné.</span><span class="sxs-lookup"><span data-stu-id="27306-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="27306-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27306-107">Return Value</span></span>

<span data-ttu-id="27306-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="27306-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="27306-109">Notes</span><span class="sxs-lookup"><span data-stu-id="27306-109">Remarks</span></span>

<span data-ttu-id="27306-110">Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="27306-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="27306-111">Utilisez cette méthode pour activer un bouton qui a été sélectionné par le biais de la méthode [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)ou [**SelectRightButton**](selectrightbutton-method.md) .</span><span class="sxs-lookup"><span data-stu-id="27306-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



