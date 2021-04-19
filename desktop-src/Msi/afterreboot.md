---
description: Le programme d’installation affecte la valeur 1 à la propriété AFTERREBOOT après un redémarrage appelé par l’action ForceReboot. Le programme d’installation ajoute AFTERREBOOT = 1 à la ligne de commande exécutée immédiatement après le redémarrage.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propriété AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541691"
---
# <a name="afterreboot-property"></a><span data-ttu-id="58b28-104">Propriété AFTERREBOOT</span><span class="sxs-lookup"><span data-stu-id="58b28-104">AFTERREBOOT property</span></span>

<span data-ttu-id="58b28-105">Le programme d’installation affecte la valeur 1 à la propriété **AFTERREBOOT** après un redémarrage appelé par l' [action ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="58b28-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="58b28-106">Le programme d’installation ajoute AFTERREBOOT = 1 à la ligne de commande exécutée immédiatement après le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="58b28-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b28-107">Notes</span><span class="sxs-lookup"><span data-stu-id="58b28-107">Remarks</span></span>

<span data-ttu-id="58b28-108">L' [action ForceReboot](forcereboot-action.md) doit toujours être utilisée avec une instruction conditionnelle de sorte que le programme d’installation déclenche un redémarrage uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58b28-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="58b28-109">Un redémarrage peut être nécessaire si un fichier particulier a été remplacé ou si un composant particulier a été installé.</span><span class="sxs-lookup"><span data-stu-id="58b28-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="58b28-110">Le cas est différent pour chaque produit et une action personnalisée peut être nécessaire pour déterminer si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58b28-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="58b28-111">La condition sur l’action ForceReboot utilise généralement la propriété **AFTERREBOOT** .</span><span class="sxs-lookup"><span data-stu-id="58b28-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="58b28-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58b28-112">Requirements</span></span>



| <span data-ttu-id="58b28-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58b28-113">Requirement</span></span> | <span data-ttu-id="58b28-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="58b28-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b28-115">Version</span><span class="sxs-lookup"><span data-stu-id="58b28-115">Version</span></span><br/> | <span data-ttu-id="58b28-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="58b28-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="58b28-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="58b28-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="58b28-118">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58b28-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="58b28-119">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="58b28-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58b28-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58b28-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b28-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58b28-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="58b28-122">Redémarrages du système</span><span class="sxs-lookup"><span data-stu-id="58b28-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




