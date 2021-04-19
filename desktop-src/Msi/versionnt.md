---
description: Le programme d’installation définit la propriété VersionNT sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propriété VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535241"
---
# <a name="versionnt-property"></a><span data-ttu-id="16fd0-103">Propriété VersionNT</span><span class="sxs-lookup"><span data-stu-id="16fd0-103">VersionNT property</span></span>

<span data-ttu-id="16fd0-104">Le programme d’installation définit la propriété **VersionNT** sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16fd0-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="16fd0-105">La valeur est un entier : MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="16fd0-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="16fd0-106">Les instructions conditionnelles qui dépendent du système d’exploitation peuvent utiliser cette propriété.</span><span class="sxs-lookup"><span data-stu-id="16fd0-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="16fd0-107">Voir aussi [valeurs de propriété du système d’exploitation](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="16fd0-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16fd0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="16fd0-108">Remarks</span></span>

<span data-ttu-id="16fd0-109">Les expressions de condition peuvent tester Windows NT, Windows 2000 ou Windows XP en utilisant le nom de propriété, ou peuvent vérifier la version à l’aide d’un opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="16fd0-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="16fd0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16fd0-110">Requirements</span></span>



| <span data-ttu-id="16fd0-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16fd0-111">Requirement</span></span> | <span data-ttu-id="16fd0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="16fd0-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16fd0-113">Version</span><span class="sxs-lookup"><span data-stu-id="16fd0-113">Version</span></span><br/> | <span data-ttu-id="16fd0-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16fd0-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="16fd0-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16fd0-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="16fd0-116">Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="16fd0-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16fd0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16fd0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16fd0-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="16fd0-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




