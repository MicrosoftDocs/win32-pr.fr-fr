---
title: LSKeyPack, structure
description: Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la structure LSKeyPack
- Services Bureau à distance pointeur de structure LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8b2c7c8b6c42464e273008f9de2730b41ea64981e44583eb48f4125da3ba9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989088"
---
# <a name="lskeypack-structure"></a>LSKeyPack, structure

Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Version du jeu de clés.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Type de jeu de clés.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Nom de la société qui a émis le jeu de clés.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

ID du jeu de clés.

</dd> <dt>

**szProductName**
</dt> <dd>

Nom du produit auquel appartient ce module de clé.

</dd> <dt>

**szProductId**
</dt> <dd>

ID du produit auquel ce module de clé appartient.

</dd> <dt>

**szProductDesc**
</dt> <dd>

Description du produit auquel ce module de clé appartient.

</dd> <dt>

**wMajorVersion**
</dt> <dd>

Version principale du produit auquel appartient ce module de clé.

</dd> <dt>

**wMinorVersion**
</dt> <dd>

Version mineure du produit auquel appartient ce module de clé.

</dd> <dt>

**dwPlatformType**
</dt> <dd>

Type de plateforme.

</dd> <dt>

**ucLicenseType**
</dt> <dd>

Type de licences dans le jeu de clés.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

ID de langue.

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

Canal d’achat.

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

Numéro de série de la première licence.

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

Nombre total de licences dans le jeu de clés.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Père.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID du jeu de clés.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

État du jeu de clés.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Date d’activation du jeu de clés.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Date d’expiration du jeu de clés.

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

Nombre de licences.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 





