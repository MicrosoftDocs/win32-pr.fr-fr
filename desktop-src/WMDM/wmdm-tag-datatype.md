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
# <a name="wmdm_tag_datatype-enumeration"></a><span data-ttu-id="1c54b-104">\_Énumération de type de données de balise WMDM \_</span><span class="sxs-lookup"><span data-stu-id="1c54b-104">WMDM\_TAG\_DATATYPE enumeration</span></span>

<span data-ttu-id="1c54b-105">Le type d’énumération DataType de la **\_ \_ balise WMDM** définit un type de données.</span><span class="sxs-lookup"><span data-stu-id="1c54b-105">The **WMDM\_TAG\_DATATYPE** enumeration type defines a data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c54b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c54b-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="1c54b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1c54b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1c54b-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**TYPE de WMDM \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1c54b-108"><span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-109">Spécifie une valeur **DWORD** sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="1c54b-109">Specifies a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_chaîne de type WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1c54b-110"><span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**WMDM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-111">Spécifie une chaîne Unicode terminée par le caractère null (2 octets par caractère).</span><span class="sxs-lookup"><span data-stu-id="1c54b-111">Specifies a null-terminated Unicode string (2 bytes per character).</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**TYPE de WMDM \_ \_ binaire**</span><span class="sxs-lookup"><span data-stu-id="1c54b-112"><span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**WMDM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-113">Spécifie un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="1c54b-113">Specifies an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_type WMDM \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1c54b-114"><span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**WMDM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-115">Spécifie une valeur booléenne sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="1c54b-115">Specifies a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**TYPE de WMDM \_ \_ QWord**</span><span class="sxs-lookup"><span data-stu-id="1c54b-116"><span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-117">Spécifie une valeur **QWord** sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="1c54b-117">Specifies an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ type \_ Word**</span><span class="sxs-lookup"><span data-stu-id="1c54b-118"><span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-119">Spécifie une valeur de **mot** de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="1c54b-119">Specifies a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID de type WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1c54b-120"><span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**WMDM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-121">Spécifie un GUID 128 bits (16 octets).</span><span class="sxs-lookup"><span data-stu-id="1c54b-121">Specifies a 128-bit (16-byte) GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1c54b-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**\_date du type de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="1c54b-122"><span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM\_TYPE\_DATE**</span></span>
</dt> <dd>

<span data-ttu-id="1c54b-123">Spécifie une date.</span><span class="sxs-lookup"><span data-stu-id="1c54b-123">Specifies a date.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c54b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c54b-124">Requirements</span></span>



| <span data-ttu-id="1c54b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c54b-125">Requirement</span></span> | <span data-ttu-id="1c54b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c54b-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c54b-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c54b-127">Header</span></span><br/> | <dl> <span data-ttu-id="1c54b-128"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c54b-128"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c54b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c54b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c54b-130">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="1c54b-130">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





