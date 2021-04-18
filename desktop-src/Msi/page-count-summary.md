---
description: La propriété Résumé du nombre de pages contient la version minimale du programme d’installation requise par le package d’installation.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propriété du résumé du nombre de pages
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533129"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="a2405-103">Propriété du résumé du nombre de pages</span><span class="sxs-lookup"><span data-stu-id="a2405-103">Page Count Summary property</span></span>

<span data-ttu-id="a2405-104">La propriété **Résumé du nombre de pages** contient la version minimale du programme d’installation requise par le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="a2405-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="a2405-105">Pour un minimum de Windows Installer 2,0, cette propriété doit être définie sur l’entier 200.</span><span class="sxs-lookup"><span data-stu-id="a2405-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="a2405-106">Pour un minimum de Windows Installer 3,0, cette propriété doit être définie sur l’entier 300.</span><span class="sxs-lookup"><span data-stu-id="a2405-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="a2405-107">Pour un minimum de Windows Installer 3,1, cette propriété doit être définie sur 301.</span><span class="sxs-lookup"><span data-stu-id="a2405-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="a2405-108">Pour un minimum de Windows Installer 4,5, cette propriété doit être définie sur 405.</span><span class="sxs-lookup"><span data-stu-id="a2405-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="a2405-109">Pour un minimum de Windows Installer 5,0, cette propriété doit être définie sur 500.</span><span class="sxs-lookup"><span data-stu-id="a2405-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="a2405-110">Pour les [Packages Windows Installers 64 bits](64-bit-windows-installer-packages.md), cette propriété doit être définie sur l’entier 200 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="a2405-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="a2405-111">Pour les packages de Windows Installer 64 bits sur la plateforme Arm64, cette propriété doit être définie sur l’entier 500 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="a2405-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="a2405-112">Pour un package de transformation, la propriété **Résumé du nombre de pages** contient la version minimale du programme d’installation requise pour traiter la transformation.</span><span class="sxs-lookup"><span data-stu-id="a2405-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="a2405-113">Défini sur la plus grande des deux valeurs de propriété **récapitulatives du nombre de pages** qui appartiennent aux bases de données utilisées pour générer la transformation.</span><span class="sxs-lookup"><span data-stu-id="a2405-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="a2405-114">Pour un package de correctifs, la propriété de **Résumé du nombre de pages** est définie sur null.</span><span class="sxs-lookup"><span data-stu-id="a2405-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="a2405-115">Cette propriété de résumé est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a2405-115">This summary property is required.</span></span>

<span data-ttu-id="a2405-116">Cette propriété peut être utilisée pour créer un package qui ne peut être installé que par la version minimale ou ultérieure spécifiée du Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a2405-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2405-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2405-117">Requirements</span></span>



| <span data-ttu-id="a2405-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2405-118">Requirement</span></span> | <span data-ttu-id="a2405-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2405-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2405-120">Version</span><span class="sxs-lookup"><span data-stu-id="a2405-120">Version</span></span><br/> | <span data-ttu-id="a2405-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a2405-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a2405-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2405-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a2405-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2405-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2405-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2405-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2405-125">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="a2405-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




