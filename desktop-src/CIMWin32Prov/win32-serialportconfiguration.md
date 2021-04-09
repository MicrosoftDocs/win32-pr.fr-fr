---
description: La \_ classe WMI Win32 SerialPortConfiguration représente les paramètres de transmission de données sur un port série Windows. Cela comprend les configurations permettant d’établir une connexion et une vérification des erreurs.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950449"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="e8f2e-104">\_Classe SerialPortConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="e8f2e-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="e8f2e-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SerialPortConfiguration** représente les paramètres de transmission de données sur un port série Windows.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="e8f2e-106">Cela comprend les configurations permettant d’établir une connexion et une vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="e8f2e-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e8f2e-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8f2e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8f2e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="e8f2e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e8f2e-110">Members</span></span>

<span data-ttu-id="e8f2e-111">La classe **Win32 \_ SerialPortConfiguration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e8f2e-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="e8f2e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8f2e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8f2e-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e8f2e-113">Properties</span></span>

<span data-ttu-id="e8f2e-114">La classe **Win32 \_ SerialPortConfiguration** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8f2e-115">**AbortReadWriteOnError**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-118">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-119">Si la **valeur est true**, les opérations de lecture et d’écriture sont terminées si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="e8f2e-120">Si la **valeur est true**, le pilote met fin à toutes les opérations de lecture et d’écriture avec un état d’erreur si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="e8f2e-121">Le pilote n’accepte aucune autre opération de communication tant que l’application n’a pas confirmé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-122">**BaudRate**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-125">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| structures de communication win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baudrate »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-126">Vitesse en bauds (bits par seconde) à laquelle l’appareil de communication fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="e8f2e-127">Exemple : 9600</span><span class="sxs-lookup"><span data-stu-id="e8f2e-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-128">**BinaryModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-129">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-131">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-132">Si la **valeur est true**, les transferts de données en mode binaire sont activés pour le port série.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="e8f2e-133">Les systèmes informatiques qui exécutent Windows autorisent uniquement les transferts binaires via les ports série. cette valeur est donc toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-134">**BitsPerByte**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-135">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| , octets)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-138">Nombre de bits transmis et reçus pour chaque octet de données pour le port série Windows.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="e8f2e-139">Le nombre peut varier selon les bits de contrôle et de correction d’erreur, tels que les bits de parité.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="e8f2e-140">Exemple : 8</span><span class="sxs-lookup"><span data-stu-id="e8f2e-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-144">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-145">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-145">Short textual description of the current object.</span></span>

<span data-ttu-id="e8f2e-146">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-150">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-151">Si la **valeur est true**, les transmissions de données continuent lorsque la mémoire tampon d’entrée se trouve dans **XOffXMitThreshold** octets de plein et que le pilote a transmis la valeur **XOffChararcter** pour arrêter la réception d’octets.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="e8f2e-152">Si la valeur est **false**, la transmission ne continue pas tant que la mémoire tampon d’entrée ne se trouve pas dans **XOnXMitThreshold** octets de vide et que le pilote a transmis la valeur **XOnCharacter** pour reprendre la réception.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-153">**CTSOutflowControl**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-154">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-156">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-157">Si la **valeur est true**, le signal CTS (Clear to Send) est vérifié avant de transmettre les données.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="e8f2e-158">CTS signale que les deux appareils sur la connexion série sont prêts à transférer des données.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="e8f2e-159">La transmission de données est suspendue jusqu’à ce que le signal CTS soit donné.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-160">**Description**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-163">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-163">Textual description of the current object.</span></span>

<span data-ttu-id="e8f2e-164">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-165">**DiscardNULLBytes**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-166">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-168">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-169">Si la **valeur est true**, les octets **nuls** (caractères) sont ignorés lorsqu’ils sont reçus.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-171">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-173">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-174">Si la **valeur est true**, le contrôle de flux de données est activé lorsqu’il existe une condition de jeu de données prêt (DSR).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="e8f2e-175">DSR signale que la connexion a été établie par les appareils sur la connexion série.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="e8f2e-176">La transmission des données DSR est suspendue jusqu’à ce que le signal DSR soit donné.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-177">**Sensibilité DSR**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-178">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-180">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-181">Si la **valeur est true**, le pilote de communication est sensible à l’état du signal DSR.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="e8f2e-182">Le pilote ignore les octets reçus, sauf si la ligne d’entrée du modem DSR est élevée.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-186">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-187">Utilisation du contrôle de déroulement DTR (Data Terminal Ready) après l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="e8f2e-188">**Activer** (« activer »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e8f2e-189">**Désactiver** (« désactiver »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="e8f2e-190">**Protocole de transfert** (« négociation »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e8f2e-191">**Caractère EOF**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-192">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-194">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-195">Valeur du caractère utilisé pour signaler la fin des données.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="e8f2e-196">Exemple : ^ Z</span><span class="sxs-lookup"><span data-stu-id="e8f2e-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-197">**ErrorReplaceCharacter**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-198">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-200">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-201">Valeur du caractère utilisé pour remplacer les octets reçus avec une erreur de parité.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="e8f2e-202">Exemple : ^ C</span><span class="sxs-lookup"><span data-stu-id="e8f2e-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-203">**ErrorReplacementEnabled**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-204">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-206">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-207">Si la valeur est **true**, les octets reçus avec des erreurs de parité sont remplacés par la valeur **ErrorReplaceCharacter** .</span><span class="sxs-lookup"><span data-stu-id="e8f2e-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="e8f2e-208">Les caractères avec des erreurs de parité sont remplacés uniquement si cette propriété a la **valeur true** et que la parité est activée.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-210">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-212">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-213">Valeur du caractère de contrôle utilisé pour signaler un événement, telle que la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="e8f2e-214">Exemple : ^ e</span><span class="sxs-lookup"><span data-stu-id="e8f2e-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-215">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-218">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| fichier functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-219">Si la **valeur est true**, le port série est occupé.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-220">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-223">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-224">Nom du port série Windows.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="e8f2e-225">Exemple : « COM1 »</span><span class="sxs-lookup"><span data-stu-id="e8f2e-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-226">**Parité**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-229">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| structures de communication win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parity »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-230">Méthode de contrôle de parité à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-230">Method of parity checking to be used.</span></span> <span data-ttu-id="e8f2e-231">La parité est utilisée comme une technique de vérification des erreurs où un bit de parité supplémentaire est inclus avec chaque unité de données.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="e8f2e-232">Le récepteur peut ensuite vérifier la validité des données en comptant les bits qui sont définis.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="e8f2e-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (« aucun »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-234">Vérification de la parité non utilisée.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="e8f2e-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Impair** (« impair »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-236">Définit le bit de parité afin que le nombre de bits défini soit un nombre impair.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="e8f2e-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Même** (« pair »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-238">Définit le bit de parité afin que le nombre de bits défini soit un nombre pair.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="e8f2e-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** (« Mark »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-240">Laisse le bit de parité avec la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="e8f2e-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espace** (« Space »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-242">Laisse le bit de parité défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e8f2e-243">**ParityCheckEnabled**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-244">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-246">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-247">Si la **valeur est true**, le contrôle de parité est activé.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-248">**RTSFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-251">Contrôle de flow de demande d’envoi (RTS).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="e8f2e-252">RTS est utilisé pour signaler que les données sont disponibles pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="e8f2e-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Activer** (« activer »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-254">RTS est conservé pour la session de transfert de données.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="e8f2e-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (« désactiver »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-256">RTS est ignoré après la réception du premier signal RTS.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="e8f2e-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Protocole de transfert** (« négociation »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-258">RTS est désactivé si la mémoire tampon de transmission est pleine de plus de trois quarts et que RTS est activé lorsque la mémoire tampon est inférieure à une moitié pleine.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="e8f2e-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Activer/désactiver** (« bascule »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-260">RTS est activé si des données sont mises en mémoire tampon pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e8f2e-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-262">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-264">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-265">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="e8f2e-266">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-267">**Bits d'arrêt**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-270">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| arrêt")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-271">Nombre de bits d’arrêt à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-271">Number of stop bits to be used.</span></span> <span data-ttu-id="e8f2e-272">Les bits d’arrêt séparent chaque unité de données sur une connexion série asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="e8f2e-273">Ils sont également envoyés en continu quand aucune donnée n’est disponible pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="e8f2e-274">**1** (« 1 »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="e8f2e-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="e8f2e-276">**2** (« 2 »)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e8f2e-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-278">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-280">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-281">Valeur du caractère XOFF pour la transmission et la réception.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="e8f2e-282">XOFF est un contrôle logiciel permettant d’arrêter la transmission de données (alors que RTS et CTS sont des contrôles matériels).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="e8f2e-283">XON reprend la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-287">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-288">Nombre maximal d’octets autorisés dans la mémoire tampon d’entrée avant l’envoi du caractère XOFF.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-290">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-292">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-293">Valeur du caractère XON pour la transmission et la réception.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="e8f2e-294">XON est un contrôle logiciel pour reprendre la transmission de données (alors que RTS et CTS sont des contrôles matériels).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="e8f2e-295">XOFF arrête la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-297">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-299">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-300">Nombre minimal d’octets autorisés dans la mémoire tampon d’entrée avant l’envoi du caractère XON.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="e8f2e-301">Cette propriété fonctionne conjointement avec **XOffXMitThreshold** pour réguler la vitesse à laquelle les données sont transférées.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="e8f2e-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-303">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-305">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-306">Si la **valeur est true**, le contrôle de workflow XON/XOFF est utilisé lors de la réception.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="e8f2e-307">Si la valeur est **true**, la valeur **XOffCharacter** est envoyée lorsque la mémoire tampon d’entrée se trouve dans **XOffXMitThreshold** octets de plein, et la valeur **XOnCharacter** est envoyée lorsque la mémoire tampon d’entrée est vide dans **XOnXMitThreshold** octets.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="e8f2e-308"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-309">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8f2e-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="e8f2e-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="e8f2e-311">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8f2e-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e8f2e-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8f2e-313">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e8f2e-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8f2e-315">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , structures de communication \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")</span><span class="sxs-lookup"><span data-stu-id="e8f2e-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="e8f2e-316">Le **XOnXOffOutFlowControl** spécifie si le contrôle de Flow Xon ou XOFF est utilisé lors de la transmission.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="e8f2e-317">Si la valeur est **true**, la transmission s’arrête lorsque la valeur **XOffCharacter** est reçue et redémarre lorsque la valeur **XOnCharacter** est reçue.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8f2e-318">Notes</span><span class="sxs-lookup"><span data-stu-id="e8f2e-318">Remarks</span></span>

<span data-ttu-id="e8f2e-319">La classe **Win32 \_ SerialPortConfiguration** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="e8f2e-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8f2e-320">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8f2e-320">Requirements</span></span>



| <span data-ttu-id="e8f2e-321">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8f2e-321">Requirement</span></span> | <span data-ttu-id="e8f2e-322">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8f2e-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8f2e-323">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8f2e-323">Minimum supported client</span></span><br/> | <span data-ttu-id="e8f2e-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8f2e-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8f2e-325">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8f2e-325">Minimum supported server</span></span><br/> | <span data-ttu-id="e8f2e-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8f2e-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8f2e-327">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e8f2e-327">Namespace</span></span><br/>                | <span data-ttu-id="e8f2e-328">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e8f2e-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8f2e-329">MOF</span><span class="sxs-lookup"><span data-stu-id="e8f2e-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8f2e-330"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8f2e-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8f2e-331">DLL</span><span class="sxs-lookup"><span data-stu-id="e8f2e-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8f2e-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8f2e-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8f2e-333">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8f2e-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8f2e-334">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="e8f2e-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="e8f2e-335">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="e8f2e-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
