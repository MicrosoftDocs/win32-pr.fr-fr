---
description: La propriété Privileged indique si l’installation est effectuée dans le contexte de privilèges élevés.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Privileged, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535395"
---
# <a name="privileged-property"></a><span data-ttu-id="eb028-103">Privileged, propriété</span><span class="sxs-lookup"><span data-stu-id="eb028-103">Privileged property</span></span>

<span data-ttu-id="eb028-104">La propriété **Privileged** indique si l’installation est effectuée dans le contexte de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="eb028-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="eb028-105">Le programme d’installation définit cette propriété si l’utilisateur dispose de privilèges d’administrateur, si l’application a été affectée par un administrateur système, ou si les stratégies d’utilisateur et d’ordinateur AlwaysInstallElevated a sont définies sur true.</span><span class="sxs-lookup"><span data-stu-id="eb028-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="eb028-106">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="eb028-106">Default Value</span></span>

<span data-ttu-id="eb028-107">Le programme d’installation ne définit pas cette propriété si l’utilisateur n’est pas autorisé à installer avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="eb028-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb028-108">Notes</span><span class="sxs-lookup"><span data-stu-id="eb028-108">Remarks</span></span>

<span data-ttu-id="eb028-109">Les développeurs de packages d’installation peuvent utiliser la propriété **Privileged** pour rendre l’installation conditionnelle sur la stratégie système, sur l’utilisateur en tant qu’administrateur ou sur une attribution par un administrateur.</span><span class="sxs-lookup"><span data-stu-id="eb028-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="eb028-110">En cas d’exécution sur Windows Vista, les **privilèges** et les [**adminuser**](adminuser.md) sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="eb028-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb028-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb028-111">Requirements</span></span>



| <span data-ttu-id="eb028-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb028-112">Requirement</span></span> | <span data-ttu-id="eb028-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb028-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb028-114">Version</span><span class="sxs-lookup"><span data-stu-id="eb028-114">Version</span></span><br/> | <span data-ttu-id="eb028-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eb028-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eb028-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb028-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eb028-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb028-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="eb028-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="eb028-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb028-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb028-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb028-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eb028-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




