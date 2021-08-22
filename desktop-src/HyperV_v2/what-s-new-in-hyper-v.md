---
description: la Version 2 du fournisseur WMI Hyper-V est une nouveauté pour les Windows 8 et les Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: Nouveautés du fournisseur WMI Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbaab65c08031c291eb11e8f865b77e256e5600deba060e0f8176ec8d13c3714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754929"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>Nouveautés du fournisseur WMI Hyper-V

la Version 2 du fournisseur WMI Hyper-V est une nouveauté pour les Windows 8 et les Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, version 1709

Nouvelles classes :

-   [**\_Batterie MSVM**](msvm-battery.md)
-   [**MSVM \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**MSVM \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Nouvelles propriétés :

-   [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md): **ExportedGuestStateFilePaths**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode** et **DefaultQueueVrssMinQueuePairs**
-   [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading**, **VrssExcludePrimaryProcessor**, **VrssQueueSchedulingModes** et **VrssMinQueuePairs**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **DataAlignment**, **PmemAddressAbstractionType** et **IsPmemCompatible**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **DisableDifferentialOfIgnoredStorage** et **ExcludedVirtualHardDisks**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **HypervisorRootSchedulerEnabled**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **CPUCappingMagnitude** et **CancelIfBlackoutThresholdExceeded**
-   [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md): **ExportedGuestStateFilePath**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **architecture**, **AutomaticSnapshotsEnabled**, **IsAutomaticSnapshot**, **GuestStateFile** et **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10 version 1703

Nouvelles classes :

-   [**MSVM \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**MSVM \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**MSVM \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**MSVM \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**MSVM \_ GpuPartition**](msvm-gpupartition.md)
-   [**MSVM \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**MSVM \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**MSVM \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**MSVM \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**MSVM \_ PciExpress**](msvm-pciexpress.md)
-   [**MSVM \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**MSVM \_ SecurityElement**](msvm-securityelement.md)
-   [**MSVM \_ securityservice**](msvm-securityservice.md)
-   [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**MSVM \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**MSVM \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Classes supprimées :

-   [**MSVM \_ TPMSettingData**](msvm-tpmsettingdata.md)

Nouvelles méthodes :

-   [**MSVM \_ Classe CollectionSnapshotService**](msvm-collectionsnapshotservice.md) : [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**MSVM \_ Classe VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) : [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)et [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**MSVM \_ Classe VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) : [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Nouvelles propriétés :

-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVmmqQueuePairs**, **DefaultQueueVmmqEnabled** et **DefaultQueueVrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VmmqQueuePairs**, **VmmqEnabled** et **VrssEnabled**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **VmmqQueuePairs**, **VmmqEnabled** et **VrssEnabled**
-   [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md): **LastResourceMoveTime**
-   [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md): **DisableHostKVPItems**
-   [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md): **SgxSize** et **SgxEnabled**
-   [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md): **CompatibleForVirtualization** et **DriverModelVersion**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **HwThreadsPerCoreCpuGroupId**, **HideHypervisorPresent** et **ExposeVirtualizationExtensions**
-   [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md): **SupportStatement**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **WriteHardeningMethod**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **protégé**
-   [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md): **AllowPacketDirect**
-   [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md): **LastApplyConsistencyLevel**, **LastApplyVirtualMachineIds**, **LastApplyTime**, **FailedOverReplicationType**, **ReplicationMode** et **ReplicationState**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **ExportForLiveMigration**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **AvoidRemovingVHDs** et **AllowOverwriteExistingFile**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **HighMmioGapSize**
-   [**MSVM \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md): **GuestBackupType**

Propriétés supprimées :

-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **ParentPackage**

## <a name="windows-10"></a>Windows 10

Nouvelles classes :

-   [**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
-   [**\_Collection CIM**](cim-collection.md)
-   [**\_COLLECTIONOFMSES CIM**](cim-collectionofmses.md)
-   [**\_ELEMENTVIEW CIM**](cim-elementview.md)
-   [**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
-   [**\_TPM CIM**](cim-tpm.md)
-   [**\_Vue CIM**](cim-view.md)
-   [**MSVM \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**MSVM \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**MSVM \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**MSVM \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**MSVM \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**MSVM \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**MSVM \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**MSVM \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**MSVM \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**MSVM \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**MSVM \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**MSVM \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**MSVM \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**MSVM \_ ManagementCollection**](msvm-managementcollection.md)
-   [**MSVM \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md)
-   [**MSVM \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**MSVM \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**MSVM \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**MSVM \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**MSVM \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md)
-   [**MSVM \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**MSVM \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**MSVM \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**MSVM \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**\_TPM MSVM**](msvm-tpm.md)
-   [**MSVM \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**MSVM \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**MSVM \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**MSVM \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**MSVM \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**MSVM \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**MSVM \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**MSVM \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**MSVM \_ VssService**](msvm-vssservice.md)

Classe supprimée :

-   [**MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**MSVM \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Nouvelles propriétés :

-   [**MSVM \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md): **LastKnownSwitchName** et **CompartmentGuid**
-   [**MSVM \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **PacketDirectInUse**
-   [**MSVM \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**MSVM \_ EthernetSwitchPortSecuritySettingData**](msvm-ethernetswitchportsecuritysettingdata.md): **EnableFixSpeed10G** et **réservé**
-   [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md): **DefaultEnabledStatePolicy**
-   [**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md): **EnableHostResourceProtection**
-   [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **StorageQoSPolicyID**, **CachingMode** et **SnapshotId**
-   [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md): **InstanceID**, **version**, **ThumbnailImageHeight**, **ThumbnailImageWidth** et **HostComputerSystemName**
-   [**MSVM \_ Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md): **VRAMSizeBytes**
-   [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md): **TeamingEnabled** et **PacketDirectEnabled**
-   [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **ParentTimestamp** et **ParentIdentifier**
-   [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md): **horodateur**
-   [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **BackupIntent** et **DifferentialBackupBase**
-   [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **DefaultVirtualHardDiskCachingMode**
-   [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **RemoveSourceUnmanagedVhds** et **UnmanagedVhds**
-   [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **UserSnapshotType**, **GuestControlledCacheTypes**, **LockOnDisconnect**, **ParentPackage**, **AutomaticCriticalErrorActionTimeout**, **AutomaticCriticalErrorAction**, **ConsoleMode** et **SecureBootTemplateId**

Nouvelles méthodes :

-   [**MSVM \_ Classe ImageManagementService**](msvm-imagemanagementservice.md) : [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)et [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**MSVM \_ Classe ShutdownComponent**](msvm-shutdowncomponent.md) : [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md): [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)et [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**MSVM \_ Classe VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) : [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 et Windows Server 2012 R2

Windows 8.1 et Windows Server 2012 R2 incluent les nouvelles fonctionnalités de la version 2 du fournisseur WMI Hyper-V.

-   Les propriétés **IOPSAllocationUnits**, **IOPSLimit**, **IOPSReservation** et **PersistentReservationsSupported** ont été ajoutées à la classe [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .
-   La propriété **VirtualDiskId** a été ajoutée à la classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) .
-   Des informations sur la qualité de service de stockage ont été ajoutées à la propriété **OperationalStatus** des classes [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) et [**MSVM \_ ResourcePool**](msvm-resourcepool.md) .
-   [**MSVM \_ StorageAlert**](msvm-storagealert.md) , classe
-   La propriété **ClusterMonitored** a été ajoutée aux classes [**MSVM \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) et [**MSVM \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) .
-   Les propriétés **EnableCompression** et **EnableSmbTransport** ont été ajoutées à la [**classe \_ VirtualSystemMigrationServiceSettingData MSVM**](msvm-virtualsystemmigrationservicesettingdata.md) .
-   La propriété **EnableCompression** a été ajoutée à la classe [**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) . La propriété **TransportType** contient des informations sur la migration dynamique.
-   [**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) , classe
-   [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) , classe
-   [**MSVM \_ GuestFileService**](msvm-guestfileservice.md) , classe
-   [**MSVM \_ GuestService**](msvm-guestservice.md) , classe
-   [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) , classe
-   [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) , classe
-   [**MSVM \_ RegisteredGuestService**](msvm-registeredguestservice.md) , classe
-   La propriété **EnhancedSessionModeEnabled** a été ajoutée à la classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .
-   La propriété **EnhancedModeState** et la méthode [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) ont été ajoutées à la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .
-   Les propriétés **BootSourceOrder**, **LowMmioGapSize**, **NetworkBootPreferredProtocol**, **PauseAfterBootFailure** , **SecureBootEnabled** et **VirtualSystemSubType** ont été ajoutées à la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .
-   [**MSVM \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) , classe
-   [**MSVM \_ BootSourceComponent**](msvm-bootsourcecomponent.md) , classe
-   [**MSVM \_ LogicalIdentity**](msvm-logicalidentity.md) , classe
-   [**MSVM \_ CompatibilityVector**](msvm-compatibilityvector.md) , classe
-   La méthode [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) a été ajoutée à la classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .
-   Les propriétés **ReplicationStateEx**, **ReplicationHealthEx**, **EnhancedSessionModeState**, **VirtualSwitchNames** et **VirtualSystemSubType** ont été ajoutées à la classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Les propriétés **ReplicationState** et **ReplicationHealth** sont dépréciées et remplacées par les propriétés **ReplicationStateEx** et **ReplicationHealthEx** .
-   La propriété **PnpDevicePath** a été ajoutée à la classe [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) .
-   Les propriétés **AllowedHashAlgorithms** et **TrustedIssuerCertificateHashes** ont été ajoutées à la [**classe \_ TerminalServiceSettingData MSVM**](msvm-terminalservicesettingdata.md) .

Windows 8.1 et Windows Server 2012 R2 incluent de nouvelles fonctionnalités de réplication de machines virtuelles et de récupération de basculement.

-   [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) , classe
-   [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) , classe
-   Les méthodes [**ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**InitiateFailback**](initiatefailback-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)et [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) ont été ajoutées à la classe [**MSVM \_ ReplicationService**](msvm-replicationservice.md) . Les méthodes **GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** et **ResetReplicationStatisticsEx** remplacent les méthodes [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)et [**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md) .
-   La classe [**MSVM \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md) montre une association entre un ordinateur virtuel et de nombreuses relations de réplication.
-   Les propriétés **AdditionalSettings** et **ReplicationProvider** ont été ajoutées à la [**classe \_ ReplicationSettingData MSVM**](msvm-replicationsettingdata.md) .
-   Des informations sur le fournisseur hôte à hôte ont été ajoutées aux méthodes [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) et [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) de la classe [**MSVM \_ ReplicationService**](msvm-replicationservice.md) .
-   La méthode [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) a été ajoutée à la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) et remplace la méthode [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) . La propriété **InstanceID** peut désormais indiquer une réplication étendue. Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   [**MSVM \_**](msvm-replicationsettingdata.md) Les instances ReplicationSettingData et [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) ont une relation 1:1 que vous pouvez représenter avec une association [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

    | [**MSVM \_**](msvm-settingsdefinestate.md) Nom de la propriété SettingsDefineState | Valeur                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Propriété ManagedElement**                                                          | Représente l’objet [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md)          |
    | **SettingData**                                                             | Représente l’objet [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) associé |

    

     

-   [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) peut faire la différence entre la définition d’instances pour la relation de réplication basée sur la propriété **InstanceID** ou **ReplicationRelationship** . Par conséquent, ces méthodes qui gèrent une seule relation n’ont pas modifié leur signature :

    -   [**MSVM \_ ReplicationService :: CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService :: ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService :: Resync**](resynchronize-msvm-replicationservice.md)
    -   [**MSVM \_ ReplicationService :: StartReplication**](startreplication-msvm-replicationservice.md)

-   Bien que vous puissiez utiliser [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)et [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) Always pour la relation principale, nous vous recommandons d’utiliser à la place [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)et [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) , car ils peuvent traiter la relation de réplication principale et étendue. Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   Bien que ces propriétés de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) continuent d’indiquer l’état de la relation de réplication principale, utilisez plutôt ces propriétés d’un objet [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour déterminer l’état actuel de la relation de réplication principale et étendue.

    | Nom de la propriété                                | Type        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO) |
    | **ReplicationHealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | DateTime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | DateTime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 



