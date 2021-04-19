---
description: Le programme d’installation définit la propriété MsiNTProductType pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Propriété MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537568"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="25516-103">Propriété MsiNTProductType</span><span class="sxs-lookup"><span data-stu-id="25516-103">MsiNTProductType property</span></span>

<span data-ttu-id="25516-104">Le programme d’installation définit la propriété **MsiNTProductType** pour les systèmes d’exploitation Windows NT, Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="25516-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="25516-105">Cette propriété indique le type de produit Windows.</span><span class="sxs-lookup"><span data-stu-id="25516-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="25516-106">Pour les systèmes d’exploitation Windows 2000 et versions ultérieures, le programme d’installation définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="25516-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="25516-107">Notez que les valeurs sont les mêmes que celles du champ **wProductType** de la structure [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="25516-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="25516-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="25516-108">Value</span></span> | <span data-ttu-id="25516-109">Signification</span><span class="sxs-lookup"><span data-stu-id="25516-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="25516-110">1</span><span class="sxs-lookup"><span data-stu-id="25516-110">1</span></span>     | <span data-ttu-id="25516-111">Windows 2000 professionnel et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="25516-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="25516-112">2</span><span class="sxs-lookup"><span data-stu-id="25516-112">2</span></span>     | <span data-ttu-id="25516-113">Contrôleur de domaine Windows 2000 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="25516-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="25516-114">3</span><span class="sxs-lookup"><span data-stu-id="25516-114">3</span></span>     | <span data-ttu-id="25516-115">Windows 2000 Server et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="25516-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="25516-116">Pour les systèmes d’exploitation antérieurs à Windows 2000, le programme d’installation définit les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="25516-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="25516-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="25516-117">Value</span></span> | <span data-ttu-id="25516-118">Signification</span><span class="sxs-lookup"><span data-stu-id="25516-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="25516-119">1</span><span class="sxs-lookup"><span data-stu-id="25516-119">1</span></span>     | <span data-ttu-id="25516-120">Station de travail Windows NT</span><span class="sxs-lookup"><span data-stu-id="25516-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="25516-121">2</span><span class="sxs-lookup"><span data-stu-id="25516-121">2</span></span>     | <span data-ttu-id="25516-122">Contrôleur de domaine Windows NT</span><span class="sxs-lookup"><span data-stu-id="25516-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="25516-123">3</span><span class="sxs-lookup"><span data-stu-id="25516-123">3</span></span>     | <span data-ttu-id="25516-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="25516-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="25516-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25516-125">Requirements</span></span>



| <span data-ttu-id="25516-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25516-126">Requirement</span></span> | <span data-ttu-id="25516-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="25516-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25516-128">Version</span><span class="sxs-lookup"><span data-stu-id="25516-128">Version</span></span><br/> | <span data-ttu-id="25516-129">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="25516-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="25516-130">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25516-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="25516-131">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="25516-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="25516-132">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="25516-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25516-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25516-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25516-134">Propriétés</span><span class="sxs-lookup"><span data-stu-id="25516-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
