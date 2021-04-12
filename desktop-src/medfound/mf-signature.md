---
description: Contient une signature de liste de révocation globale (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Structure MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210365"
---
# <a name="mf_signature-structure"></a>\_Structure de signature MF

Contient une signature de liste de révocation globale (GRL).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSignVer**
</dt> <dd>

Numéro de version de la signature.

</dd> <dt>

**cbSign**
</dt> <dd>

Taille de la signature en octets.

</dd> <dt>

**rgSign**
</dt> <dd>

Tableau d’octets de taille **cbSign** qui contient la signature. La taille réelle du tableau est supérieure à la taille spécifiée dans la déclaration de la structure.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure n’est pas déclarée dans un en-tête SDK. Pour utiliser cette structure, ajoutez la déclaration indiquée ici à votre code source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Révocation de certificat OPM](opm-certificate-revocation.md)
</dt> <dt>

[Structures OPM](opm-structures.md)
</dt> </dl>

 

 




