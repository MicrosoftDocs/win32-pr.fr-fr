---
description: Représente un appareil qui peut utiliser un média pour stocker et récupérer des données.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Classe CIM_MediaAccessDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bb97ded03cfc853fc0dde6ede26083be01cf218f210c31f947f315634599e179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900259"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a>Classe CIM_MediaAccessDevice (gestion Hyper-V)

Représente un appareil qui peut utiliser un média pour stocker et récupérer des données.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ MediaAccessDevice** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **CIM \_ MediaAccessDevice** possède ces méthodes.



| Méthode                                               | Description                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [**LockMedia**](cim-mediaaccessdevice-lockmedia.md) | Verrouille et déverrouille les supports amovibles dans un appareil d’accès aux médias.<br/> |



 

### <a name="properties"></a>Propriétés

La classe **CIM \_ MediaAccessDevice** possède les propriétés suivantes.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|appareils de Stockage DMTF \| 001,9 "," MIF. \|appareils de Stockage DMTF \| 001,11 "," MIF. \|appareils de Stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "," MIF. \|Disque hôte DMTF \| 001,2 "," MIF. \|Disque hôte DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")
</dt> </dl>

Tableau qui contient les fonctionnalités de l’appareil d’accès au média.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

**Accès séquentiel** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

**Accès aléatoire** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

**Prend en charge l’écriture** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

**Chiffrement** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

**Compression** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

**Prend en charge les supports amovibles** (7)


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

**Nettoyage manuel** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

**Nettoyage automatique** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

**Notification intelligente** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

**Prend en charge les supports à double face** (11)


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

**Predismount EJECT non requis** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Capacités**»)
</dt> </dl>

Tableau de descriptions des fonctionnalités pour les éléments du tableau de **fonctionnalités** .

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’algorithme ou de l’outil utilisé par l’appareil pour prendre en charge la compression.

Si aucun type de compression n’est spécifié, l’une des valeurs suivantes peut être utilisée :

-   La prise en charge de la compression « inconnue » est inconnue ou non spécifiée.
-   La compression « compressée » est prise en charge, mais le type est inconnu ou non spécifié.
-   « Non compressé » l’appareil ne prend pas en charge les fonctionnalités de compression.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")
</dt> </dl>

Taille de bloc par défaut, en octets, pour l’appareil.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de détection d’erreurs et de correction pris en charge par l’appareil.

</dd> <dt>

**LastCleaned**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure du dernier nettoyage de l’appareil.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)
</dt> </dl>

Temps nécessaire, en millisecondes, pour que l’appareil soit en mesure de lire ou d’écrire un support une fois le chargement du périphérique commencé. Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour les opérations de lecture/écriture. Pour les lecteurs de bande, cette opération démarre lorsque le média est inséré et se termine lorsque le lecteur signale qu’il est prêt pour une application. Il s’agit généralement de la zone de début de bande (BOT) de la bande.

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)
</dt> </dl>

Le temps d’accès maximal du média, en millisecondes. Pour un lecteur de disque, cela représente une recherche complète et un délai de rotation totale. Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement.

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")
</dt> </dl>

Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Les \| appareils d’accès séquentiel DMTF \| 001,2 "," MIF. \|Disque hôte DMTF \| 001,5 ")
</dt> </dl>

Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")
</dt> </dl>

Nombre maximal d’unités qui peuvent être utilisées avant le nettoyage de l’appareil. **UnitsDescription** définit le type d’unité.

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**. Pour les appareils non amovibles, cette valeur doit être **true**.

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")
</dt> </dl>

Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **compteur**
</dt> </dl>

Nombre de fois où le média a été monté pour le transfert de données ou pour nettoyer l’appareil. Si l’appareil ne prend pas en charge les supports amovibles, cette propriété doit être définie sur zéro.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si l’appareil doit être nettoyé ; Sinon, **false**.

> [!Note]  
> La propriété **Capabilities** indique si le nettoyage manuel ou automatique est possible.

 

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Si l’appareil prend en charge plusieurs médias individuels, cette propriété définit le nombre maximal qui peut être pris en charge ou inséré.

</dd> <dt>

**Sécurité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Disques DMTF \| 003,22 ")
</dt> </dl>

Sécurité opérationnelle pour l’appareil.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (3)


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

**Lecture seule** (4)


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

**Verrouillé** (5)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

**Contournement du démarrage** (6)


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

**Contournement de démarrage et lecture seule** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de la dernière montée du média sur l’appareil. Cette propriété est utilisée uniquement par les appareils qui prennent en charge les supports amovibles.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, pendant laquelle le média a été monté pour le transfert de données ou pour nettoyer l’appareil. Si l’appareil ne prend pas en charge les supports amovibles, cette propriété doit être définie sur zéro.

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets par seconde »), **punitif** (« octet/seconde \* 10 ^ 3 »)
</dt> </dl>

Taux de transfert de données soutenu, en kilo-octets, auquel l’appareil peut lire et écrire sur un média. Il s’agit d’un débit de données brutes soutenu. Les taux ou taux maximaux avec compression ne doivent pas être signalés dans cette propriété.

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**CIM \_ MediaAccessDevice**.**UnitsUsed**")
</dt> </dl>

Décrit le type d’unité des propriétés **MaxUnitsBeforeCleaning** et **UnitsUsed** .

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**","**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")
</dt> </dl>

Nombre d’unités utilisées par l’appareil. Cette propriété est utilisée pour déterminer quand l’appareil doit être nettoyé. **UnitsDescription** définit le type d’unité.

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)
</dt> </dl>

Temps nécessaire, en millisecondes, pour que l’appareil passe de la lecture ou de l’écriture du média au déchargement. Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque tournant à des vitesses nominales et un disque qui ne tourne pas. Pour les lecteurs de bande, il s’agit de la durée pendant laquelle un support doit passer de son robot à être complètement éjecté et accessible à un élément sélecteur ou à un opérateur humain.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

