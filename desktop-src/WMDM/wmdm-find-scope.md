---
title: Énumération WMDM_FIND_SCOPE
description: Le \_ \_ type d’énumération de l’étendue de recherche WMDM définit la portée de l’objet de stockage.
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525149"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="88547-104">WMDM \_ Rechercher l' \_ énumération de l’étendue</span><span class="sxs-lookup"><span data-stu-id="88547-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="88547-105">Le type d’énumération de l' **\_ \_ étendue de recherche WMDM** définit la portée de l’objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="88547-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88547-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88547-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="88547-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="88547-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88547-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ Rechercher l' \_ étendue \_ globale**</span><span class="sxs-lookup"><span data-stu-id="88547-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="88547-109">Recherche de l’objet correspondant n’importe où sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88547-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="88547-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ Rechercher l' \_ étendue \_ enfants immédiats \_**</span><span class="sxs-lookup"><span data-stu-id="88547-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="88547-111">Recherche de l’objet correspondant dans ce stockage et ses enfants.</span><span class="sxs-lookup"><span data-stu-id="88547-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88547-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88547-112">Requirements</span></span>



| <span data-ttu-id="88547-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88547-113">Requirement</span></span> | <span data-ttu-id="88547-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="88547-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88547-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="88547-115">Header</span></span><br/> | <dl> <span data-ttu-id="88547-116"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88547-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88547-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88547-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88547-118">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="88547-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





