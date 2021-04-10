---
title: Constantes WINBIO_IDENTITY_TYPE ( \_ types WINBIO. h)
description: Spécifiez le format des informations d’identité contenues dans la \_ structure d’identité WINBIO.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941901"
---
# <a name="winbio_identity_type-constants"></a><span data-ttu-id="fedd6-103">\_Constantes de type d’identité WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="fedd6-103">WINBIO\_IDENTITY\_TYPE Constants</span></span>

<span data-ttu-id="fedd6-104">Les constantes de **\_ \_ type d’identité WINBIO** suivantes peuvent être utilisées pour spécifier le format des informations d’identité contenues dans la structure d' [**\_ identité WINBIO**](winbio-identity.md) .</span><span class="sxs-lookup"><span data-stu-id="fedd6-104">The following **WINBIO\_IDENTITY\_TYPE** constants can be used to specify the format of the identity information contained in the [**WINBIO\_IDENTITY**](winbio-identity.md) structure.</span></span>



| <span data-ttu-id="fedd6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="fedd6-105">Constant</span></span>                                                                                                                                                                                      | <span data-ttu-id="fedd6-106">Description</span><span class="sxs-lookup"><span data-stu-id="fedd6-106">Description</span></span>                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="fedd6-107"><dt>**\_type d’ID WINBIO \_ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="fedd6-107"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="fedd6-108">Le modèle n’a pas d’ID associé.</span><span class="sxs-lookup"><span data-stu-id="fedd6-108">The template has no associated ID.</span></span> <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="fedd6-109"><dt>**\_ \_ caractère générique de type d’ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedd6-109"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="fedd6-110">La structure correspond à toutes les identités de modèle.</span><span class="sxs-lookup"><span data-stu-id="fedd6-110">The structure matches all template identities.</span></span><br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="fedd6-111"><dt>**\_GUID du \_ type d’ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fedd6-111"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="fedd6-112">Un GUID identifie le modèle.</span><span class="sxs-lookup"><span data-stu-id="fedd6-112">A GUID identifies the template.</span></span><br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="fedd6-113"><dt>**\_ID \_ sid type \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="fedd6-113"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="fedd6-114">Un SID de compte identifie le modèle.</span><span class="sxs-lookup"><span data-stu-id="fedd6-114">An account SID identifies the template.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="fedd6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fedd6-115">Requirements</span></span>



| <span data-ttu-id="fedd6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fedd6-116">Requirement</span></span> | <span data-ttu-id="fedd6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fedd6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fedd6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fedd6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fedd6-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fedd6-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fedd6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fedd6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fedd6-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fedd6-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fedd6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fedd6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fedd6-123"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fedd6-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fedd6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fedd6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fedd6-125">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="fedd6-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="fedd6-126">**\_identité WINBIO**</span><span class="sxs-lookup"><span data-stu-id="fedd6-126">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)
</dt> </dl>

 

 





