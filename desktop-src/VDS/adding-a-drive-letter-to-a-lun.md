---
description: Ajout d’une lettre de lecteur à un numéro d’unité logique
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Ajout d’une lettre de lecteur à un numéro d’unité logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388c59a2e1b719e792855460f45fa0c04add7502f8e06aba56f0416a212a9aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755498"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Ajout d’une lettre de lecteur à un numéro d’unité logique

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Vous pouvez affecter des lettres de lecteur à des objets de volume directement ; Toutefois, si votre disque est un objet LUN, quelques étapes supplémentaires sont nécessaires.

**Pour affecter une lettre de lecteur à un objet LUN**

1.  Si nécessaire, démasquez le numéro d’unité logique à l’hôte local.
    > [!Note]  
    > Vous ne pouvez pas effectuer d’opérations d’administration logicielle sur un objet LUN qui n’est pas masqué sur un autre ordinateur au sein de la session VDS en cours.

     

2.  Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) sur l’ordinateur qui exécute le fournisseur de matériel.
3.  Initialisez le numéro d’unité logique en tant que disque de base, comme suit :
    1.  Appelez la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet lun pour interroger l’interface [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .
    2.  Appelez la méthode [**IVdsSwProvider :: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) pour créer un pack de base.
    3.  Appelez la méthode [**IVdsPack :: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) pour ajouter le disque au nouveau Pack.
4.  Créez une partition sur le disque et obtenez l’objet volume comme suit :
    1.  Appelez la méthode [**IVdsCreatePartitionEx :: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) pour créer une partition.
    2.  Appelez la méthode [**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) sur l’objet Async retourné par [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) pour récupérer l’identificateur de volume à partir de la structure de [**\_ \_ sortie asynchrone VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .
    3.  Transmettez l’identificateur de volume en tant que paramètre à la méthode [**IVdsService :: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) pour obtenir un pointeur d’objet de volume.
5.  Appelez la méthode [**IVdsVolumeMF :: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) pour affecter la lettre de lecteur.

> [!Note]  
> La méthode [**IVdsAdvancedDisk :: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) affecte des lettres de lecteur à des partitions sans volumes associés, comme des partitions OEM ou ESP. Vous ne pouvez pas l’utiliser pour affecter une lettre de lecteur à un objet LUN.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VDS](using-vds.md)
</dt> <dt>

[**IVdsService :: réénumération**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**\_sortie asynchrone \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
