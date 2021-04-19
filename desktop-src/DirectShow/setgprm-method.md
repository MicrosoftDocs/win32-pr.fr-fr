---
description: La méthode SetGPRM définit le registre de paramètres généraux spécifié sur la valeur spécifiée.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Méthode SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513887"
---
# <a name="setgprm-method"></a><span data-ttu-id="73dfc-103">Méthode SetGPRM</span><span class="sxs-lookup"><span data-stu-id="73dfc-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="73dfc-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73dfc-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="73dfc-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="73dfc-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="73dfc-106">La `SetGPRM` méthode définit le registre de paramètres généraux spécifié sur la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="73dfc-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="73dfc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73dfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73dfc-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="73dfc-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="73dfc-109">Spécifie le registre de paramètres général à définir en tant qu’entier.</span><span class="sxs-lookup"><span data-stu-id="73dfc-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="73dfc-110">La valeur entière doit être comprise entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="73dfc-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="73dfc-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValeur*</span><span class="sxs-lookup"><span data-stu-id="73dfc-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="73dfc-112">Spécifie la nouvelle valeur du Registre sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="73dfc-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73dfc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="73dfc-113">Remarks</span></span>

<span data-ttu-id="73dfc-114">Les registres de paramètres généraux, ou GPRMs, sont des registres 16 bits que chaque disque peut utiliser de manière unique pour le stockage de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="73dfc-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="73dfc-115">Une application de lecteur n’a pas besoin d’accéder à ces registres pour un contrôle de lecture ou de navigation standard à l’aide de l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="73dfc-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="73dfc-116">Cette méthode est fournie pour les applications de lecteur qui implémentent des fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="73dfc-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="73dfc-117">N’essayez pas de modifier le GPRMs directement à moins d’avoir une connaissance approfondie de la spécification DVD et de la façon dont les GPRMs sont utilisés sur le disque en question pour être lu.</span><span class="sxs-lookup"><span data-stu-id="73dfc-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="73dfc-118">La modification de ces valeurs peut entraîner un comportement imprévisible.</span><span class="sxs-lookup"><span data-stu-id="73dfc-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



