---
title: Énumération WMDM_TAG_DATATYPE
description: Le \_ \_ type d’énumération DataType de la balise WMDM définit un type de données.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545362"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_Énumération de type de données de balise WMDM \_

Le type d’énumération DataType de la **\_ \_ balise WMDM** définit un type de données.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**TYPE de WMDM \_ \_ DWORD**
</dt> <dd>

Spécifie une valeur **DWORD** sur 4 octets.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_chaîne de type WMDM \_**
</dt> <dd>

Spécifie une chaîne Unicode terminée par le caractère null (2 octets par caractère).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**TYPE de WMDM \_ \_ binaire**
</dt> <dd>

Spécifie un tableau d’octets.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_type WMDM \_ bool**
</dt> <dd>

Spécifie une valeur booléenne sur 4 octets.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**TYPE de WMDM \_ \_ QWord**
</dt> <dd>

Spécifie une valeur **QWord** sur 8 octets.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ type \_ Word**
</dt> <dd>

Spécifie une valeur de **mot** de 2 octets.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID de type WMDM \_**
</dt> <dd>

Spécifie un GUID 128 bits (16 octets).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_date du type de WMDM \_**
</dt> <dd>

Spécifie une date.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





