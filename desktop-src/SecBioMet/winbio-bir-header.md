---
title: Structure WINBIO_BIR_HEADER ( \_ types WINBIO. h)
description: Contient l’en-tête d’un enregistrement d’informations biométriques (BIR).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BIR_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103699"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="ffc2f-104">\_Structure d' \_ en-tête Bir WINBIO</span><span class="sxs-lookup"><span data-stu-id="ffc2f-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="ffc2f-105">La structure d' **\_ \_ en-tête WINBIO Bir** contient l’en-tête d’un enregistrement d’informations biométriques (Bir).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc2f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffc2f-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="ffc2f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ffc2f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ffc2f-108">**ValidFields**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-109">Masque de masque qui spécifie les champs de cette structure qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="ffc2f-110">Pour plus d’informations, [**consultez \_ \_ constantes de champ WINBIO Bir**](winbio-bir-field-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-112">Constante **de \_ \_ version WINBIO Bir** qui spécifie la version d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="ffc2f-113">Les numéros de version sont des valeurs 8 bits où les quatre bits supérieurs spécifient le nombre majeur et les quatre bits de poids faible spécifient le numéro de version mineure.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="ffc2f-114">Actuellement, il doit s' \_ agir \_ de la version d’en-tête CBEFF WINBIO \_ (0x11).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-115">**PatronHeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-116">Constante **de \_ \_ version WINBIO Bir** qui spécifie la version d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="ffc2f-117">Les numéros de version sont des valeurs 8 bits où les quatre bits supérieurs spécifient le nombre majeur et les quatre bits de poids faible spécifient le numéro de version mineure.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="ffc2f-118">Actuellement, il doit s' \_ agir \_ de WINBIO version d’en-tête d’un patron \_ (0x11).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-119">**DataFlags**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-120">Valeur qui spécifie le format des données d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="ffc2f-121">Il peut s’agir d’une opération **de bits or** des indicateurs de niveau de sécurité et de traitement suivants.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="ffc2f-122">Pour plus d’informations, [**consultez \_ \_ \_ constantes d’indicateurs de données WINBIO Bir**](winbio-bir-data-flags-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="ffc2f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc2f-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ffc2f-124">Signification</span><span class="sxs-lookup"><span data-stu-id="ffc2f-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="ffc2f-125"><dt>**WINBIO \_ \_ \_ Confidentialité des indicateurs de données**</dt> <dt>((UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="ffc2f-126">Les données sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="ffc2f-127"><dt>**WINBIO \_ \_ \_ Intégrité des indicateurs de données**</dt> <dt>((UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="ffc2f-128">Les données sont signées numériquement ou protégées par un code d’authentification de message (MAC).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="ffc2f-129"><dt>**WINBIO \_ Indicateur de données \_ \_ signé**</dt> <dt>((UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="ffc2f-130">Si cet indicateur et l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** sont définis, les données sont signées.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="ffc2f-131">Si cet indicateur n’est pas défini, mais que l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** est défini, un Mac est calculé sur les données.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="ffc2f-132"><dt>**WINBIO \_ Indicateur de données \_ \_ brut**</dt> <dt>((UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="ffc2f-133">Les données sont au format avec lequel elles ont été capturées.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="ffc2f-134"><dt>**WINBIO \_ Indicateur de données \_ \_ intermédiaire**</dt> <dt>((UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="ffc2f-135">Les données ne sont pas brutes, mais elles n’ont pas été complètement traitées.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="ffc2f-136"><dt>**WINBIO \_ Indicateur de données \_ \_ traité**</dt> <dt>((UCHAR) 0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="ffc2f-137">Les données ont été traitées.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="ffc2f-138"><dt>**WINBIO \_ Masque d’option de l’indicateur de données \_ \_ \_ \_ présent**</dt> <dt>((UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="ffc2f-139">Cette valeur est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="ffc2f-140">**Type**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-141">\_ \_ Valeur de type biométrique WINBIO qui spécifie le type de données biométriques référencées dans l’enregistrement d’informations biométriques.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="ffc2f-142">Actuellement, seules les **\_ \_ empreintes digitales de type WINBIO** sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="ffc2f-143">Pour plus d’informations, [**consultez \_ \_ constantes de type de biométrie WINBIO**](winbio-biometric-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-144">**Sous-type**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-145">Valeur de sous- **\_ \_ type biométrique WINBIO** qui spécifie le sous-facteur associé aux données biométriques.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="ffc2f-146">Pour plus d’informations, consultez la section Notes et [**\_ \_ constantes de sous-types biométriques WINBIO**](winbio-biometric-subtype-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-147">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-148">Masque **d' \_ \_ objectif WINBIO Bir** qui spécifie l’utilisation prévue des données.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="ffc2f-149">Il peut s’agir d’une **opération or au niveau du** bit des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="ffc2f-150">Pour plus d’informations, consultez [**WINBIO \_ Bir \_ Purpose, constantes**](winbio-bir-purpose-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="ffc2f-151">vérification de l' \_ objectif WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="ffc2f-152">identification de l’objectif de WINBIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="ffc2f-153">inscription à l’objectif de WINBIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="ffc2f-154">\_inscription de l’objectif WINBIO \_ pour la \_ \_ vérification</span><span class="sxs-lookup"><span data-stu-id="ffc2f-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="ffc2f-155">\_inscription de l’objectif WINBIO \_ pour l' \_ \_ identification</span><span class="sxs-lookup"><span data-stu-id="ffc2f-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="ffc2f-156">\_ \_ audit d’objectif WINBIO</span><span class="sxs-lookup"><span data-stu-id="ffc2f-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-157">**DataQuality**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-158">Valeur qui spécifie la qualité relative des données biométriques dans l’enregistrement des informations biométriques (BIR).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="ffc2f-159">Il peut s’agir d’un entier compris entre 0 et 100 ou de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="ffc2f-160">Pour plus d’informations, [**consultez \_ \_ constantes de qualité WINBIO Bir**](winbio-bir-quality-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ffc2f-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="ffc2f-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc2f-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="ffc2f-162">Signification</span><span class="sxs-lookup"><span data-stu-id="ffc2f-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="ffc2f-163"><dt>**WINBIO \_ Qualité des données \_ \_ non \_ définie**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="ffc2f-164">Les mesures de qualité sont prises en charge par le créateur BIR, mais aucune valeur n’est définie dans BIR.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="ffc2f-165"><dt>**WINBIO \_ Qualité des données \_ \_ non \_ prise en charge**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="ffc2f-166">Les mesures de qualité ne sont pas prises en charge par le créateur BIR.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="ffc2f-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-168">La date et l’heure, en temps universel coordonné (heure de Greenwich), que le BIR a été créé.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-170">Période pendant laquelle le BIR est valide.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="ffc2f-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-172">Date et heure, en temps universel coordonné, de début de la période de validité.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="ffc2f-173">**EndDate**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-174">Date et heure, en temps universel coordonné, auxquelles le BIR cesse d’être valide.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ffc2f-175">**BiometricDataFormat**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-176">Structure [**de \_ \_ format WINBIO inscrit**](winbio-registered-format.md) qui spécifie le format de données du bloc de données standard dans la structure [**WINBIO \_ Bir**](winbio-bir.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc2f-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="ffc2f-177">Les membres de **\_ \_ format inscrits WINBIO** ne peuvent pas être nuls.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="ffc2f-178">Vous pouvez utiliser les constantes suivantes pour simplifier la vérification des erreurs.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="ffc2f-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc2f-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="ffc2f-180">Signification</span><span class="sxs-lookup"><span data-stu-id="ffc2f-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="ffc2f-181"><dt>**WINBIO \_ AUCUN \_ propriétaire de format \_ \_ disponible**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="ffc2f-182">Aucune valeur propriétaire n’a été spécifiée pour l’Association de l’IBIA de l’industrie biométrique internationale.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="ffc2f-183"><dt>**WINBIO \_ AUCUN \_ type de format \_ \_ disponible**</dt> <dt>((UShort) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="ffc2f-184">Aucun type de format n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="ffc2f-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="ffc2f-186">Structure [**de \_ \_ format enregistrée par WINBIO**](winbio-registered-format.md) qui spécifie l’ID de produit du composant qui a généré le bloc de données standard dans Bir.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="ffc2f-187">Les membres du **\_ \_ format enregistré WINBIO** peuvent être nuls.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffc2f-188">Notes</span><span class="sxs-lookup"><span data-stu-id="ffc2f-188">Remarks</span></span>

<span data-ttu-id="ffc2f-189">Le paramètre *SubType* spécifie le sous-facteur associé aux données biométriques.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="ffc2f-190">Actuellement, le Windows Biometric Framework (WBF) prend uniquement en charge la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de sous-type :</span><span class="sxs-lookup"><span data-stu-id="ffc2f-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="ffc2f-191">WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="ffc2f-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="ffc2f-192">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="ffc2f-193">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="ffc2f-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-194">WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle</span><span class="sxs-lookup"><span data-stu-id="ffc2f-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-195">WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-196">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger</span><span class="sxs-lookup"><span data-stu-id="ffc2f-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-197">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="ffc2f-198">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="ffc2f-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-199">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger</span><span class="sxs-lookup"><span data-stu-id="ffc2f-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-200">\_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="ffc2f-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-201">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt</span><span class="sxs-lookup"><span data-stu-id="ffc2f-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="ffc2f-202">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="ffc2f-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="ffc2f-203">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="ffc2f-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="ffc2f-204">WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces</span><span class="sxs-lookup"><span data-stu-id="ffc2f-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ffc2f-205">N’essayez pas de valider la valeur fournie pour la valeur du paramètre *SubType* .</span><span class="sxs-lookup"><span data-stu-id="ffc2f-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="ffc2f-206">Le service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="ffc2f-207">Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="ffc2f-208">Si l’un des bits suivants est déclaré, la structure **d' \_ \_ en-tête Bir WINBIO** n’est pas correctement formée.</span><span class="sxs-lookup"><span data-stu-id="ffc2f-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="ffc2f-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffc2f-209">Requirements</span></span>



| <span data-ttu-id="ffc2f-210">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffc2f-210">Requirement</span></span> | <span data-ttu-id="ffc2f-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc2f-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc2f-212">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffc2f-212">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc2f-213">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffc2f-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ffc2f-214">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffc2f-214">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc2f-215">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffc2f-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ffc2f-216">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffc2f-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffc2f-217"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffc2f-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc2f-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffc2f-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc2f-219">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="ffc2f-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-220">**\_Constantes de sous-type biométrique WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-221">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-222">**\_ \_ Constantes d’indicateurs de données WINBIO Bir \_**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-223">**\_ \_ Constantes de champ WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-224">**\_ \_ Constantes WINBIO Bir Purpose**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-225">**\_ \_ Constantes de qualité WINBIO Bir**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="ffc2f-226">**WINBIO \_ , \_ constantes de version Bir**</span><span class="sxs-lookup"><span data-stu-id="ffc2f-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





