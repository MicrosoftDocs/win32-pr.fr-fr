---
description: Le programme d’installation définit la propriété VersionNT64 sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriété VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262071"
---
# <a name="versionnt64-property"></a><span data-ttu-id="416bc-103">Propriété VersionNT64</span><span class="sxs-lookup"><span data-stu-id="416bc-103">VersionNT64 property</span></span>

<span data-ttu-id="416bc-104">Le programme d’installation définit la propriété **VersionNT64** sur le numéro de version du système d’exploitation uniquement si le système s’exécute sur un ordinateur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="416bc-104">The installer sets the **VersionNT64** property to the version number for the operating system only if the system is running on a 64-bit computer.</span></span> <span data-ttu-id="416bc-105">La propriété n’est pas définie si le système d’exploitation n’est pas 64 bits.</span><span class="sxs-lookup"><span data-stu-id="416bc-105">The property is undefined if the operating system is not 64-bit.</span></span>

<span data-ttu-id="416bc-106">La valeur est un entier : MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="416bc-106">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="416bc-107">Pour des raisons de compatibilité, la propriété est également non définie si la propriété [**Résumé du modèle**](template-summary.md) indique que le package est destiné aux systèmes Intel (x86) 32 bits et que le système d’exploitation ne peut pas exécuter le code Intel (x64) 64 bits, tel que Windows 10 sur ARM (ARM64).</span><span class="sxs-lookup"><span data-stu-id="416bc-107">For compatibility reasons, the property is also undefined if the [**Template Summary**](template-summary.md) property indicates the package is for 32-bit Intel (x86) systems and the operating system cannot run 64-bit Intel (x64) code, such as Windows 10 on ARM (ARM64).</span></span>

> [!NOTE]
> <span data-ttu-id="416bc-108">À compter de Windows 10 Build 21277, ARM64 est généré dans le canal de développement du programme Windows Insider Preview, qui prend en charge les applications x64.</span><span class="sxs-lookup"><span data-stu-id="416bc-108">As of Windows 10 Build 21277, ARM64 builds in the Dev channel of the Windows Insider Preview program have support for x64 applications.</span></span> <span data-ttu-id="416bc-109">Sur ces builds ARM64, la propriété VersionNT64 est définie pour les packages x86.</span><span class="sxs-lookup"><span data-stu-id="416bc-109">On these ARM64 builds, the VersionNT64 property is defined for x86 packages.</span></span>

## <a name="remarks"></a><span data-ttu-id="416bc-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="416bc-110">Remarks</span></span>

<span data-ttu-id="416bc-111">Les expressions conditionnelles testent les fenêtres 64 bits simplement en utilisant le nom de la propriété ou en vérifiant la version à l’aide d’un opérateur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="416bc-111">Conditional expressions test for 64-bit Windows simply by using the property name, or by verifying the version using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="416bc-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="416bc-112">Requirements</span></span>



| <span data-ttu-id="416bc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="416bc-113">Requirement</span></span> | <span data-ttu-id="416bc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="416bc-114">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416bc-115">Version</span><span class="sxs-lookup"><span data-stu-id="416bc-115">Version</span></span><br/> | <span data-ttu-id="416bc-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="416bc-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="416bc-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="416bc-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="416bc-118">Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="416bc-118">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="416bc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="416bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416bc-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="416bc-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




