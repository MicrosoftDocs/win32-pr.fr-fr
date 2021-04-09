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
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953146"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**informations de \_ signature du signataire \_**](signer-signature-info.md)
</dt> </dl>

 

 
