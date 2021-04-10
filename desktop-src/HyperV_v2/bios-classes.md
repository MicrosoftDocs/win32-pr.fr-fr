---
description: Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique. Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classes BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952052"
---
# <a name="bios-classes"></a><span data-ttu-id="cea6c-104">Classes BIOS</span><span class="sxs-lookup"><span data-stu-id="cea6c-104">BIOS classes</span></span>

<span data-ttu-id="cea6c-105">Le BIOS virtuel est une image logicielle qui est chargée dans la mémoire RAM pour configurer certains des aspects de base de et démarrer un système informatique.</span><span class="sxs-lookup"><span data-stu-id="cea6c-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="cea6c-106">Il y a un seul élément BIOS par système informatique et cet élément ne peut pas être remplacé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="cea6c-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="cea6c-107">Par conséquent, il n’existe pas de pool de ressources pour l’ajout de nouveaux éléments BIOS à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="cea6c-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="cea6c-108">L’élément BIOS n’a pas non plus sa propre classe SettingData pour décrire les paramètres du BIOS.</span><span class="sxs-lookup"><span data-stu-id="cea6c-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="cea6c-109">Les paramètres du BIOS, tels que les numéros de série, l’ordre de démarrage et l’état VERR. num, se trouvent dans la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="cea6c-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="cea6c-110">Voici les classes WMI de virtualisation associées au BIOS.</span><span class="sxs-lookup"><span data-stu-id="cea6c-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="cea6c-111">Ces classes se trouvent dans le \\ \\ . \\ \\Espace de noms de virtualisation racine.</span><span class="sxs-lookup"><span data-stu-id="cea6c-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cea6c-112">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="cea6c-112">In this section</span></span>



| <span data-ttu-id="cea6c-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="cea6c-113">Topic</span></span>                                                    | <span data-ttu-id="cea6c-114">Description</span><span class="sxs-lookup"><span data-stu-id="cea6c-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cea6c-115">**MSVM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="cea6c-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="cea6c-116">Représente le logiciel de bas niveau qui est chargé dans la mémoire RAM pour configurer et démarrer le système.</span><span class="sxs-lookup"><span data-stu-id="cea6c-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="cea6c-117">**MSVM \_ SystemBIOS**</span><span class="sxs-lookup"><span data-stu-id="cea6c-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="cea6c-118">Utilisé pour associer un ordinateur virtuel à son BIOS.</span><span class="sxs-lookup"><span data-stu-id="cea6c-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




