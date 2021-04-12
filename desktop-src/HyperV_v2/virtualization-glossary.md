---
description: Glossaire des termes utilisés dans la documentation du kit de développement logiciel (SDK) de virtualisation Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glossaire Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210058"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="efafc-103">Glossaire Hyper-V</span><span class="sxs-lookup"><span data-stu-id="efafc-103">Hyper-V glossary</span></span>

<span data-ttu-id="efafc-104">Cette rubrique fournit un glossaire des termes utilisés dans la documentation du kit de développement logiciel (SDK) de virtualisation Windows.</span><span class="sxs-lookup"><span data-stu-id="efafc-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="efafc-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**liant**</span><span class="sxs-lookup"><span data-stu-id="efafc-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-106">Processus par lequel les services logiciels et les couches sont liés entre eux.</span><span class="sxs-lookup"><span data-stu-id="efafc-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="efafc-107">Lors de l’installation d’un service réseau, les relations de liaison et les dépendances des services sont établies.</span><span class="sxs-lookup"><span data-stu-id="efafc-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**contrôler**</span><span class="sxs-lookup"><span data-stu-id="efafc-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-109">Instantané d’un ordinateur virtuel qui permet à un administrateur de restaurer l’ordinateur virtuel à son état au moment où le point de contrôle a été créé.</span><span class="sxs-lookup"><span data-stu-id="efafc-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**ROM**</span><span class="sxs-lookup"><span data-stu-id="efafc-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-111">Pour réduire la taille d’un disque dur virtuel à extension dynamique en supprimant l’espace inutilisé du fichier. vhd.</span><span class="sxs-lookup"><span data-stu-id="efafc-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disque dur virtuel de différenciation**</span><span class="sxs-lookup"><span data-stu-id="efafc-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-113">Disque dur virtuel qui stocke les modifications apportées à un disque dur virtuel parent associé afin de conserver le parent intact.</span><span class="sxs-lookup"><span data-stu-id="efafc-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="efafc-114">Le disque de différenciation est un fichier. vhd distinct qui est associé au fichier. vhd du disque parent.</span><span class="sxs-lookup"><span data-stu-id="efafc-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="efafc-115">Les modifications continuent à s’accumuler sur le disque de différenciation jusqu’à ce qu’elles soient fusionnées sur le disque parent.</span><span class="sxs-lookup"><span data-stu-id="efafc-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disque dur virtuel de taille dynamique**</span><span class="sxs-lookup"><span data-stu-id="efafc-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-117">Disque dur virtuel dont la taille augmente chaque fois qu’il est modifié.</span><span class="sxs-lookup"><span data-stu-id="efafc-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="efafc-118">Ce type de disque dur virtuel démarre en tant que fichier. vhd de 3 Ko et peut croître jusqu’à la taille maximale spécifiée lors de la création du fichier.</span><span class="sxs-lookup"><span data-stu-id="efafc-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="efafc-119">La seule façon de réduire la taille du fichier consiste à supprimer la valeur zéro des données supprimées, puis à compacter le disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="efafc-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disque dur virtuel de taille fixe**</span><span class="sxs-lookup"><span data-stu-id="efafc-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-121">Un disque dur virtuel d’une taille fixe déterminée et pour lequel tout l’espace est alloué lors de la création du disque.</span><span class="sxs-lookup"><span data-stu-id="efafc-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="efafc-122">La taille du disque ne change pas lorsque des données sont ajoutées ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="efafc-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Ordinateur virtuel de génération 1**</span><span class="sxs-lookup"><span data-stu-id="efafc-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-124">Une machine virtuelle (VM) qui contient le même matériel virtuel présent dans les versions d’Hyper-V antérieures à Windows 8.1 et Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="efafc-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="efafc-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Ordinateur virtuel de génération 2**</span><span class="sxs-lookup"><span data-stu-id="efafc-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-126">Machine virtuelle qui contient un modèle de matériel virtuel simplifié et utilise le microprogramme UEFI au lieu du BIOS.</span><span class="sxs-lookup"><span data-stu-id="efafc-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="efafc-127">Dans cette machine virtuelle, la plupart des appareils émulés sont supprimés, ce qui réduit la complexité de la gestion et la surface d’attaque de sécurité.</span><span class="sxs-lookup"><span data-stu-id="efafc-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**système d’exploitation invité**</span><span class="sxs-lookup"><span data-stu-id="efafc-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-129">Système d’exploitation qui s'exécute sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="efafc-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**services d’intégration**</span><span class="sxs-lookup"><span data-stu-id="efafc-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-131">Ensemble de services et de pilotes logiciels qui optimisent les performances et offrent une meilleure expérience utilisateur au sein d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="efafc-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="efafc-132">Les services d’intégration sont uniquement disponibles pour les systèmes d’exploitation invités pris en charge.</span><span class="sxs-lookup"><span data-stu-id="efafc-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**paire clé-valeur**</span><span class="sxs-lookup"><span data-stu-id="efafc-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-134">Ensemble d’éléments de données qui contient un identificateur unique, appelé clé, et une valeur qui correspond aux données réelles de la clé.</span><span class="sxs-lookup"><span data-stu-id="efafc-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**ordinateur physique**</span><span class="sxs-lookup"><span data-stu-id="efafc-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-136">Un ordinateur basé sur le matériel, par opposition à un ordinateur virtuel basé sur un logiciel.</span><span class="sxs-lookup"><span data-stu-id="efafc-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**état enregistré**</span><span class="sxs-lookup"><span data-stu-id="efafc-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-138">Méthode de stockage d’une machine virtuelle pour qu’elle puisse être reprise rapidement, similaire à un ordinateur portable en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="efafc-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="efafc-139">Lorsque vous placez un ordinateur virtuel en cours d’exécution dans un état enregistré, Virtual Server et Hyper-V arrêtent l’ordinateur virtuel, écrivent les données qui existent en mémoire dans des fichiers temporaires et arrêtent la consommation des ressources système.</span><span class="sxs-lookup"><span data-stu-id="efafc-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="efafc-140">La restauration d’un ordinateur virtuel à partir d’un état enregistré le renvoie dans la même condition que celle dans laquelle il se trouvait lors de l’enregistrement de son état.</span><span class="sxs-lookup"><span data-stu-id="efafc-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquette virtuelle**</span><span class="sxs-lookup"><span data-stu-id="efafc-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-142">Version fichier d'une disquette physique.</span><span class="sxs-lookup"><span data-stu-id="efafc-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="efafc-143">Une disquette virtuelle est stockée sous la forme d’un fichier avec une extension de nom de fichier. vfd.</span><span class="sxs-lookup"><span data-stu-id="efafc-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disque dur virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-145">Le support de stockage pour une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="efafc-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="efafc-146">Il peut résider sur n’importe quelle topologie de stockage à laquelle le système d’exploitation hôte peut accéder, y compris les périphériques externes, les réseaux de zone de stockage et le stockage connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="efafc-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="efafc-147">L’extension de nom de fichier est. vhd.</span><span class="sxs-lookup"><span data-stu-id="efafc-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**ordinateur virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-149">Un ordinateur au sein d’un ordinateur, implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="efafc-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="efafc-150">Un ordinateur virtuel émule un système matériel complet, du processeur à la carte réseau, dans un environnement autonome logiciel isolé, ce qui permet d'exécuter plusieurs systèmes d'exploitation incompatibles les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="efafc-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="efafc-151">Chaque système d’exploitation enfant s’exécute dans sa propre machine virtuelle logicielle isolée.</span><span class="sxs-lookup"><span data-stu-id="efafc-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuration de la machine virtuelle**</span><span class="sxs-lookup"><span data-stu-id="efafc-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-153">Configuration des ressources affectées à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="efafc-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="efafc-154">Il peut s’agir d’appareils tels que des disques et des cartes réseau, ainsi que de la mémoire et des processeurs.</span><span class="sxs-lookup"><span data-stu-id="efafc-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Service de gestion d’ordinateurs virtuels**</span><span class="sxs-lookup"><span data-stu-id="efafc-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-156">Service Hyper-V qui fournit un accès de gestion aux ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="efafc-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**capture instantanée d’ordinateur virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-158">Instantané basé sur des fichiers de l’État, des données de disque et de la configuration d’un ordinateur virtuel à un moment précis dans le temps.</span><span class="sxs-lookup"><span data-stu-id="efafc-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**réseau virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-160">Version virtuelle d’un commutateur de réseau physique.</span><span class="sxs-lookup"><span data-stu-id="efafc-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="efafc-161">Il est possible de configurer un réseau virtuel pour fournir à un ou plusieurs ordinateurs virtuels un accès à des ressources locales ou réseau externes.</span><span class="sxs-lookup"><span data-stu-id="efafc-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gestionnaire de réseau virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-163">Service Hyper-V utilisé pour créer et gérer des réseaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="efafc-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**commutateur virtuel**</span><span class="sxs-lookup"><span data-stu-id="efafc-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-165">Consultez réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="efafc-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="efafc-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Redimensionnement VHDX**</span><span class="sxs-lookup"><span data-stu-id="efafc-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="efafc-167">Opération qui réduit ou développe un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="efafc-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



