---
description: Contient des informations sur les modules étendus.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Structure de AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540636"
---
# <a name="aux_module_extended_info-structure"></a>\_Structure des \_ informations étendues du module aux \_

Contient des informations sur les modules étendus.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**BasicInfo**
</dt> <dd>

Structure [**des \_ \_ \_ informations de base des modules**](aux-module-basic-info-struct.md) aux.

</dd> <dt>

**ImageSize**
</dt> <dd>

Taille, en octets, du module chargé.

</dd> <dt>

**FileNameOffset**
</dt> <dd>

Offset du nom de fichier dans la mémoire tampon **FullPathName** .

</dd> <dt>

**FullPathName**
</dt> <dd>

Chemin d’accès complet du module.

</dd> </dl>

## <a name="remarks"></a>Notes

La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure<br/>                          |
| En-tête<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**\_informations de \_ base du module aux \_**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




