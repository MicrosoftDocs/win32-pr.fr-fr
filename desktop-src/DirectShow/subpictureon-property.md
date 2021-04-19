---
description: La propriété SubpictureOn définit ou récupère l’état de la sous-image actuelle (on ou OFF).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propriété SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523412"
---
# <a name="subpictureon-property"></a><span data-ttu-id="dbd7a-103">Propriété SubpictureOn</span><span class="sxs-lookup"><span data-stu-id="dbd7a-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="dbd7a-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dbd7a-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dbd7a-106">La `SubpictureOn` propriété définit ou récupère l’état de la sous-image actuelle (on ou OFF).</span><span class="sxs-lookup"><span data-stu-id="dbd7a-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="dbd7a-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dbd7a-107">Return Value</span></span>

<span data-ttu-id="dbd7a-108">Retourne une valeur booléenne indiquant si la sous-image est affichée.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbd7a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dbd7a-109">Remarks</span></span>

<span data-ttu-id="dbd7a-110">Cette propriété n’a aucune incidence sur l’affichage des sous-titres.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="dbd7a-111">Les sous-titres sont incorporés dans le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="dbd7a-112">Les sous-images de DVD sont transportées sur un flux de travail distinct.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="dbd7a-113">Lorsque le flux de sous-image est modifié à l’aide de [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` propriété bascule sur **true**.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="dbd7a-114">Cette propriété est en lecture/écriture et sa valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="dbd7a-114">This property is read/write with a default value of false.</span></span>

 

 



