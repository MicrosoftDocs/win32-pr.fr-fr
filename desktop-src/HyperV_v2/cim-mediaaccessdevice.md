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
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106529524"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="879fb-103">Classe CIM_MediaAccessDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="879fb-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="879fb-104">Représente un appareil qui peut utiliser un média pour stocker et récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="879fb-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="879fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="879fb-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="879fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="879fb-106">Members</span></span>

<span data-ttu-id="879fb-107">La classe **CIM \_ MediaAccessDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="879fb-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="879fb-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="879fb-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="879fb-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="879fb-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="879fb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="879fb-110">Methods</span></span>

<span data-ttu-id="879fb-111">La classe **CIM \_ MediaAccessDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="879fb-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="879fb-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="879fb-112">Method</span></span>                                               | <span data-ttu-id="879fb-113">Description</span><span class="sxs-lookup"><span data-stu-id="879fb-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="879fb-114">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="879fb-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="879fb-115">Verrouille et déverrouille les supports amovibles dans un appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="879fb-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="879fb-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="879fb-116">Properties</span></span>

<span data-ttu-id="879fb-117">La classe **CIM \_ MediaAccessDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="879fb-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="879fb-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="879fb-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-119">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="879fb-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="879fb-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-121">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Périphériques de stockage DMTF \| 001,9 "," MIF. \|Périphériques de stockage DMTF \| 001,11 "," MIF. \|Périphériques de stockage DMTF \| 001,12 "," MIF. \|Disques DMTF \| 003,7 "," MIF. \|Disque hôte DMTF \| 001,2 "," MIF. \|Disque hôte DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="879fb-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-122">Tableau qui contient les fonctionnalités de l’appareil d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="879fb-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="879fb-123">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="879fb-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="879fb-124">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="879fb-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="879fb-125">**Accès séquentiel** (2)</span><span class="sxs-lookup"><span data-stu-id="879fb-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="879fb-126">**Accès aléatoire** (3)</span><span class="sxs-lookup"><span data-stu-id="879fb-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="879fb-127">**Prend en charge l’écriture** (4)</span><span class="sxs-lookup"><span data-stu-id="879fb-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="879fb-128">**Chiffrement** (5)</span><span class="sxs-lookup"><span data-stu-id="879fb-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="879fb-129">**Compression** (6)</span><span class="sxs-lookup"><span data-stu-id="879fb-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="879fb-130">**Prend en charge les supports amovibles** (7)</span><span class="sxs-lookup"><span data-stu-id="879fb-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="879fb-131">**Nettoyage manuel** (8)</span><span class="sxs-lookup"><span data-stu-id="879fb-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="879fb-132">**Nettoyage automatique** (9)</span><span class="sxs-lookup"><span data-stu-id="879fb-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="879fb-133">**Notification intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="879fb-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="879fb-134">**Prend en charge les supports à double face** (11)</span><span class="sxs-lookup"><span data-stu-id="879fb-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="879fb-135">**Predismount EJECT non requis** (12)</span><span class="sxs-lookup"><span data-stu-id="879fb-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="879fb-136">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="879fb-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-137">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="879fb-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="879fb-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-139">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="879fb-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-140">Tableau de descriptions des fonctionnalités pour les éléments du tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="879fb-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="879fb-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="879fb-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-144">Nom de l’algorithme ou de l’outil utilisé par l’appareil pour prendre en charge la compression.</span><span class="sxs-lookup"><span data-stu-id="879fb-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="879fb-145">Si aucun type de compression n’est spécifié, l’une des valeurs suivantes peut être utilisée :</span><span class="sxs-lookup"><span data-stu-id="879fb-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="879fb-146">La prise en charge de la compression « inconnue » est inconnue ou non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="879fb-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="879fb-147">La compression « compressée » est prise en charge, mais le type est inconnu ou non spécifié.</span><span class="sxs-lookup"><span data-stu-id="879fb-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="879fb-148">« Non compressé » l’appareil ne prend pas en charge les fonctionnalités de compression.</span><span class="sxs-lookup"><span data-stu-id="879fb-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-149">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="879fb-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-150">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-152">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="879fb-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-153">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="879fb-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="879fb-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-157">Type de détection d’erreurs et de correction pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-158">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="879fb-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-159">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-161">Date et heure du dernier nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-162">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-163">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-165">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)</span><span class="sxs-lookup"><span data-stu-id="879fb-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-166">Temps nécessaire, en millisecondes, pour que l’appareil soit en mesure de lire ou d’écrire un support une fois le chargement du périphérique commencé.</span><span class="sxs-lookup"><span data-stu-id="879fb-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="879fb-167">Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour les opérations de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="879fb-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="879fb-168">Pour les lecteurs de bande, cette opération démarre lorsque le média est inséré et se termine lorsque le lecteur signale qu’il est prêt pour une application.</span><span class="sxs-lookup"><span data-stu-id="879fb-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="879fb-169">Il s’agit généralement de la zone de début de bande (BOT) de la bande.</span><span class="sxs-lookup"><span data-stu-id="879fb-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-170">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-171">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-173">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)</span><span class="sxs-lookup"><span data-stu-id="879fb-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-174">Le temps d’accès maximal du média, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="879fb-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="879fb-175">Pour un lecteur de disque, cela représente une recherche complète et un délai de rotation totale.</span><span class="sxs-lookup"><span data-stu-id="879fb-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="879fb-176">Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement.</span><span class="sxs-lookup"><span data-stu-id="879fb-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-177">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="879fb-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-178">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-180">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="879fb-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-181">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-182">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="879fb-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-183">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-185">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Les \| appareils d’accès séquentiel DMTF \| 001,2 "," MIF. \|Disque hôte DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="879fb-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-186">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-187">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="879fb-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-188">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-190">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")</span><span class="sxs-lookup"><span data-stu-id="879fb-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-191">Nombre maximal d’unités qui peuvent être utilisées avant le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="879fb-192">**UnitsDescription** définit le type d’unité.</span><span class="sxs-lookup"><span data-stu-id="879fb-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-193">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="879fb-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-194">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="879fb-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-196">**true** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="879fb-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="879fb-197">Pour les appareils non amovibles, cette valeur doit être **true**.</span><span class="sxs-lookup"><span data-stu-id="879fb-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-198">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="879fb-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-199">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-201">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitif** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="879fb-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-202">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-203">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="879fb-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-204">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-206">Qualificateurs : **compteur**</span><span class="sxs-lookup"><span data-stu-id="879fb-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="879fb-207">Nombre de fois où le média a été monté pour le transfert de données ou pour nettoyer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="879fb-208">Si l’appareil ne prend pas en charge les supports amovibles, cette propriété doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="879fb-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-209">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="879fb-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-210">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="879fb-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-212">**true** si l’appareil doit être nettoyé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="879fb-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="879fb-213">La propriété **Capabilities** indique si le nettoyage manuel ou automatique est possible.</span><span class="sxs-lookup"><span data-stu-id="879fb-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="879fb-214">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="879fb-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-215">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="879fb-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-217">Si l’appareil prend en charge plusieurs médias individuels, cette propriété définit le nombre maximal qui peut être pris en charge ou inséré.</span><span class="sxs-lookup"><span data-stu-id="879fb-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-218">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="879fb-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="879fb-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-221">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Disques DMTF \| 003,22 ")</span><span class="sxs-lookup"><span data-stu-id="879fb-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-222">Sécurité opérationnelle pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="879fb-223">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="879fb-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="879fb-224">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="879fb-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="879fb-225">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="879fb-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="879fb-226">**Lecture seule** (4)</span><span class="sxs-lookup"><span data-stu-id="879fb-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="879fb-227">**Verrouillé** (5)</span><span class="sxs-lookup"><span data-stu-id="879fb-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="879fb-228">**Contournement du démarrage** (6)</span><span class="sxs-lookup"><span data-stu-id="879fb-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="879fb-229">**Contournement de démarrage et lecture seule** (7)</span><span class="sxs-lookup"><span data-stu-id="879fb-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="879fb-230">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="879fb-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-231">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-233">Date et heure de la dernière montée du média sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="879fb-234">Cette propriété est utilisée uniquement par les appareils qui prennent en charge les supports amovibles.</span><span class="sxs-lookup"><span data-stu-id="879fb-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-235">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-236">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="879fb-238">Durée, en secondes, pendant laquelle le média a été monté pour le transfert de données ou pour nettoyer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="879fb-239">Si l’appareil ne prend pas en charge les supports amovibles, cette propriété doit être définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="879fb-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-240">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="879fb-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-241">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="879fb-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-243">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets par seconde »), **punitif** (« octet/seconde \* 10 ^ 3 »)</span><span class="sxs-lookup"><span data-stu-id="879fb-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-244">Taux de transfert de données soutenu, en kilo-octets, auquel l’appareil peut lire et écrire sur un média.</span><span class="sxs-lookup"><span data-stu-id="879fb-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="879fb-245">Il s’agit d’un débit de données brutes soutenu.</span><span class="sxs-lookup"><span data-stu-id="879fb-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="879fb-246">Les taux ou taux maximaux avec compression ne doivent pas être signalés dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="879fb-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-247">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="879fb-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="879fb-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-250">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**CIM \_ MediaAccessDevice**.**UnitsUsed**")</span><span class="sxs-lookup"><span data-stu-id="879fb-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-251">Décrit le type d’unité des propriétés **MaxUnitsBeforeCleaning** et **UnitsUsed** .</span><span class="sxs-lookup"><span data-stu-id="879fb-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-252">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="879fb-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-253">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-255">Qualificateurs : [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**","**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span><span class="sxs-lookup"><span data-stu-id="879fb-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-256">Nombre d’unités utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="879fb-256">The number of units used by the device.</span></span> <span data-ttu-id="879fb-257">Cette propriété est utilisée pour déterminer quand l’appareil doit être nettoyé.</span><span class="sxs-lookup"><span data-stu-id="879fb-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="879fb-258">**UnitsDescription** définit le type d’unité.</span><span class="sxs-lookup"><span data-stu-id="879fb-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="879fb-259">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="879fb-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="879fb-260">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="879fb-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="879fb-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="879fb-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="879fb-262">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »), **punitif** (« deuxième \* 10 ^-3 »)</span><span class="sxs-lookup"><span data-stu-id="879fb-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="879fb-263">Temps nécessaire, en millisecondes, pour que l’appareil passe de la lecture ou de l’écriture du média au déchargement.</span><span class="sxs-lookup"><span data-stu-id="879fb-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="879fb-264">Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque tournant à des vitesses nominales et un disque qui ne tourne pas.</span><span class="sxs-lookup"><span data-stu-id="879fb-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="879fb-265">Pour les lecteurs de bande, il s’agit de la durée pendant laquelle un support doit passer de son robot à être complètement éjecté et accessible à un élément sélecteur ou à un opérateur humain.</span><span class="sxs-lookup"><span data-stu-id="879fb-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="879fb-266">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="879fb-266">Requirements</span></span>



| <span data-ttu-id="879fb-267">Condition requise</span><span class="sxs-lookup"><span data-stu-id="879fb-267">Requirement</span></span> | <span data-ttu-id="879fb-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="879fb-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="879fb-269">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="879fb-269">Minimum supported client</span></span><br/> | <span data-ttu-id="879fb-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="879fb-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="879fb-271">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="879fb-271">Minimum supported server</span></span><br/> | <span data-ttu-id="879fb-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="879fb-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="879fb-273">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="879fb-273">Namespace</span></span><br/>                | <span data-ttu-id="879fb-274">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="879fb-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="879fb-275">MOF</span><span class="sxs-lookup"><span data-stu-id="879fb-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="879fb-276"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="879fb-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="879fb-277">DLL</span><span class="sxs-lookup"><span data-stu-id="879fb-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="879fb-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="879fb-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="879fb-279">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879fb-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879fb-280">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="879fb-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

