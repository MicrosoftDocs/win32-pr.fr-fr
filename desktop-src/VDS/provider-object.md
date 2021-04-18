---
description: L’objet fournisseur modélise le programme qui est responsable de la gestion du stockage.
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: Provider (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb36517f0091776b9429911212610134f31077a2
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104555845"
---
# <a name="provider-object"></a>Provider (objet)

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

L’objet fournisseur modélise le programme qui est responsable de la gestion du stockage. Cet objet permet d’accéder aux fonctionnalités du fournisseur de logiciels et du fournisseur de matériel. Les programmes de fournisseur exécutent des opérations sur des appareils logiciels (volumes et disques) et des périphériques matériels (sous-systèmes de stockage et groupes de lecteurs derrière les contrôleurs RAID).

VDS inscrit un objet fournisseur en tant qu’objet COM dans le Registre Windows et utilise des interfaces contenues (et non une agrégation) pour implémenter les objets restants, en encapsulant toutes les interfaces et méthodes et en ajoutant des fonctionnalités de manière conditionnelle. Les objets et les interfaces encapsulés par l’objet fournisseur varient en fonction du type de fournisseur.

Vous ne pouvez pas instancier un objet de fournisseur directement à partir de votre application. Au lieu de cela, vous devez démarrer VDS, obtenir un pointeur vers un objet de service et utiliser l’objet service pour interroger les fournisseurs connus de l’hôte. Pour obtenir des instructions sur le chargement de VDS, consultez [démarrage et objets de service](startup-and-service-objects.md).

Utilisez la méthode [**IVdsService :: QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) pour énumérer les programmes de fournisseur inscrits sur un ordinateur hôte. Le premier paramètre de la méthode vous permet de spécifier les fournisseurs de logiciels uniquement, les fournisseurs de matériel uniquement, ou les deux. Avec un objet fournisseur, vous pouvez effectuer des opérations sur les objets gérés par ce fournisseur. Comme le montre l’illustration suivante, vous pouvez utiliser les méthodes exposées par l’interface [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) pour créer et interroger des objets Pack associés aux fournisseurs de logiciels. De même, vous pouvez utiliser les méthodes sur l’interface [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) pour interagir avec les objets du sous-système associés aux fournisseurs de matériel.

![Diagramme montrant une branche « application » dans « Providers », « Pack » ou « Subsystem », puis « axes ».](images/vdsproviderobject.png)

Les propriétés d’objet incluent un identificateur d’objet GUID persistant qui représente un fournisseur spécifique et un deuxième GUID qui représente la version du fournisseur. Notez que les autres identificateurs d’objet dans le modèle objet VDS ne sont pas persistants. Les propriétés restantes de cet objet incluent le nom d’un fournisseur, des informations supplémentaires sur la version, le type de logiciel ou le matériel du fournisseur), les différents indicateurs et un paramètre de reconstruction-priorité qui s’applique uniquement aux fournisseurs de logiciels.

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                                                                         | Élément                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| Interfaces toujours exposées par les fournisseurs de logiciels uniquement                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| Interfaces toujours exposées par les fournisseurs de matériel uniquement                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| Interfaces qui peuvent être exposées par cet objet                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| Interfaces qui peuvent être exposées par des fournisseurs de matériel uniquement                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype), [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows Server 2008, windows Vista et Windows Server 2003 :** l’interface [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) n’est pas prise en charge.<br/> |
| Interfaces qui sont toujours implémentées mais ne sont pas exposées aux applications                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| Interfaces toujours implémentées par les fournisseurs de matériel mais non exposées aux applications | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| Interfaces pouvant être implémentées par les fournisseurs de matériel mais non exposées aux applications     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| Énumérations associées                                                                      | [**VDS \_ \_Indicateur de fournisseur**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag), [**\_ \_ \_ indicateur de fournisseur de requêtes VDS**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)et [**\_ \_ type de fournisseur VDS**](/windows/desktop/api/Vds/ne-vds-vds_provider_type).                                                                                                                         |
| Structures associées                                                                        | Aucun                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[Objets de démarrage et de service](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

