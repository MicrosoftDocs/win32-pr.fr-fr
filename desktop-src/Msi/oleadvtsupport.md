---
description: Le programme d’installation définit la propriété OLEAdvtSupport sur true lorsque le système de l’utilisateur actuel a été mis à niveau pour fonctionner avec l’installation à la demande via COM.
ms.assetid: 274d7658-3d33-4c3a-987c-878cbd5bf821
title: Propriété OLEAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c9bd8f5ecaaa2690654211a2dd7ecdc5e9ef2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535921"
---
# <a name="oleadvtsupport-property"></a><span data-ttu-id="6129b-103">Propriété OLEAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="6129b-103">OLEAdvtSupport property</span></span>

<span data-ttu-id="6129b-104">Le programme d’installation définit la propriété **OLEAdvtSupport** sur true lorsque le système de l’utilisateur actuel a été mis à niveau pour fonctionner avec l’installation à la demande via com.</span><span class="sxs-lookup"><span data-stu-id="6129b-104">The installer sets the **OLEAdvtSupport** property to true when the current user's system has been upgraded to work with installation-on-demand through COM.</span></span> <span data-ttu-id="6129b-105">Notez que pour que le programme d’installation enregistre une classe COM et active l’installation à la demande, la classe doit être listée dans les tables [Class](class-table.md) et [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6129b-105">Note that for the installer to register a COM class and enable installation-on-demand, the class must be listed in the [Class](class-table.md) and [ProgId](progid-table.md) tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="6129b-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6129b-106">Requirements</span></span>



| <span data-ttu-id="6129b-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6129b-107">Requirement</span></span> | <span data-ttu-id="6129b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="6129b-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6129b-109">Version</span><span class="sxs-lookup"><span data-stu-id="6129b-109">Version</span></span><br/> | <span data-ttu-id="6129b-110">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6129b-110">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6129b-111">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6129b-111">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6129b-112">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6129b-112">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6129b-113">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6129b-113">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6129b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6129b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6129b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6129b-115">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6129b-116">**Propriété ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="6129b-116">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> <dt>

[<span data-ttu-id="6129b-117">Prise en charge des plateformes de la publication</span><span class="sxs-lookup"><span data-stu-id="6129b-117">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 




