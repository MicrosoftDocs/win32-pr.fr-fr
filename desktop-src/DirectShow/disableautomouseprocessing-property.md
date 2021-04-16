---
description: La propriété DisableAutoMouseProcessing active ou désactive la fonctionnalité de traitement de la souris de l’objet MSWebDVD.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Propriété DisableAutoMouseProcessing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480857"
---
# <a name="disableautomouseprocessing-property"></a><span data-ttu-id="ce0c9-103">Propriété DisableAutoMouseProcessing</span><span class="sxs-lookup"><span data-stu-id="ce0c9-103">DisableAutoMouseProcessing Property</span></span>

> [!Note]  
> <span data-ttu-id="ce0c9-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ce0c9-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ce0c9-106">La `DisableAutoMouseProcessing` propriété active ou désactive la fonctionnalité de traitement de la souris de l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="ce0c9-106">The `DisableAutoMouseProcessing` property enables or disables the **MSWebDVD** object's mouse-processing functionality.</span></span>

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a><span data-ttu-id="ce0c9-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce0c9-107">Return Value</span></span>

<span data-ttu-id="ce0c9-108">Retourne une valeur booléenne indiquant s’il faut désactiver le traitement par défaut de la souris.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-108">Returns a boolean value indicating whether to disable the default mouse processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce0c9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ce0c9-109">Remarks</span></span>

<span data-ttu-id="ce0c9-110">Cette propriété est en lecture/écriture et sa valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-110">This property is read/write with a default value of false.</span></span> <span data-ttu-id="ce0c9-111">L’objet **mswebdvd** gère automatiquement les actions de la souris pour les menus sur écran de DVD par défaut ; les utilisateurs peuvent mettre en surbrillance et activer des boutons de menu sans programmation particulière par l’application.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-111">The **MSWebDVD** object automatically handles mouse actions for DVD on-screen menus by default; users can highlight and activate menu buttons without special programming by the application.</span></span> <span data-ttu-id="ce0c9-112">Une application peut désactiver cette fonctionnalité de gestion de la souris par défaut en affectant à cette propriété la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-112">An application can turn off this default mouse-handling functionality by setting this property to **true**.</span></span> <span data-ttu-id="ce0c9-113">Lorsque le traitement automatique de la souris est désactivé, une application doit utiliser les différentes méthodes et propriétés liées aux boutons pour gérer les déplacements de la souris et les clics de souris dans les menus à l’écran.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-113">When the automatic mouse processing is turned off, an application must use the various button-related methods and properties to handle mouse moves and mouse clicks on the on-screen menus.</span></span> <span data-ttu-id="ce0c9-114">En outre, une application peut utiliser les méthodes associées à un bouton pour remplacer la gestion automatique de la souris même lorsque when `DisableAutoMouseProcessing` a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="ce0c9-114">Also, an application can use the button-related methods to override the automatic mouse handling even when when `DisableAutoMouseProcessing` is set to **false**.</span></span>

 

 



