---
description: Spécifie les attributs d’une signature Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Structure SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cce522403e4b4e416bd3d1ecb9d6c4a551ef3bb67407f853f586bd061f3d8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898946"
---
# <a name="signer_attr_authcode-structure"></a>\_Structure facteurs attr de signataire \_

La structure **\_ \_ facteurs attr du signataire** spécifie des attributs pour une signature [*Authenticode*](../secgloss/a-gly.md) .

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**fCommercial**
</dt> <dd>

**True** pour signer le sujet en tant que serveur de publication commercial ; Sinon, **false**.

</dd> <dt>

**fIndividual**
</dt> <dd>

**True** pour signer le sujet en tant qu’éditeur individuel ; Sinon, **false**.

</dd> <dt>

**pwszName**
</dt> <dd>

Nom complet du fichier lors du téléchargement.

</dd> <dt>

**pwszInfo**
</dt> <dd>

Nom complet de l’URL du fichier lors du téléchargement.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**informations de \_ signature du signataire \_**](signer-signature-info.md)
</dt> </dl>

 

 
