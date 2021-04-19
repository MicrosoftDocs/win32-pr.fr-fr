---
description: Réénumération et actualisation
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Réénumération et actualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528157"
---
# <a name="reenumerating-and-refreshing"></a>Réénumération et actualisation

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L’opération de réénumération Découvre les appareils qui viennent d’être connectés et qui viennent d’être déconnectés. L’opération d’actualisation met à jour les informations de configuration des appareils existants.

**Pour réénumérer les objets du fournisseur de logiciels**

-   Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) . Cette méthode Découvre tous les disques récemment connectés et déconnectés et les lecteurs de CD-ROM, et garantit que tous les disques possèdent le propriétaire approprié. VDS possède des disques bruts ou des disques défaillants ; le fournisseur de base possède des disques de base ; et le fournisseur dynamique possède des disques dynamiques. Cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente.

**Pour réénumérer et actualiser des objets de fournisseur de logiciels**

-   Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) , puis appelez la méthode [**IVdsService :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) . En plus de découvrir les disques récemment connectés et déconnectés et les lecteurs de CD-ROM, cette combinaison de méthodes met à jour toutes les informations sur les disques, les volumes et les plex dans le cache VDS pour les disques qui n’ont pas été récemment connectés ou déconnectés. Appelez **Refresh** seul pour actualiser les informations sur les propriétés des objets existants dans le cache. Cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente. Notez que VDS met à jour automatiquement le cache chaque fois qu’une modification se produit et déclenche une notification. En outre, l’appel de l' **actualisation** en réponse à une notification VDS peut entraîner l’envoi d’une boucle infinie de notifications. Pour ces raisons, l' **actualisation** doit être appelée uniquement lorsqu’il semble que le cache n’est pas mis à jour correctement.

**Pour réénumérer les sous-systèmes matériels**

-   Appelez la méthode [**IVdsHwProvider :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) . Selon le fournisseur, cette opération peut impliquer l’envoi de paquets réseau et l’attente de délais d’attente, la nouvelle analyse des bus SCSI et l’attente de délais d’attente, etc.

**Pour réénumérer les objets du sous-système matériel**

-   Appelez la méthode [**IVdsSubSystem :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) pour inventorier les objets (généralement des lecteurs) dans le sous-système. Selon le sous-système, cette opération peut impliquer l’analyse des bus du sous-système interne et l’attente des délais d’attente.

**Pour actualiser des sous-systèmes matériels et des objets de sous-système**

-   Appelez la méthode [**IVdsHwProvider :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) pour actualiser le cache VDS d’informations sur les sous-systèmes existants qui sont gérés par les fournisseurs de matériel VDS. Notez que VDS met à jour automatiquement le cache chaque fois qu’une modification se produit et déclenche une notification. En outre, l’appel de l' [**actualisation**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) en réponse à une notification VDS peut entraîner l’envoi d’une boucle infinie de notifications. Pour ces raisons, l' **actualisation** doit être appelée uniquement lorsqu’il semble que le cache n’est pas mis à jour correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de VDS](using-vds.md)
</dt> <dt>

[**IVdsService :: réénumération**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider :: réénumération**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem :: réénumération**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider :: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
