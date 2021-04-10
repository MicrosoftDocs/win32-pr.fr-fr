---
description: La méthode ShowCursor rend le curseur visible lorsque l’objet MSWebDVD est en mode plein écran.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Méthode ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846414"
---
# <a name="showcursor-method"></a><span data-ttu-id="54b8b-103">Méthode ShowCursor</span><span class="sxs-lookup"><span data-stu-id="54b8b-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="54b8b-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="54b8b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="54b8b-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="54b8b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="54b8b-106">La `ShowCursor` méthode rend le curseur visible lorsque l’objet **mswebdvd** est en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="54b8b-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="54b8b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54b8b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b8b-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="54b8b-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="54b8b-109">Spécifie s’il faut afficher le curseur en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="54b8b-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="54b8b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="54b8b-110">Value</span></span> | <span data-ttu-id="54b8b-111">Description</span><span class="sxs-lookup"><span data-stu-id="54b8b-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="54b8b-112">true</span><span class="sxs-lookup"><span data-stu-id="54b8b-112">true</span></span>  | <span data-ttu-id="54b8b-113">Afficher le curseur</span><span class="sxs-lookup"><span data-stu-id="54b8b-113">Show the cursor</span></span>        |
| <span data-ttu-id="54b8b-114">false</span><span class="sxs-lookup"><span data-stu-id="54b8b-114">false</span></span> | <span data-ttu-id="54b8b-115">Ne pas afficher le curseur</span><span class="sxs-lookup"><span data-stu-id="54b8b-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b8b-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54b8b-116">Return Value</span></span>

<span data-ttu-id="54b8b-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="54b8b-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b8b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="54b8b-118">Remarks</span></span>

<span data-ttu-id="54b8b-119">Lorsque l’affichage du DVD passe en mode plein écran, le curseur disparaît dans les 3 à 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="54b8b-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="54b8b-120">Utilisez cette méthode pour que le curseur soit de nouveau visible si les boutons de contrôle de votre application sont visibles en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="54b8b-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



