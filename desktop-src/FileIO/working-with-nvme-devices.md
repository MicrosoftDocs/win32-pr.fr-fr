---
description: Découvrez comment utiliser des appareils NVMe à haut débit à partir de votre application Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Utilisation des lecteurs NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521474"
---
# <a name="working-with-nvme-drives"></a>Utilisation des lecteurs NVMe

**S’applique à :**

-   Windows 10
-   Windows Server 2016

Découvrez comment utiliser des appareils NVMe à haut débit à partir de votre application Windows. L’accès aux appareils est activé via **StorNVMe.sys**, le pilote intégré introduit pour la première fois dans Windows Server 2012 R2 et Windows 8.1. Elle est également disponible pour les appareils Windows 7 via un correctif logiciel de base de connaissances. Dans Windows 10, plusieurs nouvelles fonctionnalités ont été introduites, notamment un mécanisme direct pour les commandes NVMe spécifiques au fournisseur et les mises à jour des IOCTL existants.

Cette rubrique fournit une vue d’ensemble des API d’utilisation générale que vous pouvez utiliser pour accéder aux lecteurs NVMe dans Windows 10. Elle décrit également les éléments suivants :

-   Envoi d’une commande NVMe spécifique à un fournisseur avec [transfert direct](#pass-through-mechanism)
-   Comment [Envoyer une commande d’identification, d’obtention de fonctionnalités ou d’obtention de pages de journal](#protocol-specific-queries) au lecteur NVMe
-   Obtention d' [informations de température](#temperature-queries) à partir d’un lecteur NVMe
-   Comment exécuter des commandes de modification de comportement, telles que la [définition de seuils de température](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>API pour l’utilisation des lecteurs NVMe

Vous pouvez utiliser les API d’utilisation générale suivantes pour accéder aux lecteurs NVMe dans Windows 10. Ces API se trouvent dans **winioctl. h** pour les applications en mode utilisateur, et **ntddstor. h** pour les pilotes en mode noyau. Pour plus d’informations sur les fichiers d’en-tête, consultez [fichiers d’en-tête](#header-files).

-   [**IOCTL \_ \_ \_ Commande de protocole de stockage**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : utilisez cette IOCTL avec la structure de **\_ \_ commande du protocole de stockage** pour émettre des commandes NVMe. Cette IOCTL active l’interconnexion NVMe et prend en charge le journal des effets de commande dans NVMe. Vous pouvez l’utiliser avec des commandes spécifiques au fournisseur. Pour plus d’informations, consultez [mécanisme direct](#pass-through-mechanism).

-   [**Stockage \_ \_Commande de protocole**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : cette structure de mémoire tampon d’entrée comprend un champ **ReturnStatus** qui peut être utilisé pour signaler les valeurs d’État suivantes.
    -   **État du protocole de stockage \_ \_ \_ en attente**
    -   **État du protocole de stockage \_ \_ \_ réussite**
    -   **\_erreur d' \_ État du protocole de stockage \_**
    -   **demande d’État du protocole de stockage \_ \_ \_ non valide \_**
    -   **État du protocole de stockage \_ \_ \_ sans \_ appareil**
    -   **État du protocole de stockage \_ \_ \_ occupé**
    -   **\_dépassement des \_ données d’État du protocole de stockage \_ \_**
    -   **État du protocole de stockage- \_ \_ \_ ressources insuffisantes \_**
    -   **État du protocole de stockage \_ \_ \_ non \_ pris en charge**
-   [**IOCTL \_ \_ \_ Propriété de requête de stockage**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : utilisez cette IOCTL avec la structure de **\_ \_ requête de propriété de stockage** pour récupérer les informations de l’appareil. Pour plus d’informations, consultez requêtes [spécifiques au protocole](#protocol-specific-queries) et [requêtes de température](#temperature-queries).

-   [**Stockage \_ \_Requête de propriété**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : cette structure comprend les champs **PropertyId** et **AdditionalParameters** pour spécifier les données à interroger. Dans le champ **PropertyId** , utilisez l’énumération de l' **\_ \_ ID de propriété de stockage** pour spécifier le type de données. Utilisez le champ **AdditionalParameters** pour spécifier plus de détails, en fonction du type de données. Pour les données spécifiques au protocole, utilisez la structure de **\_ \_ \_ données spécifique au protocole de stockage** dans le champ **AdditionalParameters** . Pour les données de température, utilisez la structure d' **\_ \_ informations** sur la température du stockage dans le champ **AdditionalParameters** .
-   [**Stockage \_ \_ID de propriété**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : cette énumération comprend de nouvelles valeurs qui permettent à la **\_ \_ \_ propriété de requête de stockage IOCTL** d’extraire des informations relatives au protocole et à la température.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Utilisez l’un de ces ID de propriété spécifiques au protocole en association avec des **\_ \_ \_ données de protocole de stockage** pour récupérer des données spécifiques au protocole dans la structure du [**\_ \_ \_ descripteur des données de protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Utilisez l’un de ces ID de propriété de température pour récupérer les données de température dans la structure du [**\_ \_ \_ descripteur des données de température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .

-   [**Stockage \_ \_ \_ Données spécifiques au protocole**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : permet de récupérer les données spécifiques à NVMe lorsque cette structure est utilisée pour le champ **AdditionalParameters** de la **\_ \_ requête de propriété de stockage** et qu’une valeur enum de [**\_ \_ \_ \_ type de données NVMe du protocole de stockage**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) est spécifiée. Utilisez l’une des valeurs **de \_ \_ type de \_ données \_ NVME du protocole de stockage** suivantes dans le champ **DataType** de la structure de **\_ \_ \_ données spécifique au protocole de stockage** :

    -   Utilisez **NVMeDataTypeIdentify** pour identifier les données du contrôleur ou identifier les données de l’espace de noms.
    -   Utilisez **NVMeDataTypeLogPage** pour accéder aux pages de journal (y compris les données d’intégrité/de santé).
    -   Utilisez **NVMeDataTypeFeature** pour récupérer les fonctionnalités du lecteur NVMe.

-   [**Stockage \_ \_Informations de température**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : cette structure est utilisée pour stocker des données de température spécifiques. Elle est utilisée dans le **\_ \_ \_ descripteur des données de TEMERATURE de stockage** pour retourner les résultats d’une requête de température.

-   [**IOCTL \_ \_Seuil de \_ température \_ du jeu de stockage**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : utilisez cette IOCTL avec la structure du **\_ \_ seuil de température de stockage** pour définir les seuils de température. Pour plus d’informations, consultez [commandes de changement de comportement](#behavior-changing-commands).

-   [**Stockage \_ \_Seuil de température**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : cette structure est utilisée comme mémoire tampon d’entrée pour spécifier le seuil de température. Le champ de **surseuil** (booléen) spécifie si le champ de **seuil** est la valeur de seuil supérieur ou non (dans le cas contraire, il s’agit de la valeur de seuil).

## <a name="pass-through-mechanism"></a>Mécanisme de transfert

Les commandes qui ne sont pas définies dans la spécification NVMe sont les plus difficiles à gérer par le système d’exploitation hôte : l’hôte n’a pas d’informations sur les effets que les commandes peuvent avoir sur l’appareil cible, l’infrastructure exposée (espaces de noms/tailles de bloc) et son comportement.

Pour mieux transporter de telles commandes spécifiques à des appareils via la pile de stockage Windows, un nouveau mécanisme direct permet de transférer les commandes spécifiques au fournisseur. Ce canal direct vous aide également à développer des outils de gestion et de test. Toutefois, ce mécanisme direct nécessite l’utilisation du journal des effets de commande. En outre, StoreNVMe.sys nécessite que toutes les commandes, et non pas uniquement les commandes de transfert, soient décrites dans le journal des effets de commande.

> [!IMPORTANT]
> StorNVMe.sys et Storport.sys bloquent toute commande sur un appareil s’il n’est pas décrit dans le journal des effets de commande.

 

### <a name="supporting-the-command-effects-log"></a>Prise en charge du journal des effets de commande

Le journal des effets de commande (comme décrit dans commandes prises en charge et effets, section 5.10.1.5 de la [spécification NVMe 1,2](https://nvmexpress.org/specifications)) permet de décrire les effets des commandes spécifiques au fournisseur, ainsi que les commandes définies par la spécification. Cela facilite la validation de la prise en charge des commandes, ainsi que l’optimisation du comportement des commandes, et doivent donc être implémentées pour l’ensemble des commandes que l’appareil prend en charge. Les conditions suivantes décrivent le résultat de l’envoi de la commande en fonction de son entrée de journal des effets de commande.

Pour toute commande spécifique décrite dans le journal des effets de commande...

**Pendant**:

-   La commande prise en charge (CSUPP) est définie sur « 1 », ce qui signifie que la commande est prise en charge par le contrôleur (bit 01)

    > [!Note]  
    > Quand CSUPP a la valeur « 0 » (ce qui signifie que la commande n’est pas prise en charge), la commande est bloquée

     

**Et si** l’une des conditions suivantes est définie :

-   La modification de la capacité du contrôleur (CCC) est définie sur « 1 », ce qui signifie que la commande peut modifier les fonctionnalités du contrôleur (bit 04)

-   La modification de l’inventaire des espaces de noms (NIC) est définie sur « 1 », ce qui signifie que la commande peut modifier le nombre, ou les fonctionnalités de plusieurs espaces de noms (bit 03)

-   La modification de la capacité d’espace de noms (CNSFM) est définie sur « 1 », ce qui signifie que la commande peut modifier les fonctionnalités d’un espace de noms unique (bit 02)

-   L’exécution de la commande (CSE) a la valeur 001B ou 010b, ce qui signifie que la commande peut être envoyée quand aucune autre commande n’est en suspens au même espace de noms ou à un espace de noms quelconque, et qu’une autre commande ne doit pas être envoyée au même espace de noms ou à un espace de noms jusqu’à ce que cette commande soit terminée (bits 18:16)

La commande est **alors** envoyée comme seule commande en suspens pour l’adaptateur.

**Sinon, si**:

-   La valeur de l’exécution de la commande est définie sur 001B, ce qui signifie que la commande peut être envoyée lorsqu’il n’existe aucune autre commande en suspens vers le même espace de noms, et qu’une autre commande ne doit pas être envoyée au même espace de noms tant que cette commande n’est pas terminée (bits 18:16)

La commande est **alors** envoyée comme seule commande en suspens à l’objet de numéro d’unité logique (LUN).

Dans le **cas contraire**, la commande est envoyée avec d’autres commandes en attente sans inhibition. Par exemple, si une commande spécifique au fournisseur est envoyée à l’appareil pour récupérer des informations statistiques qui ne sont pas définies par des spécifications, il ne doit y avoir aucun risque de modifier le comportement ou la capacité de l’appareil à exécuter des commandes d’e/s. De telles demandes peuvent être effectuées en parallèle à des e/s et aucune pause-reprise n’est nécessaire.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Utilisation \_ de la \_ \_ commande du protocole de stockage ioctl pour envoyer des commandes

Le transfert direct peut être effectué à l’aide de la [**\_ commande de \_ protocole \_ de stockage IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduite dans Windows 10. Cette IOCTL a été conçue pour avoir un comportement similaire à celui des IOCTL pass-through SCSI et ATA existants, pour envoyer une commande incorporée à l’appareil cible. Via cette IOCTL, l’envoi direct peut être envoyé à un périphérique de stockage, y compris un lecteur NVMe.

Par exemple, dans NVMe, l’IOCTL autorise l’envoi des codes de commande suivants.

-   Commandes d’administration spécifiques au fournisseur (C0H – FFh)
-   Commandes NVMe spécifiques au fournisseur (80h – FFh)

Comme avec toutes les autres IOCTL, utilisez [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) pour envoyer l’IOCTL direct. L’IOCTL est remplie à l’aide de la structure de mémoire tampon d’entrée de [**\_ \_ commande du protocole de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) trouvée dans **ntddstor. h**. Renseignez le champ de **commande** avec la commande spécifique au fournisseur.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



La commande spécifique au fournisseur à envoyer doit être renseignée dans le champ en surbrillance ci-dessus. Notez à nouveau que le journal des effets de commande doit être implémenté pour les commandes directes. En particulier, ces commandes doivent être signalées telles qu’elles sont prises en charge dans le journal des effets de commande (voir la section précédente pour plus d’informations). Notez également que les champs PRP sont spécifiques aux pilotes, ce qui signifie que les applications qui envoient des commandes peuvent les conserver sous la forme 0.

Enfin, cette IOCTL directe est destinée à l’envoi de commandes spécifiques au fournisseur. Pour envoyer d’autres commandes NVMe d’administration ou non spécifiques à un fournisseur, telles que l’identification, cette IOCTL directe ne doit pas être utilisée. Par exemple, **la \_ \_ \_ propriété de requête de stockage IOCTL** doit être utilisée pour identifier ou obtenir des pages de journal. Pour plus d’informations, consultez la section suivante, [requêtes spécifiques au protocole](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Ne pas mettre à jour le microprogramme via le mécanisme de transfert

Les commandes de téléchargement et d’activation du microprogramme ne doivent pas être envoyées à l’aide de direct. **IOCTL \_ La \_ \_ commande de protocole de stockage** doit être utilisée uniquement pour les commandes spécifiques au fournisseur.

Au lieu de cela, utilisez les opérations d’IOCTL de stockage générales suivantes (introduites dans Windows 10) pour éviter les applications directement à l’aide \_ de la version de miniport SCSI de l’IOCTL du microprogramme. Les pilotes de stockage traduisent l’IOCTL en une commande SCSI ou la \_ version de miniport SCSI de l’IOCTL sur le miniport.

Ces IOCTL sont recommandées pour développer les outils de mise à niveau de microprogramme dans Windows 10 et Windows Server 2016 :

-   [**\_informations de \_ récupération du microprogramme de stockage IOCTL \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**\_ \_ Téléchargement du microprogramme de stockage IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_ \_ activation du microprogramme de stockage IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Pour obtenir des informations de stockage et mettre à jour le microprogramme, Windows prend également en charge les applets de commande PowerShell pour effectuer cette tâche rapidement :

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Pour mettre à jour le microprogramme sur NVMe dans Windows 8.1, utilisez le \_ \_ microprogramme de miniport SCSI IOCTL \_ . Cette IOCTL n’a pas été reportée vers Windows 7. Pour plus d’informations, consultez [mise à niveau du microprogramme d’un appareil NVMe dans Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Retour d’erreurs via le mécanisme de transfert

À l’instar des IOCTL SCSI et ATA directe, quand une commande/demande est envoyée au miniport ou au périphérique, l’IOCTL retourne si elle a réussi ou non. Dans la structure de [**\_ \_ commande du protocole de stockage**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , l’IOCTL retourne l’état via le champ **ReturnStatus** .

### <a name="example-sending-a-vendor-specific-command"></a>Exemple : envoi d’une commande spécifique au fournisseur

Dans cet exemple, une commande arbitraire spécifique au fournisseur (0xFF) est envoyée via un transfert vers un lecteur NVMe. Le code suivant alloue une mémoire tampon, Initialise une requête, puis envoie la commande à l’appareil via DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



Dans cet exemple, nous nous attendons à ce que `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` la commande aboutisse à l’appareil.

## <a name="protocol-specific-queries"></a>Requêtes spécifiques au protocole

Windows 8.1 a introduit la [**\_ propriété de \_ requête \_ de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour la récupération des données. Dans Windows 10, l’IOCTL a été améliorée pour prendre en charge les fonctionnalités NVMe couramment demandées, telles que les **pages de journalisation**, les **fonctionnalités d’extraction** et l' **identification**. Cela permet la récupération d’informations spécifiques à NVMe à des fins de surveillance et d’inventaire.

La mémoire tampon d’entrée pour la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) ioctl (à partir de Windows 10) est présentée ici.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Lorsque vous utilisez la [**\_ propriété de \_ requête \_ de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour récupérer les informations spécifiques au protocole NVMe dans le [**\_ \_ \_ descripteur des données de protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configurez la structure de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) comme suit :

-   Allouez une mémoire tampon qui peut contenir à la fois une [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) et une structure de [**\_ \_ \_ données spécifique**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) à un protocole de stockage.

-   Définissez le champ **PropertyId** sur **StorageAdapterProtocolSpecificProperty** ou **StorageDeviceProtocolSpecificProperty** pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.

-   Définissez le champ **QueryType** sur **PropertyStandardQuery**.

-   Remplissez la structure de [**\_ \_ \_ données spécifique au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) avec les valeurs souhaitées. Le début des **\_ \_ \_ données spécifiques au protocole de stockage** est le champ **AdditionalParameters** de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

La [**structure \_ \_ des \_ données spécifiques au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (à partir de Windows 10) est indiquée ici.


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Pour spécifier un type d’informations propres au protocole NVMe, configurez la structure de [**\_ \_ \_ données spécifique au protocole de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) comme suit :

-   Définissez le champ **ProtocolType** sur **ProtocolTypeNVMe**.

-   Définissez le champ **DataType** sur une valeur d’énumération définie par le [**\_ \_ \_ \_ type de données NVME du protocole de stockage**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Utilisez **NVMeDataTypeIdentify** pour identifier les données du contrôleur ou identifier les données de l’espace de noms.
    -   Utilisez **NVMeDataTypeLogPage** pour accéder aux pages de journal (y compris les données d’intégrité/de santé).
    -   Utilisez **NVMeDataTypeFeature** pour récupérer les fonctionnalités du lecteur NVMe.

Lorsque **ProtocolTypeNVMe** est utilisé comme le **ProtocolType**, les requêtes relatives aux informations spécifiques au protocole peuvent être récupérées en parallèle avec d’autres e/s sur le lecteur NVMe.

Les exemples suivants illustrent des requêtes spécifiques au protocole NVMe.

### <a name="example-nvme-identify-query"></a>Exemple : requête d’identification NVMe

Dans cet exemple, la demande d' **identification** est envoyée à un lecteur NVMe. Le code suivant initialise la structure de données de la requête, puis l’envoie à l’appareil via DeviceIoControl.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



Notez que l’appelant doit allouer une seule mémoire tampon contenant \_ \_ la requête de propriété de stockage et la taille des \_ données spécifiques au protocole de stockage \_ \_ . Dans cet exemple, il utilise la même mémoire tampon pour l’entrée et la sortie de la requête de propriété. C’est la raison pour laquelle la mémoire tampon qui a été allouée a une taille de « décalage de champ \_ (requête de propriété de stockage \_ \_ , AdditionalParameters) + sizeof ( \_ données spécifiques au protocole de stockage \_ \_ ) + \_ taille maximale des \_ journaux NVME \_ ». Bien qu’il soit possible d’allouer des tampons distincts à la fois pour l’entrée et la sortie, nous vous recommandons d’utiliser une seule mémoire tampon pour interroger les informations relatives à NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Exemple : requête des pages du journal d’extraction NVMe

Dans cet exemple, en fonction de la précédente, la requête _ *obtenir le journal des pages** est envoyée à un lecteur NVMe. Le code suivant prépare la structure des données de la requête, puis envoie la commande à l’appareil via DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Exemple : requête obtenir des fonctionnalités NVMe

Dans cet exemple, en fonction de la précédente, la demande _ *obtenir des fonctionnalités** est envoyée à un lecteur NVMe. Le code suivant prépare la structure des données de la requête, puis envoie la commande à l’appareil via DeviceIoControl.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a>Ensemble spécifique au protocole

À partir de Windows 10 19H1, le IOCTL_STORAGE_SET_PROPERTY a été amélioré pour prendre en charge les fonctionnalités Set NVMe.

La mémoire tampon d’entrée pour le IOCTL_STORAGE_SET_PROPERTY est présentée ici :

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

Quand vous utilisez IOCTL_STORAGE_SET_PROPERTY pour définir la fonctionnalité NVMe, configurez la structure STORAGE_PROPERTY_SET comme suit :

-   Allouez une mémoire tampon qui peut contenir à la fois une STORAGE_PROPERTY_SET et une structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT ;
-   Définissez le champ PropertyID sur StorageAdapterProtocolSpecificProperty ou StorageDeviceProtocolSpecificProperty pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.
-   Remplissez la structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT avec les valeurs souhaitées. Le début de la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT est le champ AdditionalParameters de STORAGE_PROPERTY_SET.

La structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT est présentée ici.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Pour spécifier un type de fonctionnalité NVMe à définir, configurez la structure STORAGE_PROTOCOL_SPECIFIC_DATA_EXT comme suit :
-   Définissez le champ ProtocolType sur ProtocolTypeNvme ;
-   Définissez le champ DataType sur la valeur d’énumération NVMeDataTypeFeature définie par STORAGE_PROTOCOL_NVME_DATA_TYPE ;

Les exemples suivants illustrent l’ensemble de fonctionnalités NVMe.

### <a name="example-nvme-set-features"></a>Exemple : fonctions set de NVMe

Dans cet exemple, la demande Set features est envoyée à un lecteur NVMe. Le code suivant prépare la structure de données Set, puis envoie la commande à l’appareil via DeviceIoControl.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Requêtes de température

Dans Windows 10, [**la \_ \_ \_ propriété requête de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) peut également être utilisée pour interroger des données de température à partir d’appareils NVMe.

Pour récupérer les informations de température d’un lecteur NVMe dans le [**\_ \_ \_ descripteur des données de température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configurez la structure de la [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) comme suit :

-   Allouez une mémoire tampon qui peut contenir une structure de [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .

-   Définissez le champ **PropertyId** sur **StorageAdapterTemperatureProperty** ou **StorageDeviceTemperatureProperty** pour une demande de contrôleur ou d’appareil/espace de noms, respectivement.

-   Définissez le champ **QueryType** sur **PropertyStandardQuery**.

La structure d' [**\_ \_ informations sur la température de stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (à partir de Windows 10) est indiquée ici.


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Commandes de modification de comportement

Les commandes qui manipulent les attributs de l’appareil ou qui peuvent avoir un impact sur le comportement de l’appareil sont plus difficiles à traiter par le système d’exploitation. Si les attributs de l’appareil changent au moment de l’exécution pendant le traitement des e/s, des problèmes de synchronisation ou d’intégrité des données peuvent survenir si le traitement n’est pas correct.

La commande **Set-featurs** NVMe est un bon exemple de commande de changement de comportement. Il permet de modifier le mécanisme d’arbitrage et le paramétrage des seuils de température. Pour s’assurer que les données en cours ne sont pas menacées lorsque des commandes SET affectant le comportement sont envoyées, Windows suspend toutes les e/s sur l’appareil NVMe, draine les files d’attente et vide les tampons. Une fois l’exécution de la commande set terminée, l’e/s reprend (si possible). Si les e/s ne peuvent pas être reprises, une réinitialisation de l’appareil peut être nécessaire.

### <a name="setting-temperature-thresholds"></a>Définition des seuils de température

Windows 10 a introduit le [**seuil de température du \_ jeu de stockage \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), une ioctl pour l’obtention et la définition des seuils de température. Vous pouvez également l’utiliser pour récupérer la température actuelle de l’appareil. La mémoire tampon d’entrée/sortie pour cette IOCTL est la structure d' [**\_ \_ informations sur la température du stockage**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , à partir de la section de code précédente.

### <a name="example-setting-over-threshold-temperature"></a>Exemple : définition de la température sur seuil

Dans cet exemple, la température de dépassement du seuil d’un lecteur NVMe est définie. Le code suivant prépare la commande, puis l’envoie à l’appareil via DeviceIoControl.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Définition des fonctionnalités spécifiques au fournisseur

Sans le journal des effets de commande, le pilote n’a aucune connaissance des ramifications de la commande. C’est la raison pour laquelle le journal des effets de commande est requis. Il permet au système d’exploitation de déterminer si une commande a un impact important et si elle peut être envoyée en parallèle avec d’autres commandes sur le lecteur.

Le journal des effets de commandes n’est pas encore suffisamment granulaire pour englober les commandes **Set-features** spécifiques au fournisseur. Pour cette raison, il n’est pas encore possible d’envoyer des commandes **Set-features** spécifiques au fournisseur. Toutefois, il est possible d’utiliser le mécanisme de transfert, décrit précédemment, pour envoyer des commandes spécifiques au fournisseur. Pour plus d’informations, consultez [mécanisme direct](#pass-through-mechanism).

## <a name="header-files"></a>Fichiers d’en-tête

Les fichiers suivants s’appliquent au développement NVMe. Ces fichiers sont fournis avec le [Kit de développement logiciel (SDK) Microsoft Windows](https://developer.microsoft.com/windows/downloads).



| Fichier d’en-tête    | Description                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor. h** | Définit des constantes et des types pour accéder aux pilotes de la classe de stockage à partir du mode noyau.   |
| **nVMe. h**     | Pour d’autres structures de données associées à NVMe.                                                 |
| **winioctl. h** | Pour les définitions globales IOCTL Win32, y compris les API de stockage pour les applications en mode utilisateur. |



 

 

 
