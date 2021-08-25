---
description: cette section contient les documents de référence sur le portage des api Win32 Broadband Mobile déconseillées vers les api Windows Runtime équivalentes.
title: instructions pour le portage des api Win32 haut débit Mobile vers des api Windows Runtime
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767708"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>instructions pour le portage des api Win32 haut débit Mobile vers des api Windows Runtime

ce tableau répertorie les fonctionnalités équivalentes Windows Runtime pour les api haut débit Mobile Win32 déconseillées.

| **IMbnConnection** |  fonctionnalités équivalentes de Windows Runtime |
| - | - |
| Se connecter | ConnectivityManager.AcquireConnectionAsync |
| Déconnecter | ConnectionSession. Close |
| Obtient \_ InterfaceId | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails. HasNewWwanRegistrationState – après notification, l’état actuel de l’inscription peut être récupéré à partir de WwanConnectionProfileDetails. GetNetworkRegistrationState. |
| OnConnectStateChange | NetworkStateChangeEventDetails. HasNewWwanRegistrationState – après notification, l’état actuel de l’inscription peut être récupéré à partir de WwanConnectionProfileDetails. GetNetworkRegistrationState. |
| OnDisconnectComplete | NetworkStateChangeEventDetails. HasNewWwanRegistrationState – après notification, l’état actuel de l’inscription peut être récupéré à partir de WwanConnectionProfileDetails. GetNetworkRegistrationState. |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| Supprimer | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter. GetConnectedProfileAsync |
| GetConnectionProfiles | NetworkInformation. GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession. CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession. CloseSession |
| Obtient \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| SetCommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesContext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| Obtient \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| Obtient \_ MaxDataSize | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession.DataReceived |
| **IMbnInterface** | |
| Obtient \_ InterfaceId | MobileBroadbandAccount.NetworkAccountId |
| GetConnection | ConnectionSession obtenu à partir de AcquireConnectionAsync |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| GetInterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterfaceArrival | MobileBroadbandAccountWatcher.AccountAdded |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher. compte |
| **IMbnMultiCarrier** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarrierEvents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| Modifier | MobileBroadbandPin.ChangeAsync |
| Désactiver | MobileBroadbandPin.DisableAsync |
| Activer | MobileBroadbandPin.EnableAsync |
| Entrez | MobileBroadbandPin.EnterAsync |
| Obtient \_ PinFormat | MobileBroadbandPin. format |
| Obtient \_ PinLengthMax | MobileBroadbandPin. MaxLength |
| Obtient \_ PinLengthMin | MobileBroadbandPin. MaxLength |
| Obtient \_ PinMode | MobileBroadbandPin. Enabled |
| Obtient \_ PinType | MobileBroadbandPin. type |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| Verrouillage | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin. LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| Obtient \_ SoftwareRadioState | Radio. GetRadiosAsync – radio. State |
| SetSoftwareRadioState | Radio. SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | Radio. StateChanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation. DataClasses |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| GetProviderID | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| GetRegisterState | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile. GetSignalBar/MobileBroadbandCellLte. ReferenceSignalReceivedPowerInDBm/MobileBroadbandCellGsm. ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2. SmscAddress, SmsDevice2. CellularClass, None pour CDMAShortMessageSize et MaxMessageIndex, qui n’est pas requis en tant qu’API publique. |
| SetSmsConfiguration | SmsDevice2. SmscAddress, aucun autre paramètre n’est pris en charge |
| SmsSendCdma | SendMessageAndGetResultAsync à l’aide de CellularClass dans ISmsMessageBase |
| SmsSendCdmaPdu | SendMessageAndGetResultAsync utilisant MessageType et CellularClass dans ISmsMessageBase |
| SmsSendPdu | SendMessageAndGetResultAsync utilisant MessageType dans ISmsMessageBase |
| **IMbnSmsConfiguration** | |
| Obtient \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| Obtient \_ SmsFormat | SmsDevice2.CellularClass |
| put \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration. MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| recevoir un \_ message | SmsTextMessage2. Body |
| Obtient \_ PduData | SmsTextmessage2. Body |
| **IMbnSmsReadMsgTextCdma** | |
| recevoir l' \_ adresse | SmsTextMessage2. from |
| Obtient \_ EncodingID | SmsTextMessage2. Encoding |
| recevoir un \_ message | SmsTextMessage2. Body |
| recevoir l' \_ horodateur | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| Obtient \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| Obtient \_ abonné | MobileBroadbandDeviceInformation. abonné |
| Obtient \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |
