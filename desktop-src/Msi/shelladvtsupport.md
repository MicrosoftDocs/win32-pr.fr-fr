---
description: La propriété ShellAdvtSupport est définie par le programme d’installation si l’interface IShellLink du système prend en charge la résolution du descripteur du programme d’installation.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propriété ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537322"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="1be2d-103">Propriété ShellAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="1be2d-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="1be2d-104">La propriété **ShellAdvtSupport** est définie par le programme d’installation si l’interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) du système prend en charge la résolution du descripteur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1be2d-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="1be2d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1be2d-105">Remarks</span></span>

<span data-ttu-id="1be2d-106">Si cette propriété est définie, l’interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) du système prend en charge la résolution du descripteur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="1be2d-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="1be2d-107">Cela est pris en charge par Windows 2000 et les systèmes exécutant Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="1be2d-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="1be2d-108">Si cette propriété n’est pas définie, le programme d’installation a le comportement par défaut de création de fonctionnalités non publiées lors de l’installation, soit localement, soit à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="1be2d-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be2d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1be2d-109">Requirements</span></span>



| <span data-ttu-id="1be2d-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1be2d-110">Requirement</span></span> | <span data-ttu-id="1be2d-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1be2d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be2d-112">Version</span><span class="sxs-lookup"><span data-stu-id="1be2d-112">Version</span></span><br/> | <span data-ttu-id="1be2d-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1be2d-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1be2d-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1be2d-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1be2d-115">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1be2d-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1be2d-116">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1be2d-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1be2d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1be2d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be2d-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1be2d-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1be2d-119">Prise en charge des plateformes de la publication</span><span class="sxs-lookup"><span data-stu-id="1be2d-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
