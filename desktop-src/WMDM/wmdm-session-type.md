---
title: Énumération WMDM_SESSION_TYPE
description: Le type \_ d' \_ énumération de type de session WMDM définit le type de session.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525374"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="53a7b-104">\_Énumération des types de session WMDM \_</span><span class="sxs-lookup"><span data-stu-id="53a7b-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="53a7b-105">Le type d’énumération de **\_ \_ type de session WMDM** définit le type de session.</span><span class="sxs-lookup"><span data-stu-id="53a7b-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a7b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53a7b-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="53a7b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="53a7b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53a7b-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ session \_ None**</span><span class="sxs-lookup"><span data-stu-id="53a7b-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="53a7b-109">La session n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="53a7b-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="53a7b-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_transfert de la session WMDM \_ sur l' \_ \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="53a7b-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="53a7b-111">La session est définie comme transfert de données vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="53a7b-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="53a7b-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transfert de session WMDM \_ à partir de l' \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="53a7b-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="53a7b-113">La session est définie comme transfert de données à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="53a7b-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="53a7b-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**suppression de la \_ session WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="53a7b-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="53a7b-115">La session est définie en tant que suppression de données.</span><span class="sxs-lookup"><span data-stu-id="53a7b-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="53a7b-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_session WMDM \_ personnalisée**</span><span class="sxs-lookup"><span data-stu-id="53a7b-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="53a7b-117">La session est définie en tant que session personnalisée.</span><span class="sxs-lookup"><span data-stu-id="53a7b-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53a7b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53a7b-118">Requirements</span></span>



| <span data-ttu-id="53a7b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53a7b-119">Requirement</span></span> | <span data-ttu-id="53a7b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="53a7b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53a7b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="53a7b-121">Header</span></span><br/> | <dl> <span data-ttu-id="53a7b-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53a7b-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a7b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53a7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a7b-124">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="53a7b-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





