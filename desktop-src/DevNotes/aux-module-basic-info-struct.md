---
description: Contient des informations sur le module de base.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Structure de AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: e1a25af780016c226acf46348573def8505669e16f1f645fcfce1c9324bb086d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956148"
---
# <a name="aux_module_basic_info-structure"></a>\_Structure des \_ informations de base des modules aux \_

Contient des informations sur le module de base.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**ImageBase**
</dt> <dd>

Adresse de base du module dans l’espace d’adressage du noyau.

</dd> </dl>

## <a name="remarks"></a>Remarques

La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque d’API auxiliaire version 1,0 ou ultérieure<br/>                          |
| En-tête<br/>          | <dl> <dt>Aux \_ klib. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




