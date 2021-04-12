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
# <a name="hyper-v-glossary"></a>Glossaire Hyper-V

Cette rubrique fournit un glossaire des termes utilisés dans la documentation du kit de développement logiciel (SDK) de virtualisation Windows.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**liant**
</dt> <dd>

Processus par lequel les services logiciels et les couches sont liés entre eux. Lors de l’installation d’un service réseau, les relations de liaison et les dépendances des services sont établies.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**contrôler**
</dt> <dd>

Instantané d’un ordinateur virtuel qui permet à un administrateur de restaurer l’ordinateur virtuel à son état au moment où le point de contrôle a été créé.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**ROM**
</dt> <dd>

Pour réduire la taille d’un disque dur virtuel à extension dynamique en supprimant l’espace inutilisé du fichier. vhd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disque dur virtuel de différenciation**
</dt> <dd>

Disque dur virtuel qui stocke les modifications apportées à un disque dur virtuel parent associé afin de conserver le parent intact. Le disque de différenciation est un fichier. vhd distinct qui est associé au fichier. vhd du disque parent. Les modifications continuent à s’accumuler sur le disque de différenciation jusqu’à ce qu’elles soient fusionnées sur le disque parent.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disque dur virtuel de taille dynamique**
</dt> <dd>

Disque dur virtuel dont la taille augmente chaque fois qu’il est modifié. Ce type de disque dur virtuel démarre en tant que fichier. vhd de 3 Ko et peut croître jusqu’à la taille maximale spécifiée lors de la création du fichier. La seule façon de réduire la taille du fichier consiste à supprimer la valeur zéro des données supprimées, puis à compacter le disque dur virtuel.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disque dur virtuel de taille fixe**
</dt> <dd>

Un disque dur virtuel d’une taille fixe déterminée et pour lequel tout l’espace est alloué lors de la création du disque. La taille du disque ne change pas lorsque des données sont ajoutées ou supprimées.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Ordinateur virtuel de génération 1**
</dt> <dd>

Une machine virtuelle (VM) qui contient le même matériel virtuel présent dans les versions d’Hyper-V antérieures à Windows 8.1 et Windows Server 2012 R2

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Ordinateur virtuel de génération 2**
</dt> <dd>

Machine virtuelle qui contient un modèle de matériel virtuel simplifié et utilise le microprogramme UEFI au lieu du BIOS. Dans cette machine virtuelle, la plupart des appareils émulés sont supprimés, ce qui réduit la complexité de la gestion et la surface d’attaque de sécurité.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**système d’exploitation invité**
</dt> <dd>

Système d’exploitation qui s'exécute sur un ordinateur virtuel.

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**services d’intégration**
</dt> <dd>

Ensemble de services et de pilotes logiciels qui optimisent les performances et offrent une meilleure expérience utilisateur au sein d’une machine virtuelle. Les services d’intégration sont uniquement disponibles pour les systèmes d’exploitation invités pris en charge.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**paire clé-valeur**
</dt> <dd>

Ensemble d’éléments de données qui contient un identificateur unique, appelé clé, et une valeur qui correspond aux données réelles de la clé.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**ordinateur physique**
</dt> <dd>

Un ordinateur basé sur le matériel, par opposition à un ordinateur virtuel basé sur un logiciel.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**état enregistré**
</dt> <dd>

Méthode de stockage d’une machine virtuelle pour qu’elle puisse être reprise rapidement, similaire à un ordinateur portable en veille prolongée. Lorsque vous placez un ordinateur virtuel en cours d’exécution dans un état enregistré, Virtual Server et Hyper-V arrêtent l’ordinateur virtuel, écrivent les données qui existent en mémoire dans des fichiers temporaires et arrêtent la consommation des ressources système. La restauration d’un ordinateur virtuel à partir d’un état enregistré le renvoie dans la même condition que celle dans laquelle il se trouvait lors de l’enregistrement de son état.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquette virtuelle**
</dt> <dd>

Version fichier d'une disquette physique. Une disquette virtuelle est stockée sous la forme d’un fichier avec une extension de nom de fichier. vfd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disque dur virtuel**
</dt> <dd>

Le support de stockage pour une machine virtuelle. Il peut résider sur n’importe quelle topologie de stockage à laquelle le système d’exploitation hôte peut accéder, y compris les périphériques externes, les réseaux de zone de stockage et le stockage connecté au réseau. L’extension de nom de fichier est. vhd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**ordinateur virtuel**
</dt> <dd>

Un ordinateur au sein d’un ordinateur, implémenté dans le logiciel. Un ordinateur virtuel émule un système matériel complet, du processeur à la carte réseau, dans un environnement autonome logiciel isolé, ce qui permet d'exécuter plusieurs systèmes d'exploitation incompatibles les uns avec les autres. Chaque système d’exploitation enfant s’exécute dans sa propre machine virtuelle logicielle isolée.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuration de la machine virtuelle**
</dt> <dd>

Configuration des ressources affectées à un ordinateur virtuel. Il peut s’agir d’appareils tels que des disques et des cartes réseau, ainsi que de la mémoire et des processeurs.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Service de gestion d’ordinateurs virtuels**
</dt> <dd>

Service Hyper-V qui fournit un accès de gestion aux ordinateurs virtuels.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**capture instantanée d’ordinateur virtuel**
</dt> <dd>

Instantané basé sur des fichiers de l’État, des données de disque et de la configuration d’un ordinateur virtuel à un moment précis dans le temps.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**réseau virtuel**
</dt> <dd>

Version virtuelle d’un commutateur de réseau physique. Il est possible de configurer un réseau virtuel pour fournir à un ou plusieurs ordinateurs virtuels un accès à des ressources locales ou réseau externes.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gestionnaire de réseau virtuel**
</dt> <dd>

Service Hyper-V utilisé pour créer et gérer des réseaux virtuels.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**commutateur virtuel**
</dt> <dd>

Consultez réseau virtuel.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Redimensionnement VHDX**
</dt> <dd>

Opération qui réduit ou développe un disque dur virtuel.

</dd> </dl>

 

 



