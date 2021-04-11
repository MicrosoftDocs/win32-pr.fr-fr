---
description: La propriété FullScreenMode définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Propriété FullScreenMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108538"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="64aea-103">Propriété FullScreenMode</span><span class="sxs-lookup"><span data-stu-id="64aea-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="64aea-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="64aea-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="64aea-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="64aea-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="64aea-106">La `FullScreenMode` propriété définit ou récupère une valeur indiquant si l’affichage est en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="64aea-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="64aea-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="64aea-107">Return Value</span></span>

<span data-ttu-id="64aea-108">Retourne une valeur booléenne indiquant s’il faut activer ou désactiver la lecture en plein écran.</span><span class="sxs-lookup"><span data-stu-id="64aea-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="64aea-109">Notes</span><span class="sxs-lookup"><span data-stu-id="64aea-109">Remarks</span></span>

<span data-ttu-id="64aea-110">Cette propriété est en lecture/écriture et sa valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="64aea-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="64aea-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="64aea-111">Value</span></span> | <span data-ttu-id="64aea-112">Description</span><span class="sxs-lookup"><span data-stu-id="64aea-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="64aea-113">true</span><span class="sxs-lookup"><span data-stu-id="64aea-113">true</span></span>  | <span data-ttu-id="64aea-114">Activez la lecture en plein écran.</span><span class="sxs-lookup"><span data-stu-id="64aea-114">Enable full-screen playback.</span></span> <span data-ttu-id="64aea-115">Il s'agit de la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="64aea-115">This is the default value</span></span> |
| <span data-ttu-id="64aea-116">false</span><span class="sxs-lookup"><span data-stu-id="64aea-116">false</span></span> | <span data-ttu-id="64aea-117">Désactivez la lecture en plein écran.</span><span class="sxs-lookup"><span data-stu-id="64aea-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="64aea-118">Le mode plein écran est disponible uniquement lorsque le contrôle MSWebDVD s’exécute en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="64aea-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



