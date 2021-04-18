---
description: Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propriété AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526896"
---
# <a name="adminuser-property"></a><span data-ttu-id="8824e-103">Propriété AdminUser</span><span class="sxs-lookup"><span data-stu-id="8824e-103">AdminUser property</span></span>

<span data-ttu-id="8824e-104">Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8824e-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="8824e-105">**Windows Server 2008 et Windows Vista :** La propriété **adminuser** est la même que la propriété [**Privileged**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="8824e-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="8824e-106">Les auteurs doivent utiliser la propriété **Privileged** .</span><span class="sxs-lookup"><span data-stu-id="8824e-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="8824e-107">Le programme d’installation définit ces propriétés si l’utilisateur dispose de privilèges d’administrateur, si l’application a été affectée par un administrateur système, ou si les stratégies d’utilisateur et d’ordinateur AlwaysInstallElevated a sont définies sur true.</span><span class="sxs-lookup"><span data-stu-id="8824e-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="8824e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8824e-108">Remarks</span></span>

<span data-ttu-id="8824e-109">Les différences entre ces propriétés peuvent avoir été utilisées dans certains packages hérités.</span><span class="sxs-lookup"><span data-stu-id="8824e-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="8824e-110">Par exemple, **adminuser** peut avoir été utilisé à la place de [**Privileged**](privileged.md) dans des instructions conditionnelles, car le programme d’installation définit uniquement la propriété **adminuser** si l’utilisateur est un administrateur.</span><span class="sxs-lookup"><span data-stu-id="8824e-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="8824e-111">Le programme d’installation définit la propriété **Privileged** si l’utilisateur est un administrateur ou si la stratégie permet à l’utilisateur d’installer avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="8824e-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="8824e-112">**Windows Server 2008 et Windows Vista :** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8824e-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="8824e-113">Les [**privilèges**](privileged.md) et les **adminuser** sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="8824e-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="8824e-114">Les packages qui requièrent des propriétés distinctes **privilégiées** et **adminuser** peuvent restaurer la différence en définissant la propriété [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .</span><span class="sxs-lookup"><span data-stu-id="8824e-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="8824e-115">Pour plus d’informations, consultez [installation d’un package avec des privilèges élevés pour une propriété non-administrateur](installing-a-package-with-elevated-privileges-for-a-non-admin.md)et [**privilégié**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="8824e-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8824e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8824e-116">Requirements</span></span>



| <span data-ttu-id="8824e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8824e-117">Requirement</span></span> | <span data-ttu-id="8824e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8824e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8824e-119">Version</span><span class="sxs-lookup"><span data-stu-id="8824e-119">Version</span></span><br/> | <span data-ttu-id="8824e-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8824e-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8824e-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Vista ou Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8824e-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="8824e-122">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8824e-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8824e-123">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8824e-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8824e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8824e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8824e-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8824e-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




