---
description: La méthode GetGPRM récupère le registre de paramètres généraux spécifié.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Méthode GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522311"
---
# <a name="getgprm-method"></a><span data-ttu-id="99aaf-103">Méthode GetGPRM</span><span class="sxs-lookup"><span data-stu-id="99aaf-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="99aaf-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="99aaf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="99aaf-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="99aaf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="99aaf-106">La `GetGPRM` méthode récupère le registre de paramètres généraux spécifié.</span><span class="sxs-lookup"><span data-stu-id="99aaf-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="99aaf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99aaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99aaf-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="99aaf-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="99aaf-109">Spécifie le registre à récupérer sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="99aaf-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="99aaf-110">La valeur doit être comprise entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="99aaf-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99aaf-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="99aaf-111">Return Value</span></span>

<span data-ttu-id="99aaf-112">Retourne une valeur entière représentant le registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="99aaf-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="99aaf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="99aaf-113">Remarks</span></span>

<span data-ttu-id="99aaf-114">Cette méthode n’est pas requise pour les fonctionnalités de navigation ou de lecture de DVD à l’aide de l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="99aaf-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="99aaf-115">Il est fourni pour ceux qui ont une compréhension approfondie de la spécification du DVD qui souhaite implémenter des fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="99aaf-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="99aaf-116">GPRMs peut être utilisé pour stocker toutes les valeurs, de sorte qu’elles puissent être définies et lues librement.</span><span class="sxs-lookup"><span data-stu-id="99aaf-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="99aaf-117">Toutefois, étant donné que les GPRMs sont utilisés pour stocker également les commandes de disque, la modification de leurs valeurs à l’aide de [**SetGPRM**](setgprm-method.md) peut entraîner un comportement imprévisible.</span><span class="sxs-lookup"><span data-stu-id="99aaf-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="99aaf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99aaf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99aaf-119">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="99aaf-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



