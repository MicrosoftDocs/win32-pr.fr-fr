---
title: Énumération DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: L' \_ \_ énumération de type de données de l’attribut DRM définit les types de données utilisés pour les propriétés et les attributs DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Format Windows Media d’énumération DRM_ATTR_DATATYPE
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541309"
---
# <a name="drm_attr_datatype-enumeration"></a><span data-ttu-id="a6358-105">\_Énumération de type de données de l’attr DRM \_</span><span class="sxs-lookup"><span data-stu-id="a6358-105">DRM\_ATTR\_DATATYPE enumeration</span></span>

<span data-ttu-id="a6358-106">L’énumération de **\_ \_ type** de données de l’attribut DRM définit les types de données utilisés pour les propriétés et les attributs DRM.</span><span class="sxs-lookup"><span data-stu-id="a6358-106">The **DRM\_ATTR\_DATATYPE** enumeration defines the data types used for DRM attributes and properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6358-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6358-107">Syntax</span></span>


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="a6358-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a6358-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a6358-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**\_type DRM \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6358-109"><span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**DRM\_TYPE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-110">La propriété est une valeur **DWORD** sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="a6358-110">The property is a 4-byte **DWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_chaîne de type DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a6358-111"><span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**DRM\_TYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-112">La propriété est une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="a6358-112">The property is a null-terminated Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_binaire de type DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a6358-113"><span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**DRM\_TYPE\_BINARY**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-114">La propriété est un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="a6358-114">The property is an array of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_type DRM \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a6358-115"><span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**DRM\_TYPE\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-116">La propriété est une valeur booléenne sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="a6358-116">The property is a 4-byte Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**\_type DRM \_ QWord**</span><span class="sxs-lookup"><span data-stu-id="a6358-117"><span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM\_TYPE\_QWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-118">La propriété est une valeur **QWord** sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="a6358-118">The property is an 8-byte **QWORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_mot de type DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a6358-119"><span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM\_TYPE\_WORD**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-120">La propriété est une valeur de **mot** de 2 octets.</span><span class="sxs-lookup"><span data-stu-id="a6358-120">The property is a 2-byte **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="a6358-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID du type DRM \_**</span><span class="sxs-lookup"><span data-stu-id="a6358-121"><span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**DRM\_TYPE\_GUID**</span></span>
</dt> <dd>

<span data-ttu-id="a6358-122">La propriété est une valeur GUID de 128 bits (6 octets).</span><span class="sxs-lookup"><span data-stu-id="a6358-122">The property is a 128-bit (6-byte) GUID value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6358-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6358-123">Requirements</span></span>



| <span data-ttu-id="a6358-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6358-124">Requirement</span></span> | <span data-ttu-id="a6358-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6358-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6358-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6358-126">Header</span></span><br/> | <dl> <span data-ttu-id="a6358-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6358-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6358-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6358-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6358-129">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="a6358-129">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





