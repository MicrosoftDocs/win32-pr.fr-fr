---
title: Structure WINBIO_IDENTITY ( \_ types WINBIO. h)
description: Contient une valeur d’identification associée à un modèle biométrique.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API de Windows Biometric Framework de structure de WINBIO_IDENTITY
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103996"
---
# <a name="winbio_identity-structure"></a>\_Structure d’identité WINBIO

La structure d' **\_ identité WINBIO** contient une valeur d’identification associée à un modèle biométrique.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Spécifie le format des informations d’identité contenues dans cette structure. Il peut s’agir de l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                         | Signification                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_type d’ID WINBIO \_ \_ null**</dt> </dl>             | Le modèle n’a pas d’ID associé.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ caractère générique de type d’ID WINBIO \_**</dt> </dl> | La structure correspond à toutes les identités de modèle.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_GUID du \_ type d’ID WINBIO \_**</dt> </dl>             | La structure contient un GUID associé au modèle.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**\_ID \_ sid type \_ WINBIO**</dt> </dl>                | La structure contient le SID de compte associé au modèle.<br/> |



 

</dd> <dt>

**Valeur**
</dt> <dd>

Union qui peut contenir l’une des valeurs suivantes :

<dl> <dt>

**Null**
</dt> <dd>

Contient 1 si le membre de **type** est **WINBIO \_ ID de \_ type \_ null**.

</dd> <dt>

**Caractère générique**
</dt> <dd>

Contient 1 si le membre de **type** est un **type d' \_ ID WINBIO \_ \_ générique**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contient une valeur de GUID 128 bits qui identifie le modèle si le membre de **type** est **WINBIO \_ ID de \_ type \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Structure qui contient un SID de compte si le membre de **type** est **WINBIO \_ ID \_ type \_ sid**.

<dl> <dt>

**Taille**
</dt> <dd>

Nombre de caractères dans le SID.

</dd> <dt>

**Données**
</dt> <dd>

Tableau de caractères non signés qui contiennent le SID. La taille maximale actuelle du tableau est de 68 caractères.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée dans les fonctions suivantes :

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’application cliente](client-application-structures.md)
</dt> </dl>

 

 





