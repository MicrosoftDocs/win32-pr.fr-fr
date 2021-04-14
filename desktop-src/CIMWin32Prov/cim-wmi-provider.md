---
description: Ces classes WMI sont déclarées dans CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Fournisseur WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523108"
---
# <a name="cim-wmi-provider"></a>Fournisseur WMI CIM

Ces classes WMI sont déclarées dans CimWin32. mof.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**\_Action CIM**](cim-action.md)
</dt> <dd>

Une classe d' [**\_ action CIM**](cim-action.md) est une opération qui fait partie d’un processus de création d’un élément logiciel dans son état suivant ou d’élimination de l’élément logiciel dans l’état actuel.

</dd> <dt>

[**\_ACTIONSEQUENCE CIM**](cim-actionsequence.md)
</dt> <dd>

L’Association [**CIM \_ ActionSequence**](cim-actionsequence.md) définit une série d’opérations qui font passer l’élément logiciel (référencé par l’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) à son état suivant, ou supprime l’élément logiciel de son état actuel.

</dd> <dt>

[**\_ACTSASSPARE CIM**](cim-actsasspare.md)
</dt> <dd>

L’Association [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indique les éléments qui peuvent être des éléments de rechange ou remplacer d’autres éléments agrégés. Un Spare peut fonctionner en mode de « secours », comme spécifié élément par élément.

</dd> <dt>

[**\_ADJACENTSLOTS CIM**](cim-adjacentslots.md)
</dt> <dd>

L’Association [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur. Les informations, telles que la distance entre les emplacements et si elles sont « partagées » (si l’une d’elles est remplie, l’autre emplacement ne peut pas être utilisé), sont transmises en tant que propriétés d’association.

</dd> <dt>

[**\_AGGREGATEPEXTENT CIM**](cim-aggregatepextent.md)
</dt> <dd>

La classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fournit des informations récapitulatives sur les blocs logiques adressables, qui se trouvent dans le même groupe de redondance de stockage et qui se trouvent sur le même support physique.

</dd> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> <dd>

La classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) définit le nombre de blocs logiques adressables sur un dispositif de stockage unique, à l’exception des blocs logiques mappés en tant que données de vérification. Si des jeux de volumes sont définis, les blocs logiques sont contenus dans un seul ensemble de volumes. Il s’agit d’un autre regroupement pour les [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), lorsque seules les informations de résumé sont nécessaires ou lorsque la configuration automatique est utilisée.

</dd> <dt>

[**\_AGGREGATEREDUNDANCYCOMPONENT CIM**](cim-aggregateredundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) décrit l’étendue physique agrégée dans un groupe de redondance de stockage.

</dd> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> <dd>

La [**classe \_ AlarmDevice CIM**](cim-alarmdevice.md) est un appareil d’alarme qui émet des indications audibles ou visibles relatives à une situation problématique.

</dd> <dt>

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dd>

La classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) représente une association entre les unités logiques et les ressources système et indique que la ressource est affectée à l’appareil.

</dd> <dt>

[**\_APPLICATIONSYSTEM CIM**](cim-applicationsystem.md)
</dt> <dd>

La classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) représente une application ou un système logiciel qui prend en charge une fonction commerciale particulière qui peut être gérée comme une unité indépendante. Un tel système peut être décomposé en ses composants fonctionnels à l’aide de la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) . Les fonctionnalités logicielles d’une application ou d’un système logiciel particulier sont localisées à l’aide de l’Association [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .

</dd> <dt>

[**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

La classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) représente une association qui identifie les fonctionnalités logicielles qui composent un système d’applications particulier. Les fonctionnalités du logiciel peuvent être incluses dans différents produits.

</dd> <dt>

[**\_ASSOCIATEDALARM CIM**](cim-associatedalarm.md)
</dt> <dd>

La [**dépendance \_ AssociatedAlarm CIM**](cim-associatedalarm.md) associe une alarme à un appareil logique.

</dd> <dt>

[**\_ASSOCIATEDBATTERY CIM**](cim-associatedbattery.md)
</dt> <dd>

La [**dépendance \_ AssociatedBattery CIM**](cim-associatedbattery.md) associe une batterie à une unité logique. Utilisez cette association pour modéliser les batteries individuelles qui composent un onduleur.

</dd> <dt>

[**\_ASSOCIATEDCOOLING CIM**](cim-associatedcooling.md)
</dt> <dd>

L’Association [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indique quand des ventilateurs ou d’autres appareils de refroidissement sont spécifiques à un appareil (par rapport à la fourniture d’un boîtier ou d’un refroidissement d’armoire).

</dd> <dt>

[**\_ASSOCIATEDMEMORY CIM**](cim-associatedmemory.md)
</dt> <dd>

La [**classe \_ AssociateMemory CIM**](cim-associatedmemory.md) associe la mémoire installée ou associée, telle que la mémoire cache avec un périphérique logique.

</dd> <dt>

[**\_ASSOCIATEDPROCESSORMEMORY CIM**](cim-associatedprocessormemory.md)
</dt> <dd>

La classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associe le processeur et la mémoire système, ou le cache d’un processeur.

</dd> <dt>

[**\_ASSOCIATEDSENSOR CIM**](cim-associatedsensor.md)
</dt> <dd>

La classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associe un capteur installé à un périphérique logique. Le capteur mesure les propriétés d’entrée et de sortie critiques et peut être inclus avec l’appareil ou installé à proximité.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

La classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associe une alimentation à un capteur courant (intensité) qui surveille sa fréquence d’entrée.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Associe une alimentation à un capteur de tension qui surveille sa tension d’entrée.

</dd> <dt>

[**Basé sur CIM \_**](cim-basedon.md)
</dt> <dd>

La classe basée sur [**CIM \_**](cim-basedon.md) représente une association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur. Par exemple, les extensions physiques incluent des extensions d’espace protégé. Par conséquent, les jeux de volumes sont assemblés à partir d’une ou de plusieurs extensions d’espace physique ou protégé. La mémoire cache peut être définie indépendamment et réalisée dans un élément physique, ou elle peut être basée sur des extensions de stockage volatiles ou non volatiles.

</dd> <dt>

[**\_Batterie CIM**](cim-battery.md)
</dt> <dd>

La classe de [**\_ batterie CIM**](cim-battery.md) représente les fonctionnalités et la gestion de l’unité logique de batterie. Cette classe s’applique aux batteries dans les systèmes d’ordinateurs portables et autres batteries internes et externes.

</dd> <dt>

[**\_BINARYSENSOR CIM**](cim-binarysensor.md)
</dt> <dd>

La classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fournit une sortie booléenne. Les propriétés **CurrentState** et **PossibleStates** ont été ajoutées pour le capteur, rendant ainsi la sous-classe **CIM \_ BinarySensor** plus nécessaire, bien qu’elle soit conservée pour la compatibilité descendante. Un capteur binaire peut être créé en instanciant un capteur avec deux États possibles.

</dd> <dt>

[**\_BIOSELEMENT CIM**](cim-bioselement.md)
</dt> <dd>

La classe [**CIM \_ BIOSElement**](cim-bioselement.md) représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique.

</dd> <dt>

[**\_BIOSFEATURE CIM**](cim-biosfeature.md)
</dt> <dd>

représente les fonctionnalités du logiciel de bas niveau utilisé pour démarrer et configurer un système informatique.

</dd> <dt>

[**\_BIOSFEATUREBIOSELEMENTS CIM**](cim-biosfeaturebioselements.md)
</dt> <dd>

La classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associe une fonctionnalité BIOS et ses éléments BIOS agrégés.

</dd> <dt>

[**\_BIOSLOADEDINNV CIM**](cim-biosloadedinnv.md)
</dt> <dd>

La classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associe un élément BIOS et le stockage non volatile dans lequel elle est chargée.

</dd> <dt>

[**\_BOOTOSFROMFS CIM**](cim-bootosfromfs.md)
</dt> <dd>

La classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associe le système d’exploitation et les systèmes de fichiers à partir desquels le système d’exploitation est chargé. L’Association est de plusieurs-à-plusieurs ; un système d’exploitation distribué peut dépendre de plusieurs systèmes de fichiers pour se charger correctement et complètement.

</dd> <dt>

[**\_BOOTSAP CIM**](cim-bootsap.md)
</dt> <dd>

La classe [**CIM \_ BootSAP**](cim-bootsap.md) représente les points d’accès d’un service de démarrage.

</dd> <dt>

[**\_BOOTSERVICE CIM**](cim-bootservice.md)
</dt> <dd>

La classe [**CIM \_ BootService**](cim-bootservice.md) représente la fonctionnalité fournie par un périphérique ou un logiciel, ou par un réseau, pour charger un système d’exploitation sur un système informatique unitaire.

</dd> <dt>

[**\_BOOTSERVICEACCESSBYSAP CIM**](cim-bootserviceaccessbysap.md)
</dt> <dd>

La classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associe un service de démarrage et ses points d’accès.

</dd> <dt>

[**\_CACHEMEMORY CIM**](cim-cachememory.md)
</dt> <dd>

La classe [**CIM \_ CacheMemory**](cim-cachememory.md) définit les fonctionnalités et la gestion de la mémoire cache.

</dd> <dt>

[**\_Carte CIM**](cim-card.md)
</dt> <dd>

La classe de [**\_ carte CIM**](cim-card.md) représente un type de conteneur physique qui peut être branché dans une autre carte ou un autre tableau d’accueil, ou il s’agit d’une carte d’hébergement/carte mère dans un châssis. Cette classe comprend tout package capable de transporter des signaux et de fournir un point de montage pour les composants physiques, tels que les copeaux ou autres packages physiques, tels que les autres cartes.

</dd> <dt>

[**\_CARDINSLOT CIM**](cim-cardinslot.md)
</dt> <dd>

La classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associe une carte d’adaptateur au conteneur dans lequel elle est insérée.

</dd> <dt>

[**\_CARDONCARD CIM**](cim-cardoncard.md)
</dt> <dd>

L’Association [**CIM \_ CardOnCard**](cim-cardoncard.md) décrit des relations sur les cartes qui peuvent être connectées à des cartes mères/cartes de Baseboard, daughtercards d’un adaptateur ou des cartes qui prennent en charge des modules spéciaux de type carte.

</dd> <dt>

[**\_CDROMDRIVE CIM**](cim-cdromdrive.md)
</dt> <dd>

La classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) représente un lecteur de CD-ROM sur l’ordinateur.

</dd> <dt>

[**\_Châssis CIM**](cim-chassis.md)
</dt> <dd>

La classe de [**\_ châssis CIM**](cim-chassis.md) représente les éléments physiques qui englobent d’autres éléments et fournissent des fonctionnalités définissables, telles qu’un ordinateur de bureau, un nœud de traitement, des onduleurs, un stockage sur disque ou sur bande, ou une combinaison de ces éléments.

</dd> <dt>

[**\_CHASSISINRACK CIM**](cim-chassisinrack.md)
</dt> <dd>

L’Association [**CIM \_ ChassisInRack**](cim-chassisinrack.md) représente la relation « contenant » entre un rack et un châssis qu’il contient.

</dd> <dt>

[**\_Vérification CIM**](cim-check.md)
</dt> <dd>

La classe de [**\_ vérification CIM**](cim-check.md) représente une condition ou une caractéristique supposée être vraie dans un environnement défini ou étendu par une instance d’une classe [**\_ ComputerSystem CIM**](cim-computersystem.md) . Les contrôles associés à un élément logiciel particulier sont organisés en l’un des deux groupes à l’aide de la propriété **phase** de l’Association [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) .

</dd> <dt>

[**\_Puce CIM**](cim-chip.md)
</dt> <dd>

La classe de [**\_ puces CIM**](cim-chip.md) représente le type de matériel de circuit intégré, y compris les ASIC, les processeurs, les puces de mémoire, et ainsi de suite.

</dd> <dt>

[**\_CLUSTERINGSAP CIM**](cim-clusteringsap.md)
</dt> <dd>

La classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) représente les points d’accès d’un service de clustering.

</dd> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> <dd>

La classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) représente la fonctionnalité fournie par un cluster. Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.

</dd> <dt>

[**\_CLUSTERSERVICEACCESSBYSAP CIM**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

La classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) représente la relation entre un service de clustering et ses points d’accès.

</dd> <dt>

[**\_COLLECTEDCOLLECTIONS CIM**](cim-collectedcollections.md)
</dt> <dd>

La [**classe \_ CollectedCollections CIM**](cim-collectedcollections.md) est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.

</dd> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> <dd>

La classe d’association [**CIM \_ CollectedMSEs**](cim-collectedmses.md) représente les membres de l’objet de regroupement, une classe [**CollectionOfMSEs**](cim-collectionofmses.md) .

</dd> <dt>

[**\_COLLECTIONOFMSES CIM**](cim-collectionofmses.md)
</dt> <dd>

L’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) autorise le regroupement d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) afin d’associer les paramètres et les configurations. Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.

</dd> <dt>

[**\_COLLECTIONOFSENSORS CIM**](cim-collectionofsensors.md)
</dt> <dd>

L’Association [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) représente les capteurs binaires qui composent le capteur à États multistates.

</dd> <dt>

[**\_COLLECTIONSETTING CIM**](cim-collectionsetting.md)
</dt> <dd>

La classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) représente l’association entre un [**modèle CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) et la classe de paramètres définie pour eux.

</dd> <dt>

[**\_COMPATIBLEPRODUCT CIM**](cim-compatibleproduct.md)
</dt> <dd>

La [**classe \_ CompatibleProduct CIM**](cim-compatibleproduct.md) représente une association entre des produits qui indique si deux produits référencés sont interopérables, par exemple s’ils peuvent être installés ensemble ou si l’un peut être le conteneur physique de l’autre, et ainsi de suite.

</dd> <dt>

[**\_Composant CIM**](cim-component.md)
</dt> <dd>

L’Association de [**\_ composants CIM**](cim-component.md) représente les parties d’une relation entre les MSEs.

</dd> <dt>

[**\_ComputerSystem CIM**](cim-computersystem.md)
</dt> <dd>

Une [**classe \_ ComputerSystem CIM**](cim-computersystem.md) représente une collection spéciale d' [**instances \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) . Cette collection fournit des fonctionnalités d’ordinateur et sert de point d’agrégation pour associer un ou plusieurs des éléments suivants : système de fichiers, système d’exploitation, processeur et mémoire (stockage volatile et non volatile). Cette classe est dérivée [**du \_ système CIM**](cim-system.md).

</dd> <dt>

[**\_COMPUTERSYSTEMDMA CIM**](cim-computersystemdma.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) représente une association entre un système informatique et ses canaux DMA (Direct Memory Access) disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMIRQ CIM**](cim-computersystemirq.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) représente une association entre un système informatique et ses lignes de requête d’interruption (IRQ) disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMMAPPEDIO CIM**](cim-computersystemmappedio.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) représente une association entre un système informatique et les ports d’e/s mappés en mémoire disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMPACKAGE CIM**](cim-computersystempackage.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques. L’Association est semblable à la façon dont les unités logiques sont réalisées par les éléments physiques.

</dd> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> <dd>

La classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) représente une association entre un système informatique et les ressources système disponibles.

</dd> <dt>

[**\_Configuration CIM**](cim-configuration.md)
</dt> <dd>

L’objet de [**\_ configuration CIM**](cim-configuration.md) permet de regrouper des jeux de paramètres (définis dans les objets de [**\_ paramètre CIM**](cim-setting.md) ) et des dépendances pour un ou plusieurs éléments système gérés.

</dd> <dt>

[**\_CONNECTEDTO CIM**](cim-connectedto.md)
</dt> <dd>

La classe [**CIM \_ ConnectedTo**](cim-connectedto.md) représente une association qui indique que deux ou plusieurs connecteurs physiques sont connectés.

</dd> <dt>

[**\_CONNECTORONPACKAGE CIM**](cim-connectoronpackage.md)
</dt> <dd>

La classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) représente une association qui rend explicite la relation d’imbrication entre les connecteurs et les packages. Les packages physiques contiennent des connecteurs et d’autres éléments physiques.

</dd> <dt>

[**\_Conteneur CIM**](cim-container.md)
</dt> <dd>

La classe de [**\_ conteneur CIM**](cim-container.md) représente une association entre un élément physique contenu et un élément physique contenant. Un objet conteneur doit être un package physique.

</dd> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dd>

La [**relation \_ ControlledBy CIM**](cim-controlledby.md) indique quels appareils sont demandés par l’unité logique du contrôleur, ou accessibles via celui-ci.

</dd> <dt>

[**\_Contrôleur CIM**](cim-controller.md)
</dt> <dd>

La classe de [**\_ contrôleur CIM**](cim-controller.md) est une classe parente permettant de regrouper divers appareils liés au contrôle. Les contrôleurs SCSI, les contrôleurs USB et les contrôleurs série sont des exemples de contrôleurs.

</dd> <dt>

[**\_COOLINGDEVICE CIM**](cim-coolingdevice.md)
</dt> <dd>

La classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) représente les fonctionnalités et la gestion des appareils de refroidissement.

</dd> <dt>

[**\_COPYFILEACTION CIM**](cim-copyfileaction.md)
</dt> <dd>

La classe [**CIM \_ CopyFileAction**](cim-copyfileaction.md) représente le déplacement ou la copie de fichiers à partir d’un système informatique vers un nouvel emplacement.

</dd> <dt>

[**\_CREATEDIRECTORYACTION CIM**](cim-createdirectoryaction.md)
</dt> <dd>

La classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crée des répertoires vides pour les éléments logiciels à installer localement.

</dd> <dt>

[**\_CURRENTSENSOR CIM**](cim-currentsensor.md)
</dt> <dd>

La classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.

</dd> <dt>

[**\_Fichier de fichier CIM**](cim-datafile.md)
</dt> <dd>

La classe de [**\_ fichier**](cim-datafile.md) de données CIM représente une collection nommée de données ou du code exécutable. Seules les instances de fichiers sur des disques fixes locaux sont retournées

</dd> <dt>

[**\_Dépendance CIM**](cim-dependency.md)
</dt> <dd>

La classe de [**\_ dépendance CIM**](cim-dependency.md) représente une association qui établit des relations de dépendance entre des objets.

</dd> <dt>

[**\_DEPENDENCYCONTEXT CIM**](cim-dependencycontext.md)
</dt> <dd>

La [**relation \_ DependencyContext CIM**](cim-dependencycontext.md) associe une classe de [**\_ dépendance CIM**](cim-dependency.md) à un ou plusieurs objets de [**\_ configuration CIM**](cim-configuration.md) . Par exemple, les dépendances d’un système informatique peuvent changer en fonction du réseau auquel le système est attaché.

</dd> <dt>

[**\_DESKTOPMONITOR CIM**](cim-desktopmonitor.md)
</dt> <dd>

La classe [**CIM \_ desktopmonitor**](cim-desktopmonitor.md) représente les fonctionnalités et la gestion de l’unité logique du moniteur Desktop (CRT).

</dd> <dt>

[**\_DEVICEACCESSEDBYFILE CIM**](cim-deviceaccessedbyfile.md)
</dt> <dd>

La classe d’association [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) spécifie l’appareil logique accessible à l’aide de la classe [**CIM \_ DeviceFile**](cim-devicefile.md) référencée.

</dd> <dt>

[**\_DEVICECONNECTION CIM**](cim-deviceconnection.md)
</dt> <dd>

La classe d’association [**CIM \_ DeviceConnection**](cim-deviceconnection.md) représente au moins deux appareils connectés.

</dd> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> <dd>

La [**classe \_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) est une classe statistique qui contient des compteurs relatifs aux erreurs pour un périphérique logique. Les types d’erreurs sont définis par CCITT (Rec X. 733) et ISO (IEC 10164-4).

</dd> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> <dd>

La classe [**CIM \_ DeviceFile**](cim-devicefile.md) représente un type de fichier logique, qui représente un périphérique. Cette Convention est utile pour les systèmes d’exploitation qui gèrent des appareils à l’aide d’un modèle d’e/s de flux d’octets. L’appareil logique associé à ce fichier est spécifié à l’aide de la relation [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .

</dd> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dd>

La classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté. Lorsque de nombreux périphériques logiques sont associés à un SAP, les éléments fonctionnent conjointement pour fournir le point d’accès. Si différentes implémentations d’un SAP existent, chaque implémentation entraîne des instanciations individuelles de l’objet SAP.

</dd> <dt>

[**\_DEVICESERVICEIMPLEMENTATION CIM**](cim-deviceserviceimplementation.md)
</dt> <dd>

La classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) représente une association entre un service et la manière dont il est implémenté. Lorsque plusieurs appareils sont associés à un service, les éléments fonctionnent conjointement pour fournir le service. Si différentes implémentations d’un service existent, chaque implémentation produit des instanciations individuelles de l’objet de service.

</dd> <dt>

[**\_DEVICESOFTWARE CIM**](cim-devicesoftware.md)
</dt> <dd>

La [**relation \_ DeviceSoftware CIM**](cim-devicesoftware.md) identifie les logiciels associés à un appareil, tels que les pilotes, les logiciels de configuration ou d’application, ou le microprogramme.

</dd> <dt>

[**\_Répertoire CIM**](cim-directory.md)
</dt> <dd>

La classe de [**\_ répertoire CIM**](cim-directory.md) représente un type de fichier qui regroupe logiquement les fichiers de données qu’elle contient et fournit des informations de chemin d’accès pour les fichiers groupés.

</dd> <dt>

[**\_DIRECTORYACTION CIM**](cim-directoryaction.md)
</dt> <dd>

La classe abstraite [**CIM \_ DirectoryAction**](cim-directoryaction.md) gère les répertoires. La création de répertoires est gérée par la classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) et la suppression des répertoires est gérée par la classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .

</dd> <dt>

[**\_DIRECTORYCONTAINSFILE CIM**](cim-directorycontainsfile.md)
</dt> <dd>

La classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) représente une association entre un répertoire et des fichiers contenus dans ce répertoire.

</dd> <dt>

[**\_DIRECTORYSPECIFICATION CIM**](cim-directoryspecification.md)
</dt> <dd>

La classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) capture la principale structure de répertoires d’un élément logiciel. Cette classe est utilisée pour organiser les fichiers d’un élément logiciel en unités gérables qui peuvent être déplacées sur un système informatique.

</dd> <dt>

[**\_DIRECTORYSPECIFICATIONFILE CIM**](cim-directoryspecificationfile.md)
</dt> <dd>

L’Association [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) représente le répertoire qui contient le fichier spécifié en référençant la classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .

</dd> <dt>

[**\_DISCRETESENSOR CIM**](cim-discretesensor.md)
</dt> <dd>

La classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) possède un ensemble de valeurs de chaîne valides qu’elle peut signaler. Les valeurs sont énumérées dans la propriété **PossibleValues** du capteur. Un capteur discret a toujours une lecture actuelle qui correspond à l’une des valeurs énumérées.

</dd> <dt>

[**\_DISKDRIVE CIM**](cim-diskdrive.md)
</dt> <dd>

La classe [**CIM \_ DiskDrive**](cim-diskdrive.md) représente un lecteur de disque physique tel qu’il est vu par le système d’exploitation. Les fonctionnalités du lecteur de disque correspondent aux caractéristiques logiques et de gestion du lecteur, et dans certains cas, peuvent ne pas refléter les caractéristiques physiques de l’appareil. Une interface vers un lecteur physique est un membre de cette classe. Toutefois, un objet basé sur un autre périphérique logique n’est pas un membre de cette classe.

</dd> <dt>

[**\_DISKETTEDRIVE CIM**](cim-diskettedrive.md)
</dt> <dd>

La classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) représente les fonctionnalités et la gestion d’un lecteur de disquette.

</dd> <dt>

[**\_DISKPARTITION CIM**](cim-diskpartition.md)
</dt> <dd>

La classe [**CIM \_ DiskPartition**](cim-diskpartition.md) représente une plage contiguë de blocs logiques qui est identifiable par le système d’exploitation par le biais des champs type et sous-type de la partition. Les partitions de disque doivent être réalisées directement par le support physique (indiqué par l’Association [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) ) ou par les volumes de stockage.

</dd> <dt>

[**\_DISKSPACECHECK CIM**](cim-diskspacecheck.md)
</dt> <dd>

La classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) vérifie la quantité d’espace disque disponible du système et la spécifie dans la propriété **AvailableDiskSpace** . Les détails sont comparés à la valeur de la propriété **AvailableSpace** de l’objet [**CIM \_ FileSystem**](cim-filesystem.md) associé à l' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) , qui décrit l’environnement système. Lorsque la valeur de la propriété **AvailableSpace** est supérieure ou égale à la valeur spécifiée dans la propriété **AvailableDiskSpace** , la condition est satisfaite.

</dd> <dt>

[**\_Affichage CIM**](cim-display.md)
</dt> <dd>

La classe d' [**\_ affichage CIM**](cim-display.md) est une classe parente permettant de regrouper divers périphériques d’affichage.

</dd> <dt>

[**\_DMA CIM**](cim-dma.md)
</dt> <dd>

La [**classe \_ DMA CIM**](cim-dma.md) représente l’accès direct à la mémoire (DMA) de l’architecture d’ordinateur.

</dd> <dt>

[**\_Connexion CIM**](cim-docked.md)
</dt> <dd>

L’Association de la [**\_ station d’accueil CIM**](cim-docked.md) représente la relation entre deux châssis. Par exemple, un ordinateur portable (un type de châssis) peut être ancré dans une station d’accueil (un autre type de châssis). Cette relation classique est décrite de manière explicite.

</dd> <dt>

[**\_ELEMENTCAPACITY CIM**](cim-elementcapacity.md)
</dt> <dd>

La classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associe un objet [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md) à un ou plusieurs éléments physiques. Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.

</dd> <dt>

[**\_ELEMENTCONFIGURATION CIM**](cim-elementconfiguration.md)
</dt> <dd>

L’Association [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) associe un objet de [**\_ configuration CIM**](cim-configuration.md) à un ou plusieurs éléments système gérés. L’objet de **\_ configuration CIM** représente un comportement spécifique ou un état fonctionnel souhaité pour le [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associé.

</dd> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

La classe [**CIM \_ ElementSetting**](cim-elementsetting.md) représente l’association entre les éléments système gérés et la classe de paramètres définie pour eux.

</dd> <dt>

[**\_ELEMENTSLINKED CIM**](cim-elementslinked.md)
</dt> <dd>

L’Association [**CIM \_ ElementsLinked**](cim-elementslinked.md) représente des éléments physiques reliés par un lien physique.

</dd> <dt>

[**\_ERRORCOUNTERSFORDEVICE CIM**](cim-errorcountersfordevice.md)
</dt> <dd>

La classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associe la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) à l’unité logique à laquelle elle s’applique.

</dd> <dt>

[**\_EXECUTEPROGRAM CIM**](cim-executeprogram.md)
</dt> <dd>

La classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) représente des fichiers qui peuvent être exécutés sur le système sur lequel l’élément logiciel est installé.

</dd> <dt>

[**\_Exportation CIM**](cim-export.md)
</dt> <dd>

La classe d' [**\_ exportation CIM**](cim-export.md) représente une association entre un système de fichiers local et ses répertoires, ce qui indique que les répertoires spécifiés sont disponibles pour le montage. Lorsque vous exportez un système de fichiers entier, le répertoire doit référencer le répertoire le plus haut du système de fichiers.

</dd> <dt>

[**\_EXTRACAPACITYGROUP CIM**](cim-extracapacitygroup.md)
</dt> <dd>

La classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) est dérivée d’un groupe de redondance qui indique que les éléments agrégés ont plus de capacité ou de capacité que nécessaire. Voici un exemple de ce type de redondance : l’installation de N + 1 alimentations ou de ventilateurs dans un système.

</dd> <dt>

[**\_Ventilateur CIM**](cim-fan.md)
</dt> <dd>

La classe de [**\_ ventilateur CIM**](cim-fan.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement de ventilateur.

</dd> <dt>

[**\_FILEACTION CIM**](cim-fileaction.md)
</dt> <dd>

La classe [**CIM \_ FileAction**](cim-fileaction.md) permet à l’auteur de localiser des fichiers qui existent déjà sur l’ordinateur d’un utilisateur, puis de déplacer ou de copier ces fichiers vers un nouvel emplacement.

</dd> <dt>

[**\_FILESPECIFICATION CIM**](cim-filespecification.md)
</dt> <dd>

La classe [**CIM \_ FileSpecification**](cim-filespecification.md) représente un fichier qui se trouve sur le système ou en est déconnectée. Le fichier se trouve dans le répertoire identifié par l’Association [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) . La méthode [**Invoke**](invoke-method-in-class-cim-filespecification.md) utilise les informations pour vérifier l’existence du fichier. Notez que les propriétés avec une valeur **null** ne sont pas vérifiées.

</dd> <dt>

[**\_FILESTORAGE CIM**](cim-filestorage.md)
</dt> <dd>

L’Association [**CIM \_ FileStorage**](cim-filestorage.md) lie le système de fichiers et les fichiers logiques adressés via le système de fichiers.

</dd> <dt>

[**\_Système de fichiers CIM**](cim-filesystem.md)
</dt> <dd>

La classe de système de [**\_ fichiers CIM**](cim-filesystem.md) représente un fichier ou un jeu de données local sur un système informatique ou monté à distance à partir d’un serveur de fichiers.

</dd> <dt>

[**\_Plataux CIM**](cim-flatpanel.md)
</dt> <dd>

La classe d’écran plat [**CIM \_**](cim-flatpanel.md) représente les fonctionnalités et la gestion de l’appareil logique à écran plat.

</dd> <dt>

[**\_FROMDIRECTORYACTION CIM**](cim-fromdirectoryaction.md)
</dt> <dd>

L’Association [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifie le répertoire source de l’action de fichier. Lorsque cette association est utilisée, l’hypothèse est que le répertoire source a été créé par une action précédente. Cette association ne peut pas exister avec une association [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) ; une action de fichier ne peut impliquer qu’un seul répertoire source.

</dd> <dt>

[**\_FROMDIRECTORYSPECIFICATION CIM**](cim-fromdirectoryspecification.md)
</dt> <dd>

L’Association [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifie le répertoire source de l’action de fichier. Lorsque cette association est utilisée, l’hypothèse est que le répertoire source existe déjà. Cette association ne peut pas exister avec une association [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) ; une action de fichier ne peut impliquer qu’un seul répertoire source.

</dd> <dt>

[**\_FRU CIM**](cim-fru.md)
</dt> <dd>

La [**classe \_ FRU CIM**](cim-fru.md) représente une collection définie par le fournisseur de produits et d’éléments physiques associés à une unité remplaçable sur site (FRU) pour la prise en charge, la maintenance ou la mise à niveau d’un produit à l’emplacement du client.

</dd> <dt>

[**\_FRUINCLUDESPRODUCT CIM**](cim-fruincludesproduct.md)
</dt> <dd>

La classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indique qu’une unité remplaçable sur site (FRU) peut être composée d’autres produits.

</dd> <dt>

[**\_FRUPHYSICALELEMENTS CIM**](cim-fruphysicalelements.md)
</dt> <dd>

La classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) représente les éléments physiques qui composent une unité remplaçable sur site (FRU).

</dd> <dt>

[**\_Heatpipe CIM**](cim-heatpipe.md)
</dt> <dd>

La classe [**CIM \_ Heatpipe**](cim-heatpipe.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement de tuyauterie thermique.

</dd> <dt>

[**\_HOSTEDACCESSPOINT CIM**](cim-hostedaccesspoint.md)
</dt> <dd>

La classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) représente une association entre un point d’accès de service (SAP) et le système sur lequel il est fourni. Chaque système peut héberger de nombreuses SAP.

</dd> <dt>

[**\_HOSTEDBOOTSAP CIM**](cim-hostedbootsap.md)
</dt> <dd>

La classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) définit le système informatique unitaire d’hébergement pour une classe [**CIM \_ BootSAP**](cim-bootsap.md) . Étant donné que cette relation est sous-classée à partir de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md), où un point d’accès défère au système d’hébergement. Dans ce cas, **le \_ BootSAP CIM** doit être différé à sa classe [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) d’hébergement.

</dd> <dt>

[**\_HOSTEDBOOTSERVICE CIM**](cim-hostedbootservice.md)
</dt> <dd>

La classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associe un système d’hébergement et un service de démarrage. Étant donné que cette relation est sous-classée à partir de [**CIM \_ service hébergé**](cim-hostedservice.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le service, où un service s’en remet au système d’hébergement.

</dd> <dt>

[**\_HOSTEDFILESYSTEM CIM**](cim-hostedfilesystem.md)
</dt> <dd>

L’Association [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) représente un lien entre le système informatique et le système de fichiers hébergé sur le système informatique.

</dd> <dt>

[**\_HOSTEDJOBDESTINATION CIM**](cim-hostedjobdestination.md)
</dt> <dd>

La classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) représente une association entre une destination de travail et le système sur lequel elle réside. Un système peut héberger de nombreuses files d’attente de travaux. Les destinations du travail diffèrent au système d’hébergement.

</dd> <dt>

[**\_Service hébergé CIM**](cim-hostedservice.md)
</dt> <dd>

La classe [**CIM \_ service hébergé**](cim-hostedservice.md) représente une association entre un service et le système sur lequel la fonctionnalité réside. Un système peut héberger de nombreux services, qui retardent le système d’hébergement. Le modèle ne représente pas les services hébergés sur plusieurs systèmes.

</dd> <dt>

[**\_INFRAREDCONTROLLER CIM**](cim-infraredcontroller.md)
</dt> <dd>

La classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) représente les fonctionnalités et la gestion d’un contrôleur infrarouge.

</dd> <dt>

[**CIM \_ installé**](cim-installedos.md)
</dt> <dd>

La classe d’association [**CIM \_ installos**](cim-installedos.md) représente un lien entre le système de l’ordinateur et le système d’exploitation installé. Un système d’exploitation est installé lorsqu’il se trouve dans l’extension de stockage d’un système d’ordinateur (par exemple, copié sur un lecteur de disque ou téléchargé en mémoire).

</dd> <dt>

[**\_INSTALLEDSOFTWAREELEMENT CIM**](cim-installedsoftwareelement.md)
</dt> <dd>

La classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associe un système informatique à un élément logiciel installé.

</dd> <dt>

[**\_IRQ CIM**](cim-irq.md)
</dt> <dd>

La classe d' [**\_ IRQ CIM**](cim-irq.md) représente une ligne de demande d’interruption (IRQ) d’architecture Intel.

</dd> <dt>

[**\_Travail CIM**](cim-job.md)
</dt> <dd>

La classe de [**\_ tâche CIM**](cim-job.md) représente une unité de travail pour un système, par exemple un travail d’impression. Un travail est différent d’un processus, car un travail peut être planifié.

</dd> <dt>

[**\_JOBDESTINATION CIM**](cim-jobdestination.md)
</dt> <dd>

La classe [**CIM \_ JobDestination**](cim-jobdestination.md) représente l’emplacement où un travail est soumis pour traitement. Il peut faire référence à une file d’attente qui contient zéro travail ou plus, tel qu’une file d’attente à l’impression contenant des travaux d’impression. Les destinations des travaux sont hébergées sur des systèmes, de la même façon que les services sont hébergés sur les systèmes.

</dd> <dt>

[**\_JOBDESTINATIONJOBS CIM**](cim-jobdestinationjobs.md)
</dt> <dd>

L’Association [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) décrit l’endroit où un travail est soumis pour traitement (c’est-à-dire la destination du travail).

</dd> <dt>

[**\_Clavier CIM**](cim-keyboard.md)
</dt> <dd>

La classe de [**\_ clavier CIM**](cim-keyboard.md) représente les fonctionnalités et la gestion du périphérique logique du clavier.

</dd> <dt>

[**\_LINKHASCONNECTOR CIM**](cim-linkhasconnector.md)
</dt> <dd>

La classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associe les câbles et les liens utilisés comme connecteurs physiques, qui connectent les éléments physiques. Cette association définit explicitement la relation des connecteurs pour [**les \_ PhysicalLink CIM**](cim-physicallink.md).

</dd> <dt>

[**\_LOCALFILESYSTEM CIM**](cim-localfilesystem.md)
</dt> <dd>

La classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) représente le magasin de fichiers contrôlé par un système informatique par le biais de moyens locaux (par exemple, accès direct au pilote de l’appareil). Le magasin de fichiers peut être géré directement par le système informatique, sans qu’un autre ordinateur n’ait besoin d’agir en tant que serveur de fichiers. Dans le cas d’un système de fichiers en cluster, toutefois, le système de fichiers est local et, par conséquent, diffère du cluster.

</dd> <dt>

[**\_Emplacement CIM**](cim-location.md)
</dt> <dd>

La classe d' [**\_ emplacement CIM**](cim-location.md) représente la position et l’adresse d’un élément physique.

</dd> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dd>

La classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) représente une entité matérielle qui peut ou ne peut pas être réalisée sur du matériel physique.

</dd> <dt>

[**\_Disque logique CIM**](cim-logicaldisk.md)
</dt> <dd>

La [**classe \_ LogicalDisk CIM**](cim-logicaldisk.md) représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ **DeviceID** (Key) du disque. Par exemple, dans un environnement Windows, le champ **DeviceID** contient une lettre de lecteur. dans un environnement UNIX, elle contient le chemin d’accès ; dans un environnement NetWare, il contient le nom du volume.

</dd> <dt>

[**\_LOGICALDISKBASEDONPARTITION CIM**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

La classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associe un disque logique à la partition de disque sur laquelle il réside.

</dd> <dt>

[**\_LOGICALDISKBASEDONVOLUMESET CIM**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

L’Association [**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) associe les disques logiques au volume sur lequel ils sont trouvés. Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.

</dd> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dd>

La classe [**CIM \_ LogicalElement**](cim-logicalelement.md) est la classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.

</dd> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> <dd>

La classe [**CIM \_ LogicalFile**](cim-logicalfile.md) représente une collection nommée de données, qui peut être du code exécutable, qui se trouve dans un système de fichiers sur une extension de stockage.

</dd> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dd>

La [**classe \_ LogicalIdentity CIM**](cim-logicalidentity.md) est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente.

</dd> <dt>

[**\_MAGNETOOPTICALDRIVE CIM**](cim-magnetoopticaldrive.md)
</dt> <dd>

La classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) représente les fonctionnalités et la gestion d’un lecteur magnéto-optique, un sous-type de l’appareil d’accès aux médias.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

La [**classe \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) est la classe de base pour la hiérarchie des éléments système. Tout composant système distinctif est un candidat pour l’inclusion dans cette classe.

</dd> <dt>

[**\_MANAGEMENTCONTROLLER CIM**](cim-managementcontroller.md)
</dt> <dd>

La classe [**CIM \_ ManagementController**](cim-managementcontroller.md) est associée aux fonctionnalités et à la gestion d’un contrôleur de gestion.

</dd> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> <dd>

La classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) représente la possibilité d’accéder à un ou plusieurs médias, puis d’utiliser le média pour stocker et récupérer des données.

</dd> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dd>

L’Association [**CIM \_ MediaPresent**](cim-mediapresent.md) décrit une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès aux médias.

</dd> <dt>

[**\_Mémoire CIM**](cim-memory.md)
</dt> <dd>

La classe de [**\_ mémoire CIM**](cim-memory.md) représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.

</dd> <dt>

[**\_MEMORYCAPACITY CIM**](cim-memorycapacity.md)
</dt> <dd>

La classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) représente la mémoire qui peut être installée sur un élément physique et ses configurations minimale et maximale. Les informations sur la mémoire qui est actuellement installée et les exigences minimales et maximales d’un élément se trouvent dans les instances de la classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .

</dd> <dt>

[**\_MEMORYCHECK CIM**](cim-memorycheck.md)
</dt> <dd>

La classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) spécifie une condition pour la quantité minimale de mémoire qui doit être disponible sur un système.

</dd> <dt>

[**\_MEMORYMAPPEDIO CIM**](cim-memorymappedio.md)
</dt> <dd>

La classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) représente l’architecture d’ordinateur des e/s mappées en mémoire. Cette classe résout les ressources de mémoire et d’e/s de port.

</dd> <dt>

[**\_MEMORYONCARD CIM**](cim-memoryoncard.md)
</dt> <dd>

La classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associe la mémoire physique située sur les cartes d’hébergement, les cartes d’adaptateur, etc. Cette association définit explicitement la relation entre la mémoire et les cartes.

</dd> <dt>

[**\_MEMORYWITHMEDIA CIM**](cim-memorywithmedia.md)
</dt> <dd>

La classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associe la mémoire physique à un support physique et à sa cartouche. La mémoire fournit l’identification du média et stocke les données spécifiques à l’utilisateur.

</dd> <dt>

[**\_MODIFYSETTINGACTION CIM**](cim-modifysettingaction.md)
</dt> <dd>

La classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) représente les informations pour la modification d’un fichier de paramètre spécifique, pour une entrée spécifique, avec une valeur spécifique.

</dd> <dt>

[**\_MONITORRESOLUTION CIM**](cim-monitorresolution.md)
</dt> <dd>

La classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) représente la relation entre les résolutions horizontales et verticales, ainsi que la fréquence d’actualisation et le mode d’analyse d’un moniteur d’ordinateur de bureau. Les valeurs sont spécifiées dans l’objet de contrôleur vidéo.

</dd> <dt>

[**\_MONITORSETTING CIM**](cim-monitorsetting.md)
</dt> <dd>

La classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.

</dd> <dt>

[**\_Montage CIM**](cim-mount.md)
</dt> <dd>

La [**classe \_ Mount CIM**](cim-mount.md) représente une association entre un système de fichiers et un répertoire auquel elle est attachée.

</dd> <dt>

[**\_MULTISTATESENSOR CIM**](cim-multistatesensor.md)
</dt> <dd>

La classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) représente un jeu de capteurs binaires à plusieurs membres où chaque capteur binaire signale un résultat booléen.

</dd> <dt>

[**\_NETWORKADAPTER CIM**](cim-networkadapter.md)
</dt> <dd>

La classe de la carte CIM est une classe abstraite qui définit les concepts généraux de matériel de mise en réseau (par exemple, une adresse permanente ou une vitesse de fonctionnement). [**\_**](cim-networkadapter.md) Les informations sont transmises à l’aide de l’Association [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .

</dd> <dt>

[**\_NFS CIM**](cim-nfs.md)
</dt> <dd>

La [**classe \_ NFS CIM**](cim-nfs.md) représente un système de fichiers distant monté, à l’aide du protocole NFS (Network File System), à partir d’un système informatique.

</dd> <dt>

[**\_NONVOLATILESTORAGE CIM**](cim-nonvolatilestorage.md)
</dt> <dd>

La classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) représente les fonctionnalités et la gestion du stockage non volatile. La mémoire non volatile comprend en mode natif le stockage flash et ROM.

</dd> <dt>

[**\_NUMERICSENSOR CIM**](cim-numericsensor.md)
</dt> <dd>

La classe [**CIM \_ NumericSensor**](cim-numericsensor.md) représente un capteur numérique qui retourne des lectures numériques et éventuellement prend en charge les paramètres de seuils.

</dd> <dt>

[**\_OPERATINGSYSTEM CIM**](cim-operatingsystem.md)
</dt> <dd>

La classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) représente un système d’exploitation d’ordinateur, qui est constitué de logiciels et de microprogrammes permettant de rendre le matériel d’un système d’ordinateur utilisable.

</dd> <dt>

[**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

La classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) représente les fonctionnalités logicielles qui composent le système d’exploitation.

</dd> <dt>

[**\_OSPROCESS CIM**](cim-osprocess.md)
</dt> <dd>

La classe [**CIM \_ OSProcess**](cim-osprocess.md) associe le système d’exploitation et un ou plusieurs processus en cours d’exécution dans le contexte du système d’exploitation.

</dd> <dt>

[**\_OSVERSIONCHECK CIM**](cim-osversioncheck.md)
</dt> <dd>

La classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) spécifie les versions du système d’exploitation qui peuvent prendre en charge un élément logiciel.

</dd> <dt>

[**\_PACKAGEALARM CIM**](cim-packagealarm.md)
</dt> <dd>

L’Association [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package. L’installation indique des problèmes avec l’environnement du package : son état de sécurité ou son intégrité globale.

</dd> <dt>

[**\_PACKAGECOOLING CIM**](cim-packagecooling.md)
</dt> <dd>

L’Association [**CIM \_ PackageCooling**](cim-packagecooling.md) représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.

</dd> <dt>

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> <dd>

L’Association [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) représente une relation explicite dans laquelle un composant est généralement contenu dans un package physique, tel qu’un châssis ou une carte.

</dd> <dt>

[**\_PACKAGEINCHASSIS CIM**](cim-packageinchassis.md)
</dt> <dd>

L’Association [**CIM \_ PackageInChassis**](cim-packageinchassis.md) représente la relation dans laquelle un châssis peut contenir d’autres packages, tels que d’autres châssis et cartes.

</dd> <dt>

[**\_PACKAGEINSLOT CIM**](cim-packageinslot.md)
</dt> <dd>

L’Association [**CIM \_ PackageInSlot**](cim-packageinslot.md) représente la relation entre les cartes d’appareil et le châssis dans lequel elles sont montées.

</dd> <dt>

[**\_PACKAGETEMPSENSOR CIM**](cim-packagetempsensor.md)
</dt> <dd>

L’Association [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) représente la relation dans laquelle un capteur de température est souvent installé dans un package, tel qu’un châssis ou un rack, pour surveiller l’environnement du package.

</dd> <dt>

[**\_PARALLELCONTROLLER CIM**](cim-parallelcontroller.md)
</dt> <dd>

L’Association [**CIM \_ ParallelController**](cim-parallelcontroller.md) se réfère aux fonctionnalités et à la gestion de l’unité logique de port parallèle.

</dd> <dt>

[**\_PARTICIPATESINSET CIM**](cim-participatesinset.md)
</dt> <dd>

La classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifie les éléments physiques qui doivent être remplacés ensemble.

</dd> <dt>

[**\_PCICONTROLLER CIM**](cim-pcicontroller.md)
</dt> <dd>

La classe [**CIM \_ PCIController**](cim-pcicontroller.md) représente les propriétés et la gestion d’un contrôleur PCI. Les propriétés de cette classe et de ses sous-classes sont définies dans les différentes spécifications PCI publiées par le SIG PCI.

</dd> <dt>

[**\_PCMCIACONTROLLER CIM**](cim-pcmciacontroller.md)
</dt> <dd>

La classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) représente les fonctionnalités et la gestion d’un contrôleur PCMCIA (Personal Computer Memory Card International Association).

</dd> <dt>

[**\_PCVIDEOCONTROLLER CIM**](cim-pcvideocontroller.md)
</dt> <dd>

Le [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) représente les fonctionnalités et la gestion d’un contrôleur vidéo d’ordinateur personnel, un sous-type d’un contrôleur vidéo.

</dd> <dt>

[**\_PEXTENTREDUNDANCYCOMPONENT CIM**](cim-pextentredundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) représente les extensions physiques qui participent à un groupe de redondance de stockage.

</dd> <dt>

[**\_PHYSICALCAPACITY CIM**](cim-physicalcapacity.md)
</dt> <dd>

La [**classe \_ PhysicalCapacity CIM**](cim-physicalcapacity.md) est une classe abstraite qui représente les exigences minimales et maximales d’un élément physique, ainsi que sa capacité à prendre en charge différents types de matériel. Par exemple, les exigences minimales et maximales en mémoire peuvent être modélisées en tant que sous-classe de **\_ PhysicalCapacity CIM**.

</dd> <dt>

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> <dd>

La classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) représente un composant de base ou de bas niveau au sein d’un package. Un élément physique qui n’est pas un lien, un connecteur ou un package est un descendant (ou membre) de cette classe.

</dd> <dt>

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> <dd>

La classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) représente tout élément physique utilisé pour se connecter à d’autres éléments. Tout objet qui peut se connecter et transmettre des signaux ou de la puissance entre deux ou plusieurs éléments physiques est un descendant (ou membre) de cette classe.

</dd> <dt>

[**\_PHYSICALELEMENT CIM**](cim-physicalelement.md)
</dt> <dd>

Les sous-classes [**\_ PhysicalElement CIM**](cim-physicalelement.md) définissent tout composant d’un système qui a une identité physique distincte. Les instances de cette classe peuvent être définies en termes d’étiquettes qui peuvent être physiquement attachées à l’objet.

</dd> <dt>

[**\_PHYSICALELEMENTLOCATION CIM**](cim-physicalelementlocation.md)
</dt> <dd>

La classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associe un élément physique à un objet d' [**\_ emplacement CIM**](cim-location.md) à des fins d’inventaire ou de remplacement.

</dd> <dt>

[**\_PHYSICALEXTENT CIM**](cim-physicalextent.md)
</dt> <dd>

La classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) représente une implémentation RAID SCC. Il définit les adresses de bloc adressables consécutives sur un dispositif de stockage unique qui sont traitées comme une extension de stockage unique dans la même classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) . Une alternative, lorsque la configuration automatique est utilisée, consiste à instancier ou étendre la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .

</dd> <dt>

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> <dd>

La [**classe \_ PhysicalFrame CIM**](cim-physicalframe.md) est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension. Les propriétés telles que **VisibleAlarm** et **AudibleAlarm**, ainsi que les données relatives aux violations de sécurité, sont incluses dans cette classe parente.

</dd> <dt>

[**\_PHYSICALLINK CIM**](cim-physicallink.md)
</dt> <dd>

La classe [**CIM \_ PhysicalLink**](cim-physicallink.md) représente le câblage des éléments physiques.

</dd> <dt>

[**\_PHYSICALMEDIA CIM**](cim-physicalmedia.md)
</dt> <dd>

La classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) représente les types de documentation et les supports de stockage, tels que les bandes, les CD-ROM, etc.

</dd> <dt>

[**\_PHYSICALMEMORY CIM**](cim-physicalmemory.md)
</dt> <dd>

La classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) représente des périphériques mémoire de bas niveau, tels que les SIMM, les DIMMs, les puces mémoire brutes, etc.

</dd> <dt>

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> <dd>

La classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) représente des éléments physiques qui contiennent ou hébergent d’autres composants. Il s’agit par exemple d’un boîtier en rack ou d’une carte adaptateur.

</dd> <dt>

[**\_POINTINGDEVICE CIM**](cim-pointingdevice.md)
</dt> <dd>

La classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) représente un appareil qui pointe vers des régions sur l’écran. Tout appareil qui manipule un pointeur ou qui pointe vers des régions sur un affichage visuel, est un membre de cette classe. Par exemple, une souris, un stylet, un pavé tactile ou une tablette.

</dd> <dt>

[**\_POTSMODEM CIM**](cim-potsmodem.md)
</dt> <dd>

La classe [**CIM \_ POTSModem**](cim-potsmodem.md) représente un appareil qui convertit les données binaires en modulations d’onde pour une transmission basée sur le son en se connectant au réseau pots (Plain Old Telephone System).

</dd> <dt>

[**\_Alimentation CIM**](cim-powersupply.md)
</dt> <dd>

La [**classe \_ d’alimentation CIM**](cim-powersupply.md) représente les fonctionnalités et la gestion de l’unité logique d’alimentation.

</dd> <dt>

[**\_Imprimante CIM**](cim-printer.md)
</dt> <dd>

La classe d' [**\_ imprimantes CIM**](cim-printer.md) représente les fonctionnalités et la gestion de l’unité logique d’imprimante.

</dd> <dt>

[**\_Processus CIM**](cim-process.md)
</dt> <dd>

La classe de [**\_ processus CIM**](cim-process.md) représente une instance unique d’un programme en cours d’exécution. Un utilisateur voit généralement un processus sous la forme d’une application ou d’une tâche.

</dd> <dt>

[**\_PROCESSEXECUTABLE CIM**](cim-processexecutable.md)
</dt> <dd>

La classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.

</dd> <dt>

[**\_Processeur CIM**](cim-processor.md)
</dt> <dd>

La classe du [**\_ processeur CIM**](cim-processor.md) représente les fonctionnalités et la gestion du périphérique logique du processeur.

</dd> <dt>

[**\_PROCESSTHREAD CIM**](cim-processthread.md)
</dt> <dd>

La classe [**CIM \_ ProcessThread**](cim-processthread.md) représente un lien entre un processus et les threads qui s’exécutent dans le contexte du processus.

</dd> <dt>

[**\_Produit CIM**](cim-product.md)
</dt> <dd>

La classe de [**\_ produit CIM**](cim-product.md) est une classe concrète qui représente une collection d’éléments physiques, de fonctionnalités logicielles et d’autres produits acquis en tant qu’unité. L’acquisition implique un accord entre le fournisseur et le consommateur, qui peut avoir des implications sur la licence, le support et la garantie du produit.

</dd> <dt>

[**\_PRODUCTFRU CIM**](cim-productfru.md)
</dt> <dd>

La classe [**CIM \_ ProductFRU**](cim-productfru.md) représente une association entre le produit et une unité remplaçable sur site (FRU), qui fournit des informations sur les composants du produit qui ont été ou sont remplacés.

</dd> <dt>

[**\_PRODUCTPARENTCHILD CIM**](cim-productparentchild.md)
</dt> <dd>

L’Association [**CIM \_ ProductParentChild**](cim-productparentchild.md) définit une hiérarchie parent-enfant parmi les produits. Par exemple, un produit peut être fourni avec d’autres produits.

</dd> <dt>

[**\_PRODUCTPHYSICALELEMENTS CIM**](cim-productphysicalelements.md)
</dt> <dd>

La classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) représente les éléments physiques qui composent un produit.

</dd> <dt>

[**\_PRODUCTPRODUCTDEPENDENCY CIM**](cim-productproductdependency.md)
</dt> <dd>

La [**classe \_ ProductProductDependency CIM**](cim-productproductdependency.md) représente une association entre deux produits, ce qui indique qu’un doit être installé ou absent pour que l’autre fonctionne. Il s’agit d’un concept équivalent à l’Association [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .

</dd> <dt>

[**\_PRODUCTSOFTWAREFEATURES CIM**](cim-productsoftwarefeatures.md)
</dt> <dd>

L’Association [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifie les fonctionnalités logicielles pour un produit particulier.

</dd> <dt>

[**\_PRODUCTSUPPORT CIM**](cim-productsupport.md)
</dt> <dd>

La classe [**CIM \_ ProductSupport**](cim-productsupport.md) représente une association entre le produit et l’accès au support qui indique comment le support est obtenu pour le produit. Différents types de support sont disponibles pour un produit. le même objet de support peut fournir une assistance pour plusieurs produits.

</dd> <dt>

[**\_PROTECTEDSPACEEXTENT CIM**](cim-protectedspaceextent.md)
</dt> <dd>

La classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) représente des adresses de blocs logiques adressables, qui sont traitées comme une extension de stockage unique, mais qui se trouvent sur une seule extension physique.

</dd> <dt>

[**\_PSEXTENTBASEDONPEXTENT CIM**](cim-psextentbasedonpextent.md)
</dt> <dd>

La [**classe \_ PSExtentBasedOnPExtent CIM**](cim-psextentbasedonpextent.md) associe des extensions d’espace protégé basées sur une extension physique.

</dd> <dt>

[**\_Rack CIM**](cim-rack.md)
</dt> <dd>

La classe de [**\_ rack CIM**](cim-rack.md) représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés. En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.

</dd> <dt>

[**CIM \_**](cim-realizes.md)
</dt> <dd>

La classe [**CIM \_ réalise**](cim-realizes.md) la représentation de l’Association qui définit le mappage entre un périphérique logique et le composant physique qui implémente l’appareil.

</dd> <dt>

[**\_REALIZESAGGREGATEPEXTENT CIM**](cim-realizesaggregatepextent.md)
</dt> <dd>

L’Association [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) représente la relation dans laquelle la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) est réalisée sur un support physique.

</dd> <dt>

[**\_REALIZESDISKPARTITION CIM**](cim-realizesdiskpartition.md)
</dt> <dd>

La classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) représente une partition de disque sur un support physique qui modélise la création de partitions sur un disque SCSI ou IDE brut.

</dd> <dt>

[**\_REALIZESPEXTENT CIM**](cim-realizespextent.md)
</dt> <dd>

L’Association [**CIM \_ RealizesPExtent**](cim-realizespextent.md) représente la relation dans laquelle les extensions physiques sont réalisées sur un support physique. En outre, l’adresse de début de l’étendue physique sur le support physique est spécifiée.

</dd> <dt>

[**\_REBOOTACTION CIM**](cim-rebootaction.md)
</dt> <dd>

La classe [**CIM \_ rebootaction**](cim-rebootaction.md) provoque un redémarrage du système à l’emplacement où l’élément logiciel est installé.

</dd> <dt>

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> <dd>

La classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associe un groupe de redondance composé d’éléments système gérés et indique que, ensemble, les éléments assurent la redondance. Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.

</dd> <dt>

[**\_REDUNDANCYGROUP CIM**](cim-redundancygroup.md)
</dt> <dd>

La [**classe \_ RedundancyGroup CIM**](cim-redundancygroup.md) représente une collection d’éléments système gérés, qui indique que les composants agrégés, ensemble, fournissent une redondance. Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.

</dd> <dt>

[**\_Réfrigération CIM**](cim-refrigeration.md)
</dt> <dd>

La classe de [**\_ réfrigération CIM**](cim-refrigeration.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement frigorifique.

</dd> <dt>

[**\_RELATEDSTATISTICS CIM**](cim-relatedstatistics.md)
</dt> <dd>

L’Association [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) représente les hiérarchies et les dépendances des classes [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) associées.

</dd> <dt>

[**\_REMOTEFILESYSTEM CIM**](cim-remotefilesystem.md)
</dt> <dd>

La classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) représente un système de fichiers distant accessible par le biais d’un service lié au réseau. Dans ce cas, le magasin de fichiers est hébergé par un ordinateur qui joue le rôle de serveur de fichiers.

</dd> <dt>

[**\_REMOVEDIRECTORYACTION CIM**](cim-removedirectoryaction.md)
</dt> <dd>

La classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) supprime les répertoires pour les éléments logiciels.

</dd> <dt>

[**\_REMOVEFILEACTION CIM**](cim-removefileaction.md)
</dt> <dd>

La [**classe \_ RemoveFileAction CIM**](cim-removefileaction.md) désinstalle des fichiers.

</dd> <dt>

[**\_REPLACEMENTSET CIM**](cim-replacementset.md)
</dt> <dd>

La classe [**CIM \_ ReplacementSet**](cim-replacementset.md) agrège les éléments physiques qui doivent être remplacés ensemble. Par exemple, lors du remplacement d’une carte mémoire, les puces de mémoire du composant peuvent également être supprimées et remplacées. Cette association peut être utilisée pour remplacer ou mettre à niveau un ensemble de puces mémoire.

</dd> <dt>

[**\_RESIDESONEXTENT CIM**](cim-residesonextent.md)
</dt> <dd>

La classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) représente une association entre un système de fichiers et l’extension de stockage où elle se trouve. En règle générale, un système de fichiers réside sur un disque logique.

</dd> <dt>

[**\_En cours d’exécution CIM**](cim-runningos.md)
</dt> <dd>

La classe CIM executos représente le système d’exploitation [**\_ en**](cim-runningos.md) cours d’exécution. Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.

</dd> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> <dd>

La [**classe \_ SAPSAPDependency CIM**](cim-sapsapdependency.md) est une association entre deux points d’accès de service (SAP), qui indique que le deuxième SAP est requis pour que le premier SAP se connecte à son service.

</dd> <dt>

[**\_Scanneur CIM**](cim-scanner.md)
</dt> <dd>

Le [**\_ scanneur CIM**](cim-scanner.md) représente les fonctionnalités et la gestion de l’unité logique du scanneur.

</dd> <dt>

[**\_SCSICONTROLLER CIM**](cim-scsicontroller.md)
</dt> <dd>

La classe [**CIM \_ SCSIController**](cim-scsicontroller.md) représente les fonctionnalités et la gestion de l’unité logique du contrôleur SCSI.

</dd> <dt>

[**\_SCSIINTERFACE CIM**](cim-scsiinterface.md)
</dt> <dd>

représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles via un contrôleur SCSI et les caractéristiques d’accès.

</dd> <dt>

[**\_Capteur CIM**](cim-sensor.md)
</dt> <dd>

La classe de [**\_ capteur CIM**](cim-sensor.md) représente un périphérique matériel capable de mesurer les caractéristiques d’une propriété physique (par exemple, les caractéristiques de température ou de tension d’un système informatique unitaire).

</dd> <dt>

[**\_SERIALCONTROLLER CIM**](cim-serialcontroller.md)
</dt> <dd>

La classe [**CIM \_ SerialController**](cim-serialcontroller.md) représente les fonctionnalités et la gestion de l’unité logique de port série.

</dd> <dt>

[**\_SERIALINTERFACE CIM**](cim-serialinterface.md)
</dt> <dd>

La classe [**CIM \_ SerialInterface**](cim-serialinterface.md) représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles par le biais du contrôleur série et les caractéristiques de l’accès.

</dd> <dt>

[**\_Service CIM**](cim-service.md)
</dt> <dd>

La classe de [**\_ service CIM**](cim-service.md) représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle. Un service est un objet à usage général permettant de configurer et de gérer l’implémentation des fonctionnalités. il ne s’agit pas de la fonctionnalité elle-même.

</dd> <dt>

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> <dd>

La classe d’association [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) représente les points d’accès pour un service. Par exemple, il est possible d’accéder à une imprimante par des points d’accès SAP, Macintosh ou de service Windows, qui sont potentiellement hébergés sur différents systèmes.

</dd> <dt>

[**\_SERVICEACCESSPOINT CIM**](cim-serviceaccesspoint.md)
</dt> <dd>

La classe [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) représente la possibilité d’utiliser ou d’appeler un service. Les points d’accès représentent les services qui peuvent être utilisés par d’autres entités.

</dd> <dt>

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> <dd>

La classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) représente une association entre un service et un point d’accès au service (SAP), qui indique que le SAP référencé est utilisé par le service pour fournir ses fonctionnalités.

</dd> <dt>

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dd>

La classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) représente une association entre deux services.

</dd> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dd>

La classe de [**\_ paramètres CIM**](cim-setting.md) représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.

</dd> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> <dd>

La classe [**CIM \_ SettingCheck**](cim-settingcheck.md) spécifie les informations nécessaires pour vérifier un fichier de paramètres particulier pour une entrée spécifique qui contient une valeur égale à la valeur spécifiée. Toutes les comparaisons sont supposées ne pas respecter la casse.

</dd> <dt>

[**\_SETTINGCONTEXT CIM**](cim-settingcontext.md)
</dt> <dd>

La [**classe \_ SettingContext CIM**](cim-settingcontext.md) associe les objets de configuration aux objets Setting.

</dd> <dt>

[**\_Emplacement CIM**](cim-slot.md)
</dt> <dd>

La classe d' [**\_ emplacement CIM**](cim-slot.md) représente les connecteurs dans lesquels des packages sont insérés.

</dd> <dt>

[**\_SLOTINSLOT CIM**](cim-slotinslot.md)
</dt> <dd>

La [**relation \_ SlotInSlot CIM**](cim-slotinslot.md) représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement.

</dd> <dt>

[**\_SOFTWAREELEMENT CIM**](cim-softwareelement.md)
</dt> <dd>

La classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) décompose un [**objet \_ SoftwareFeature CIM**](cim-softwarefeature.md) en un ensemble de parties gérables ou déployables individuellement pour une plateforme particulière. La plateforme d’un élément logiciel est identifiée de manière unique par son architecture matérielle sous-jacente et son système d’exploitation.

</dd> <dt>

[**\_SOFTWAREELEMENTACTIONS CIM**](cim-softwareelementactions.md)
</dt> <dd>

L’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifie les actions d’un élément logiciel.

</dd> <dt>

[**\_SOFTWAREELEMENTCHECKS CIM**](cim-softwareelementchecks.md)
</dt> <dd>

La classe d’association [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.

</dd> <dt>

[**\_SOFTWAREELEMENTVERSIONCHECK CIM**](cim-softwareelementversioncheck.md)
</dt> <dd>

La classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) représente un type d’élément logiciel qui doit exister dans l’environnement.

</dd> <dt>

[**\_SOFTWAREFEATURE CIM**](cim-softwarefeature.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) représente une fonction ou une fonctionnalité particulière d’un produit ou d’un système d’application.

</dd> <dt>

[**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel.

</dd> <dt>

[**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

La classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) représente une association entre un service et la manière dont il est implémenté dans le logiciel.

</dd> <dt>

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

L’Association [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifie les éléments logiciels qui composent une fonctionnalité logicielle spécifique.

</dd> <dt>

[**\_SPAREGROUP CIM**](cim-sparegroup.md)
</dt> <dd>

La classe [**CIM \_ SpareGroup**](cim-sparegroup.md) est dérivée de la classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) et indique qu’un ou plusieurs éléments agrégés peuvent être détachés.

</dd> <dt>

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> <dd>

La [**classe \_ StatisticalInformation CIM**](cim-statisticalinformation.md) est une classe racine pour la collection arbitraire de données statistiques ou de mesures applicables à un ou plusieurs éléments système gérés.

</dd> <dt>

[**\_Statistiques CIM**](cim-statistics.md)
</dt> <dd>

La classe de [**\_ statistiques CIM**](cim-statistics.md) représente une association qui associe les éléments système gérés aux groupes statistiques qui s’y appliquent.

</dd> <dt>

[**\_STORAGEDEFECT CIM**](cim-storagedefect.md)
</dt> <dd>

L’agrégation [**CIM \_ StorageDefect**](cim-storagedefect.md) collecte les erreurs de stockage pour une étendue de stockage.

</dd> <dt>

[**\_STORAGEERROR CIM**](cim-storageerror.md)
</dt> <dd>

La classe [**CIM \_ StorageError**](cim-storageerror.md) représente des blocs d’espace de média ou de mémoire qui sont mappés hors de l’utilisation en raison d’erreurs. La clé de la classe est la **propriété de l’erreur** de taille des octets erronés.

</dd> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> <dd>

La classe [**CIM \_ StorageExtent**](cim-storageextent.md) représente les fonctionnalités et la gestion des différents médias qui existent pour stocker des données et permettre la récupération des données. Cette classe parente peut représenter les différents composants de RAID (matériel ou logiciel) ou une extension logique brute sur les supports physiques.

</dd> <dt>

[**\_STORAGEREDUNDANCYGROUP CIM**](cim-storageredundancygroup.md)
</dt> <dd>

La classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) représente des informations de redondance relatives au stockage de masse.

</dd> <dt>

[**\_SUPPORTACCESS CIM**](cim-supportaccess.md)
</dt> <dd>

La classe [**CIM \_ SupportAccess**](cim-supportaccess.md) définit comment obtenir de l’aide pour un produit.

</dd> <dt>

[**\_SWAPSPACECHECK CIM**](cim-swapspacecheck.md)
</dt> <dd>

La classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) spécifie la quantité d’espace d’échange qui doit être disponible sur le système.

</dd> <dt>

[**\_Système CIM**](cim-system.md)
</dt> <dd>

La [**classe \_ système CIM**](cim-system.md) agrège un ensemble énumérable d’éléments système gérés. L’agrégation fonctionne comme un ensemble fonctionnel. Dans une sous-classe particulière du système, il existe une liste bien définie de classes d’éléments système gérés dont les instances doivent être agrégées.

</dd> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dd>

classe d’association Common Information Model (CIM) qui établit les relations entre un système et les éléments système gérés dont il est composé.

</dd> <dt>

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dd>

L’Association [**CIM \_ SystemDevice**](cim-systemdevice.md) représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.

</dd> <dt>

[**\_SYSTEMRESOURCE CIM**](cim-systemresource.md)
</dt> <dd>

La classe [**CIM \_ SystemResource**](cim-systemresource.md) représente une entité gérée par le BIOS, ou un système d’exploitation qui peut être utilisé par des périphériques logiciels et logiques.

</dd> <dt>

[**\_Tachymètre CIM**](cim-tachometer.md)
</dt> <dd>

La classe du [**\_ tachymètre CIM**](cim-tachometer.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.

</dd> <dt>

[**CIM \_ CIM**](cim-tapedrive.md)
</dt> <dd>

La [**classe \_ CIM CIM**](cim-tapedrive.md) représente un lecteur de bande sur le système. Les lecteurs de bande sont principalement distingués dans le fait qu’ils sont accessibles uniquement de façon séquentielle.

</dd> <dt>

[**\_Capteur CIM**](cim-temperaturesensor.md)
</dt> <dd>

La classe [**CIM \_ capteur**](cim-temperaturesensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.

</dd> <dt>

[**\_Thread CIM**](cim-thread.md)
</dt> <dd>

La classe de [**\_ thread CIM**](cim-thread.md) représente la capacité d’exécuter des unités d’un processus ou d’une tâche, en parallèle. Un processus peut avoir de nombreux threads, chacun d’entre eux étant faible au processus.

</dd> <dt>

[**\_TODIRECTORYACTION CIM**](cim-todirectoryaction.md)
</dt> <dd>

L’Association [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifie le répertoire cible de l’action de fichier.

</dd> <dt>

[**\_TODIRECTORYSPECIFICATION CIM**](cim-todirectoryspecification.md)
</dt> <dd>

L’Association [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifie le répertoire cible de l’action de fichier.

</dd> <dt>

[**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

La classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) représente les fonctionnalités et la gestion d’un onduleur.

</dd> <dt>

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dd>

La classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) représente un ordinateur de bureau, mobile, réseau, serveur ou tout autre type de système informatique à nœud unique.

</dd> <dt>

[**\_USBCONTROLLER CIM**](cim-usbcontroller.md)
</dt> <dd>

La classe [**CIM \_ USBController**](cim-usbcontroller.md) représente les fonctionnalités et la gestion d’un contrôleur USB.

</dd> <dt>

[**\_USBCONTROLLERHASHUB CIM**](cim-usbcontrollerhashub.md)
</dt> <dd>

La classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) définit les hubs en aval du contrôleur USB.

</dd> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> <dd>

La classe [**CIM \_ USBDevice**](cim-usbdevice.md) représente les caractéristiques de gestion d’un périphérique USB.

</dd> <dt>

[**\_Usbhub CIM**](cim-usbhub.md)
</dt> <dd>

La classe [**CIM \_ USBHub**](cim-usbhub.md) représente les fonctionnalités et la gestion d’un concentrateur USB.

</dd> <dt>

[**\_USERDEVICE CIM**](cim-userdevice.md)
</dt> <dd>

La [**classe \_ UserDevice CIM**](cim-userdevice.md) est une classe parente à partir de laquelle d’autres classes, telles que le [**\_ clavier CIM**](cim-keyboard.md) ou [**CIM \_ desktopmonitor**](cim-desktopmonitor.md), descendent. Les appareils utilisateur sont des périphériques logiques qui permettent à l’utilisateur d’un système informatique d’entrer, d’afficher ou d’entendre des données.

</dd> <dt>

[**\_VERSIONCOMPATIBILITYCHECK CIM**](cim-versioncompatibilitycheck.md)
</dt> <dd>

La [**classe \_ VersionCompatibilityCheck CIM**](cim-versioncompatibilitycheck.md) spécifie s’il est autorisé de créer l’état suivant d’un élément logiciel.

</dd> <dt>

[**\_VIDEOBIOSELEMENT CIM**](cim-videobioselement.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.

</dd> <dt>

[**\_VIDEOBIOSFEATURE CIM**](cim-videobiosfeature.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) représente les fonctionnalités du logiciel de bas niveau utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.

</dd> <dt>

[**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

La classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associe une fonctionnalité BIOS vidéo et ses éléments BIOS vidéo agrégés.

</dd> <dt>

[**\_VIDEOCONTROLLER CIM**](cim-videocontroller.md)
</dt> <dd>

La classe [**CIM \_ VideoController**](cim-videocontroller.md) représente les fonctionnalités et la gestion du contrôleur vidéo.

</dd> <dt>

[**\_VIDEOCONTROLLERRESOLUTION CIM**](cim-videocontrollerresolution.md)
</dt> <dd>

La classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) représente les différents modes vidéo qu’un contrôleur vidéo peut prendre en charge.

</dd> <dt>

[**\_VIDEOSETTING CIM**](cim-videosetting.md)
</dt> <dd>

La classe [**CIM \_ VideoSetting**](cim-videosetting.md) associe l’objet de paramètre [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) au contrôleur auquel il s’applique.

</dd> <dt>

[**\_VOLATILESTORAGE CIM**](cim-volatilestorage.md)
</dt> <dd>

La classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) représente les fonctionnalités et la gestion du stockage volatile.

</dd> <dt>

[**\_Capteur CIM**](cim-voltagesensor.md)
</dt> <dd>

La classe [**CIM \_ capteur**](cim-voltagesensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures. Avec les ajouts [**au \_ capteur CIM**](cim-sensor.md) et aux classes [**\_ NumericSensor CIM**](cim-numericsensor.md) dans la version 2,2, il n’est plus nécessaire.

</dd> <dt>

[**\_VOLUMESET CIM**](cim-volumeset.md)
</dt> <dd>

La classe [**CIM \_ VolumeSet**](cim-volumeset.md) représente une plage contiguë de blocs logiques présentée à l’environnement d’exploitation pour la lecture et l’écriture de données utilisateur.

</dd> <dt>

[**\_WORMDRIVE CIM**](cim-wormdrive.md)
</dt> <dd>

La classe [**CIM \_ WORMDrive**](cim-wormdrive.md) représente les fonctionnalités et la gestion d’un lecteur Worm, un sous-type de l’appareil d’accès aux médias.

</dd> </dl>

 

 
