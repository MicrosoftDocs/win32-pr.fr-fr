---
title: LSLicense, structure
description: Contient des informations sur une licence de Services Bureau à distance spécifique.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la structure LSLicense
- Services Bureau à distance pointeur de structure LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465123"
---
# <a name="lslicense-structure"></a>LSLicense, structure

Contient des informations sur une licence de Services Bureau à distance spécifique.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Version de la licence.

</dd> <dt>

**dwLicenseId**
</dt> <dd>

ID de la licence.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID du [**LSKeyPack**](lskeypack.md) qui contient la licence.

</dd> <dt>

**szHWID**
</dt> <dd>

ID matériel du client Connexion Bureau à distance (RDC) qui a émis la licence.

</dd> <dt>

**szMachineName**
</dt> <dd>

Nom du client Connexion Bureau à distance (RDC) qui a émis la licence.

</dd> <dt>

**szUserName**
</dt> <dd>

Nom de l’utilisateur qui a émis la licence.

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

Numéro de série de la licence.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Date à laquelle la licence a été émise.

</dd> <dt>

**ftExpireDate**
</dt> <dd>

Date d’expiration de la licence.

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

État actuel de la licence.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 





