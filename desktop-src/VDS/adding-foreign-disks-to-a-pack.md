---
description: Ajout de disques étrangers à un Pack
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Ajout de disques étrangers à un Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755454"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Ajout de disques étrangers à un Pack

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Le plus souvent, un disque étranger est un disque dynamique qui est alloué sur un ordinateur et physiquement déplacé vers un autre ordinateur. Toutefois, tout disque appartenant à un autre Pack que le Pack en ligne est considéré comme un disque étranger qui appartient à un pack de disques étrangers.

Un pack étranger a l' **indicateur \_ \_ étranger PKF VDS** défini dans le membre **ulFlags** de la structure de la [**\_ \_ prop Pack VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) . Les packs étrangers sont toujours hors connexion.

La procédure suivante décrit comment importer un ou plusieurs disques étrangers.

**Pour importer un ou plusieurs disques étrangers**

1.  Déplacez les disques vers le nouvel ordinateur.
2.  Sur le nouvel ordinateur, utilisez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) pour installer les disques étrangers.
3.  Sélectionnez le Pack en ligne à utiliser pour le Pack cible qui reçoit les disques étrangers. S’il n’existe aucun Pack en ligne, utilisez la méthode [**IVdsSwProvider :: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) pour créer un nouveau Pack vide.
4.  Utilisez la méthode [**IVdsPack :: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) pour importer les disques dans le nouveau Pack dynamique.
5.  Utilisez la méthode [**IVdsSwProvider :: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) pour énumérer les packs et [**IVdsPack :: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) pour déterminer quel Pack est maintenant le Pack en ligne.

Si vous créez un nouveau Pack cible vide, les disques étrangers ne sont pas réellement migrés vers ce Pack. Au lieu de cela, le Pack étranger est marqué en ligne, l’indicateur de l' **\_ \_ étranger PKF VDS** pour le Pack est effacé (par conséquent, le Pack n’est plus étranger) et le Pack cible que vous avez créé est ignoré.

> [!Note]  
> Utilisez la méthode [**IVdsPack :: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) pour ajouter des disques non alloués (disques non revendiqués par un fournisseur) à un Pack. Un disque non alloué ne peut pas être étranger.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VDS](using-vds.md)
</dt> <dt>

[**IVdsService :: réénumération**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
