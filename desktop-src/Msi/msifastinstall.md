---
description: La propriété MSIFASTINSTALL peut être utilisée pour réduire le temps nécessaire à l’installation d’un package de Windows Installer volumineux.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Propriété MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537099"
---
# <a name="msifastinstall-property"></a><span data-ttu-id="9f82d-103">Propriété MSIFASTINSTALL</span><span class="sxs-lookup"><span data-stu-id="9f82d-103">MSIFASTINSTALL property</span></span>

<span data-ttu-id="9f82d-104">La propriété **MSIFASTINSTALL** peut être utilisée pour réduire le temps nécessaire à l’installation d’un package de Windows Installer volumineux.</span><span class="sxs-lookup"><span data-stu-id="9f82d-104">The **MSIFASTINSTALL** property can be used to reduce the time required to install a large Windows Installer package.</span></span> <span data-ttu-id="9f82d-105">La propriété peut être définie sur la ligne de commande ou dans la table de [Propriétés](property-table.md) pour configurer les opérations que l’utilisateur ou le développeur détermine sont non essentielles pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="9f82d-105">The property can be set on the command line or in the [Property](property-table.md) table to configure operations that the user or developer determines are non-essential for the installation.</span></span>

<span data-ttu-id="9f82d-106">La valeur de la propriété **MSIFASTINSTALL** peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f82d-106">The value of the **MSIFASTINSTALL** property can be a combination of the following values.</span></span>



| <span data-ttu-id="9f82d-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f82d-107">Value</span></span> | <span data-ttu-id="9f82d-108">Signification</span><span class="sxs-lookup"><span data-stu-id="9f82d-108">Meaning</span></span>                                                                      |
|-------|------------------------------------------------------------------------------|
| <span data-ttu-id="9f82d-109">0</span><span class="sxs-lookup"><span data-stu-id="9f82d-109">0</span></span>     | <span data-ttu-id="9f82d-110">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="9f82d-110">Default value</span></span>                                                                |
| <span data-ttu-id="9f82d-111">1</span><span class="sxs-lookup"><span data-stu-id="9f82d-111">1</span></span>     | <span data-ttu-id="9f82d-112">Aucun point de restauration système n’est enregistré pour cette installation.</span><span class="sxs-lookup"><span data-stu-id="9f82d-112">No system restore point is saved for this installation.</span></span>                      |
| <span data-ttu-id="9f82d-113">2</span><span class="sxs-lookup"><span data-stu-id="9f82d-113">2</span></span>     | <span data-ttu-id="9f82d-114">Effectuez uniquement les [coûts des fichiers](file-costing.md) et ignorez les autres coûts.</span><span class="sxs-lookup"><span data-stu-id="9f82d-114">Perform only [File Costing](file-costing.md) and skip checking other costs.</span></span> |
| <span data-ttu-id="9f82d-115">4</span><span class="sxs-lookup"><span data-stu-id="9f82d-115">4</span></span>     | <span data-ttu-id="9f82d-116">Réduisez la fréquence des messages de progression.</span><span class="sxs-lookup"><span data-stu-id="9f82d-116">Reduce the frequency of progress messages.</span></span>                                   |



 

<span data-ttu-id="9f82d-117">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9f82d-117">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="9f82d-118">Cette propriété est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="9f82d-118">This property is available beginning with Windows Installer 5.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f82d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f82d-119">Requirements</span></span>



| <span data-ttu-id="9f82d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f82d-120">Requirement</span></span> | <span data-ttu-id="9f82d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f82d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f82d-122">Version</span><span class="sxs-lookup"><span data-stu-id="9f82d-122">Version</span></span><br/> | <span data-ttu-id="9f82d-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f82d-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f82d-124">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9f82d-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



 

 




