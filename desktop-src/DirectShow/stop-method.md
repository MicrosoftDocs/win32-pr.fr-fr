---
description: La méthode Stop arrête la lecture.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Méthode Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952644"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="fe5d6-103">Méthode Stop (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="fe5d6-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="fe5d6-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fe5d6-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fe5d6-106">La `Stop` méthode arrête la lecture.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="fe5d6-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fe5d6-107">Return Value</span></span>

<span data-ttu-id="fe5d6-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe5d6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="fe5d6-109">Remarks</span></span>

<span data-ttu-id="fe5d6-110">Si [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de `Stop` place le navigateur DVD, ainsi que le reste du graphique de filtre, à l’état arrêté, ce qui signifie que la lecture commence au début du disque la prochaine fois que l’utilisateur appuie sur le bouton de **lecture** . Si **EnableResetOnStop** a la valeur true, la lecture reprend là où elle s’est arrêtée lorsque l’utilisateur émet la commande **Play** suivante.</span><span class="sxs-lookup"><span data-stu-id="fe5d6-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



