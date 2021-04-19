---
description: Utilisé pour signaler des informations d’État ou d’erreur en réponse à une commande de détection de requête SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Structure de SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106538275"
---
# <a name="sense_data-structure"></a><span data-ttu-id="50f44-103">Structure de données de sens \_</span><span class="sxs-lookup"><span data-stu-id="50f44-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="50f44-104">Utilisé pour signaler des informations d’État ou d’erreur en réponse à une commande de **détection de requête** SCSI.</span><span class="sxs-lookup"><span data-stu-id="50f44-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50f44-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="50f44-106">Membres</span><span class="sxs-lookup"><span data-stu-id="50f44-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="50f44-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="50f44-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-108">Type de rapport.</span><span class="sxs-lookup"><span data-stu-id="50f44-108">The report type.</span></span>



| <span data-ttu-id="50f44-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f44-109">Value</span></span>                                                                           | <span data-ttu-id="50f44-110">Signification</span><span class="sxs-lookup"><span data-stu-id="50f44-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="50f44-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="50f44-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="50f44-112">Erreurs en cours.</span><span class="sxs-lookup"><span data-stu-id="50f44-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="50f44-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="50f44-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="50f44-114">Erreurs différées.</span><span class="sxs-lookup"><span data-stu-id="50f44-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50f44-115">**Valide**</span><span class="sxs-lookup"><span data-stu-id="50f44-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-116">1 si le champ d' **information** est défini dans une norme ; dans le cas contraire, le champ d' **information** est spécifique au fournisseur et n’est pas défini par une norme.</span><span class="sxs-lookup"><span data-stu-id="50f44-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-117">**SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="50f44-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-118">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="50f44-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-119">**SenseKey**</span><span class="sxs-lookup"><span data-stu-id="50f44-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-120">Indique la catégorie de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="50f44-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="50f44-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Aucun sens** (0x0)</span><span class="sxs-lookup"><span data-stu-id="50f44-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Erreur Récupérée** (0x1)</span><span class="sxs-lookup"><span data-stu-id="50f44-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (0X2)</span><span class="sxs-lookup"><span data-stu-id="50f44-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Erreur moyenne** (0x3)</span><span class="sxs-lookup"><span data-stu-id="50f44-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erreur matérielle** (0x4)</span><span class="sxs-lookup"><span data-stu-id="50f44-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Demande non conforme** (0x5)</span><span class="sxs-lookup"><span data-stu-id="50f44-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Attention** sur l’unité (0x6)</span><span class="sxs-lookup"><span data-stu-id="50f44-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Protection des données** (0x7)</span><span class="sxs-lookup"><span data-stu-id="50f44-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Erreur du microprogramme** (0x9)</span><span class="sxs-lookup"><span data-stu-id="50f44-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Commande abandonnée** (0xB)</span><span class="sxs-lookup"><span data-stu-id="50f44-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Égal** à (0xc)</span><span class="sxs-lookup"><span data-stu-id="50f44-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Dépassement de volume** (0xD)</span><span class="sxs-lookup"><span data-stu-id="50f44-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="50f44-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Comparaison** inversée (0xE)</span><span class="sxs-lookup"><span data-stu-id="50f44-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="50f44-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="50f44-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-135">Réservé.</span><span class="sxs-lookup"><span data-stu-id="50f44-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-136">**IncorrectLength**</span><span class="sxs-lookup"><span data-stu-id="50f44-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-137">1 si la longueur de bloc logique demandée ne correspond pas à la longueur de bloc logique des données sur le support.</span><span class="sxs-lookup"><span data-stu-id="50f44-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-138">**EndOfMedia**</span><span class="sxs-lookup"><span data-stu-id="50f44-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-139">1 si un appareil à accès séquentiel a atteint la fin du support ou si une imprimante n’est plus à blanc.</span><span class="sxs-lookup"><span data-stu-id="50f44-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-140">**Marque**</span><span class="sxs-lookup"><span data-stu-id="50f44-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-141">1 si la commande active a atteint un SETMARK ou un.</span><span class="sxs-lookup"><span data-stu-id="50f44-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="50f44-142">Valide uniquement pour les appareils à accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="50f44-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-143">**Informations**</span><span class="sxs-lookup"><span data-stu-id="50f44-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-144">Données spécifiques à un type d’appareil ou à une commande.</span><span class="sxs-lookup"><span data-stu-id="50f44-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-145">**AdditionalSenseLength**</span><span class="sxs-lookup"><span data-stu-id="50f44-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-146">Longueur, en octets, du reste de la structure.</span><span class="sxs-lookup"><span data-stu-id="50f44-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="50f44-147">Longueur totale moins 7.</span><span class="sxs-lookup"><span data-stu-id="50f44-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-148">**CommandSpecificInformation**</span><span class="sxs-lookup"><span data-stu-id="50f44-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-149">Données spécifiques à la commande.</span><span class="sxs-lookup"><span data-stu-id="50f44-149">Command-specific data.</span></span> <span data-ttu-id="50f44-150">Les valeurs sont définies dans la norme de commande appropriée.</span><span class="sxs-lookup"><span data-stu-id="50f44-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-151">**AdditionalSenseCode**</span><span class="sxs-lookup"><span data-stu-id="50f44-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-152">Code spécifique à l’appareil qui décrit l’erreur signalée dans le champ **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="50f44-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-153">**AdditionalSenseCodeQualifier**</span><span class="sxs-lookup"><span data-stu-id="50f44-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-154">Peut contenir des détails supplémentaires sur le champ **AdditionalSenseCode** .</span><span class="sxs-lookup"><span data-stu-id="50f44-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-155">**FieldReplaceableUnitCode**</span><span class="sxs-lookup"><span data-stu-id="50f44-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-156">Informations spécifiques au fournisseur sur le composant associé à ces données de sens.</span><span class="sxs-lookup"><span data-stu-id="50f44-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="50f44-157">**SenseKeySpecific**</span><span class="sxs-lookup"><span data-stu-id="50f44-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="50f44-158">Le contenu et le format des informations spécifiques à la clé de détection sont déterminés par la valeur du champ **SenseKey** .</span><span class="sxs-lookup"><span data-stu-id="50f44-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50f44-159">Notes</span><span class="sxs-lookup"><span data-stu-id="50f44-159">Remarks</span></span>

<span data-ttu-id="50f44-160">Pour plus d’informations sur le format de données de sens, consultez [commande SCSI Request sens](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="50f44-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="50f44-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f44-161">Requirements</span></span>



| <span data-ttu-id="50f44-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50f44-162">Requirement</span></span> | <span data-ttu-id="50f44-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f44-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="50f44-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f44-164">Minimum supported client</span></span><br/> | <span data-ttu-id="50f44-165">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50f44-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50f44-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f44-166">Minimum supported server</span></span><br/> | <span data-ttu-id="50f44-167">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50f44-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50f44-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="50f44-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f44-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="50f44-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f44-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f44-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f44-171">Transfert de cible iSCSI</span><span class="sxs-lookup"><span data-stu-id="50f44-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="50f44-172">\_transfert \_ direct via \_ le SCSI</span><span class="sxs-lookup"><span data-stu-id="50f44-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




