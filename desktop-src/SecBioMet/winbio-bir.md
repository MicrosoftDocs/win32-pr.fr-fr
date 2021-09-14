---
title: Structure WINBIO_BIR ( \_ types WINBIO. h)
description: Représente un enregistrement d’informations biométriques (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BIR
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011157"
---
# <a name="winbio_bir-structure"></a>WINBIO \_ Bir, structure

La structure **WINBIO \_ Bir** représente un enregistrement d’informations biométriques (Bir). L’enregistrement d’informations contient des blocs d’en-tête, de données et de signature.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Structure [**de \_ \_ données WINBIO Bir**](winbio-bir-data.md) qui contient la taille, en octets et le décalage de l’en-tête Bir. L’en-tête contient des informations qui décrivent le contenu de l’enregistrement d’informations.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

structure [**de \_ \_ données WINBIO BIR**](winbio-bir-data.md) qui contient la taille, en octets, et l’offset des informations biométriques traitées ou non traitées créées par le Windows Biometric Framework (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Structure [**de \_ \_ données WINBIO Bir**](winbio-bir-data.md) qui contient la taille, en octets, et le décalage des informations biométriques traitées ou non traitées fournies par les capteurs et logiciels du fournisseur.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Structure de [**\_ \_ données WINBIO Bir**](winbio-bir-data.md) facultative qui contient la taille, en octets, et le décalage du code d’authentification de message de signature numérique (Mac) qui peut être utilisé pour vérifier l’intégrité du Bir. Si elle est présente, la signature ou le MAC doit couvrir les blocs d’en-tête et de données.

</dd> </dl>

## <a name="remarks"></a>Notes

L’utilisation de décalages plutôt que de pointeurs permet de faciliter la sérialisation du BIR et de la traduction moins compliquée entre les environnements 32 et 64 bits ou entre l’utilisateur et le mode noyau.

le BIR est compatible avec l’infrastructure de Format de Exchange biométrique commune (CBEFF) définie par le NIST 6529-A.

Si cette structure contient une valeur *StandardDataBlock* , le paramètre de *type* de l’en-tête spécifié par le paramètre *HeaderBlock* doit être défini sur le **\_ \_ \_ \_ type de format ANSI 381 WINBIO**. il s’agit du seul format de données standard pris en charge par la version actuelle du Windows Biometric Framework.

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

[**WINBIO \_ Bir \_ données**](winbio-bir-data.md)
</dt> <dt>

[**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md)
</dt> </dl>

 

 





