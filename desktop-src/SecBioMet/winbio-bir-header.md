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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011162"
---
# <a name="winbio_bir_header-structure"></a>\_Structure d' \_ en-tête Bir WINBIO

La structure d' **\_ \_ en-tête WINBIO Bir** contient l’en-tête d’un enregistrement d’informations biométriques (Bir).

## <a name="syntax"></a>Syntaxe


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



## <a name="members"></a>Membres

<dl> <dt>

**ValidFields**
</dt> <dd>

Masque de masque qui spécifie les champs de cette structure qui sont valides. Pour plus d’informations, [**consultez \_ \_ constantes de champ WINBIO Bir**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Constante **de \_ \_ version WINBIO Bir** qui spécifie la version d’en-tête. Les numéros de version sont des valeurs 8 bits où les quatre bits supérieurs spécifient le nombre majeur et les quatre bits de poids faible spécifient le numéro de version mineure. Actuellement, il doit s' \_ agir \_ de la version d’en-tête CBEFF WINBIO \_ (0x11).

</dd> <dt>

**PatronHeaderVersion**
</dt> <dd>

Constante **de \_ \_ version WINBIO Bir** qui spécifie la version d’en-tête. Les numéros de version sont des valeurs 8 bits où les quatre bits supérieurs spécifient le nombre majeur et les quatre bits de poids faible spécifient le numéro de version mineure. Actuellement, il doit s' \_ agir \_ de WINBIO version d’en-tête d’un patron \_ (0x11).

</dd> <dt>

**DataFlags**
</dt> <dd>

Valeur qui spécifie le format des données d’en-tête. Il peut s’agir d’une opération **de bits or** des indicateurs de niveau de sécurité et de traitement suivants. Pour plus d’informations, [**consultez \_ \_ \_ constantes d’indicateurs de données WINBIO Bir**](winbio-bir-data-flags-constants.md).



| Valeur                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Confidentialité des indicateurs de données**</dt> <dt>((UCHAR) 0x02)</dt> </dl>                                       | Les données sont chiffrées.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Intégrité des indicateurs de données**</dt> <dt>((UCHAR) 0x01)</dt> </dl>                                 | Les données sont signées numériquement ou protégées par un code d’authentification de message (MAC).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ signé**</dt> <dt>((UCHAR) 0x04)</dt> </dl>                                          | Si cet indicateur et l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** sont définis, les données sont signées. Si cet indicateur n’est pas défini, mais que l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** est défini, un Mac est calculé sur les données.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ brut**</dt> <dt>((UCHAR) 0x20)</dt> </dl>                                                   | Les données sont au format avec lequel elles ont été capturées.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ intermédiaire**</dt> <dt>((UCHAR) 0x40)</dt> </dl>                        | Les données ne sont pas brutes, mais elles n’ont pas été complètement traitées.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Indicateur de données \_ \_ traité**</dt> <dt>((UCHAR) 0x80)</dt> </dl>                                 | Les données ont été traitées.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Masque d’option de l’indicateur de données \_ \_ \_ \_ présent**</dt> <dt>((UCHAR) 0x08)</dt> </dl> | Cette valeur est toujours 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Type**
</dt> <dd>

\_ \_ Valeur de type biométrique WINBIO qui spécifie le type de données biométriques référencées dans l’enregistrement d’informations biométriques. Actuellement, seules les **\_ \_ empreintes digitales de type WINBIO** sont prises en charge. Pour plus d’informations, [**consultez \_ \_ constantes de type de biométrie WINBIO**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtype**
</dt> <dd>

Valeur de sous- **\_ \_ type biométrique WINBIO** qui spécifie le sous-facteur associé aux données biométriques. Pour plus d’informations, consultez la section Notes et [**\_ \_ constantes de sous-types biométriques WINBIO**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Objectif**
</dt> <dd>

Masque **d' \_ \_ objectif WINBIO Bir** qui spécifie l’utilisation prévue des données. Il peut s’agir d’une **opération or au niveau du** bit des valeurs suivantes. Pour plus d’informations, consultez [**WINBIO \_ Bir \_ Purpose, constantes**](winbio-bir-purpose-constants.md).

-   vérification de l' \_ objectif WINBIO \_
-   identification de l’objectif de WINBIO \_ \_
-   inscription à l’objectif de WINBIO \_ \_
-   \_inscription de l’objectif WINBIO \_ pour la \_ \_ vérification
-   \_inscription de l’objectif WINBIO \_ pour l' \_ \_ identification
-   \_ \_ audit d’objectif WINBIO

</dd> <dt>

**DataQuality**
</dt> <dd>

Valeur qui spécifie la qualité relative des données biométriques dans l’enregistrement des informations biométriques (BIR). Il peut s’agir d’un entier compris entre 0 et 100 ou de l’une des valeurs suivantes. Pour plus d’informations, [**consultez \_ \_ constantes de qualité WINBIO Bir**](winbio-bir-quality-constants.md).



| Valeur                                                                                                                                                                                                                                                                                                        | Signification                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Qualité des données \_ \_ non \_ définie**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt> </dl>                   | Les mesures de qualité sont prises en charge par le créateur BIR, mais aucune valeur n’est définie dans BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Qualité des données \_ \_ non \_ prise en charge**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt> </dl> | Les mesures de qualité ne sont pas prises en charge par le créateur BIR.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

La date et l’heure, en temps universel coordonné (heure de Greenwich), que le BIR a été créé.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

Période pendant laquelle le BIR est valide.

<dl> <dt>

**BeginDate**
</dt> <dd>

Date et heure, en temps universel coordonné, de début de la période de validité.

</dd> <dt>

**EndDate**
</dt> <dd>

Date et heure, en temps universel coordonné, auxquelles le BIR cesse d’être valide.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Structure [**de \_ \_ format WINBIO inscrit**](winbio-registered-format.md) qui spécifie le format de données du bloc de données standard dans la structure [**WINBIO \_ Bir**](winbio-bir.md) . Les membres de **\_ \_ format inscrits WINBIO** ne peuvent pas être nuls. Vous pouvez utiliser les constantes suivantes pour simplifier la vérification des erreurs.



| Valeur                                                                                                                                                                                                                                                                                      | Signification                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ AUCUN \_ propriétaire de format \_ \_ disponible**</dt> <dt>((UShort) 0)</dt> </dl> | Aucune valeur propriétaire n’a été spécifiée pour l’Association de l’IBIA de l’industrie biométrique internationale.<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ AUCUN \_ type de format \_ \_ disponible**</dt> <dt>((UShort) 0)</dt> </dl>    | Aucun type de format n’a été spécifié.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Structure [**de \_ \_ format enregistrée par WINBIO**](winbio-registered-format.md) qui spécifie l’ID de produit du composant qui a généré le bloc de données standard dans Bir. Les membres du **\_ \_ format enregistré WINBIO** peuvent être nuls.

</dd> </dl>

## <a name="remarks"></a>Notes

Le paramètre *SubType* spécifie le sous-facteur associé aux données biométriques. actuellement, le Windows Biometric Framework (WBF) prend uniquement en charge la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de sous-type :

-   WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle
-   WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger
-   \_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts
-   WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces

> [!IMPORTANT]
>
> N’essayez pas de valider la valeur fournie pour la valeur du paramètre *SubType* . le Service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation. Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.

 

Si l’un des bits suivants est déclaré, la structure **d' \_ \_ en-tête Bir WINBIO** n’est pas correctement formée.


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> <dt>

[**\_Constantes de sous-type biométrique WINBIO \_**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_ \_ Constantes d’indicateurs de données WINBIO Bir \_**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**\_ \_ Constantes de champ WINBIO Bir**](winbio-bir-field-constants.md)
</dt> <dt>

[**\_ \_ Constantes WINBIO Bir Purpose**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**\_ \_ Constantes de qualité WINBIO Bir**](winbio-bir-quality-constants.md)
</dt> <dt>

[**WINBIO \_ , \_ constantes de version Bir**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





