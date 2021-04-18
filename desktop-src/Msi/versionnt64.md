---
description: Le programme d’installation définit la propriété VersionNT64 sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriété VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526043"
---
# <a name="versionnt64-property"></a><span data-ttu-id="d2442-103">Propriété VersionNT64</span><span class="sxs-lookup"><span data-stu-id="d2442-103">VersionNT64 property</span></span>

<span data-ttu-id="d2442-104">Le programme d’installation définit la propriété **VersionNT64** sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d2442-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="d2442-105">La propriété n’est pas définie si le système d’exploitation n’est pas 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d2442-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="d2442-106">La valeur est un entier : MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="d2442-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="d2442-107">Pour des raisons de compatibilité, la propriété est également non définie si la propriété [**Résumé du modèle**](template-summary.md) indique que le package est destiné aux systèmes Intel 32 bits et que le système d’exploitation est une architecture 64 bits qui n’est pas Intel64 ou x64 (comme ARM64).</span><span class="sxs-lookup"><span data-stu-id="d2442-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel systems and the operating system is a 64-bit architecture that is not Intel64 or x64 (such as ARM64).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2442-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d2442-108">Remarks</span></span>

<span data-ttu-id="d2442-109">Les expressions conditionnelles testent les fenêtres 64 bits simplement en utilisant le nom de la propriété ou en vérifiant la version à l’aide d’un opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="d2442-109">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2442-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2442-110">Requirements</span></span>



| <span data-ttu-id="d2442-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2442-111">Requirement</span></span> | <span data-ttu-id="d2442-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2442-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2442-113">Version</span><span class="sxs-lookup"><span data-stu-id="d2442-113">Version</span></span><br/> | <span data-ttu-id="d2442-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d2442-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d2442-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d2442-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d2442-116">Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d2442-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2442-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2442-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2442-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2442-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




