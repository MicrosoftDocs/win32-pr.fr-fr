---
description: La propriété MSIDEPLOYMENTCOMPLIANT peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au contrôle de compte d’utilisateur (UAC) dans Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriété MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540518"
---
# <a name="msideploymentcompliant-property"></a><span data-ttu-id="bbbf7-103">Propriété MSIDEPLOYMENTCOMPLIANT</span><span class="sxs-lookup"><span data-stu-id="bbbf7-103">MSIDEPLOYMENTCOMPLIANT property</span></span>

<span data-ttu-id="bbbf7-104">La propriété **MSIDEPLOYMENTCOMPLIANT** peut être définie pour indiquer au programme d’installation que le package a été créé et testé pour se conformer au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-104">The **MSIDEPLOYMENTCOMPLIANT** property can be set to indicate to the installer that the package has been authored and tested to comply with [*User Account Control*](u-gly.md) (UAC) in Windows Vista.</span></span> <span data-ttu-id="bbbf7-105">Si cette propriété n’est pas définie, le programme d’installation détermine si le package est conforme au contrôle de compte d’utilisateur sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-105">If this property is not set, the installer will determine whether the package complies with UAC on Windows Vista.</span></span>

<span data-ttu-id="bbbf7-106">Pour plus d’informations sur le contrôle de compte d’utilisateur et la Windows Installer, consultez [utilisation de Windows Installer avec UAC](using-windows-installer-with-uac.md) et [instructions pour les packages](guidelines-for-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bbbf7-106">For more information about UAC and Windows Installer, see [Using Windows Installer with UAC](using-windows-installer-with-uac.md) and [Guidelines for Packages](guidelines-for-packages.md).</span></span>

<span data-ttu-id="bbbf7-107">**Windows Installer 3,1, Windows Installer 3,0 et Windows Installer 2,0 :** Cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-107">**Windows Installer 3.1, Windows Installer 3.0 and Windows Installer 2.0:** This property is ignored.</span></span> <span data-ttu-id="bbbf7-108">Cette propriété est utilisée uniquement par Windows Installer 4,0 dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-108">This property is only used by Windows Installer 4.0 in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbbf7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbbf7-109">Requirements</span></span>



| <span data-ttu-id="bbbf7-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbbf7-110">Requirement</span></span> | <span data-ttu-id="bbbf7-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbbf7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbbf7-112">Version</span><span class="sxs-lookup"><span data-stu-id="bbbf7-112">Version</span></span><br/> | <span data-ttu-id="bbbf7-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbbf7-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbbf7-115">Pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bbbf7-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbbf7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbbf7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbbf7-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bbbf7-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bbbf7-118">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="bbbf7-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




