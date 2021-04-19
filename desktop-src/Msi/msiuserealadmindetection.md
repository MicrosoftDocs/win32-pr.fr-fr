---
description: Affectez à la propriété MSIUSEREALADMINDETECTION la valeur 1 pour demander que le programme d’installation utilise les informations utilisateur réelles lors de la définition de la propriété AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propriété MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544475"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="3bbdd-103">Propriété MSIUSEREALADMINDETECTION</span><span class="sxs-lookup"><span data-stu-id="3bbdd-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="3bbdd-104">Affectez à la propriété **MSIUSEREALADMINDETECTION** la valeur 1 pour demander que le programme d’installation utilise les informations utilisateur réelles lors de la définition de la propriété [**adminuser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbdd-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="3bbdd-105">En cas d’exécution sur Windows Vista, les [**privilèges**](privileged.md) et les **adminuser** sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="3bbdd-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="3bbdd-106">Les auteurs doivent utiliser la propriété **Privileged** dans de nouveaux packages.</span><span class="sxs-lookup"><span data-stu-id="3bbdd-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="3bbdd-107">Les packages hérités qui requièrent des propriétés distinct **Privileged** et **adminuser** peuvent restaurer la différence en définissant la propriété **MSIUSEREALADMINDETECTION** .</span><span class="sxs-lookup"><span data-stu-id="3bbdd-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bbdd-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bbdd-108">Requirements</span></span>



| <span data-ttu-id="3bbdd-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bbdd-109">Requirement</span></span> | <span data-ttu-id="3bbdd-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bbdd-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbdd-111">Version</span><span class="sxs-lookup"><span data-stu-id="3bbdd-111">Version</span></span><br/> | <span data-ttu-id="3bbdd-112">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bbdd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bbdd-113">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bbdd-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bbdd-114">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbdd-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3bbdd-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bbdd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbdd-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3bbdd-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="3bbdd-117">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="3bbdd-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




