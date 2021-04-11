---
title: Structure WINBIO_IDENTITY ( \_ types WINBIO. h)
description: Contient une valeur d’identification associée à un modèle biométrique.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API de Windows Biometric Framework de structure de WINBIO_IDENTITY
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103996"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="3dd4a-104">\_Structure d’identité WINBIO</span><span class="sxs-lookup"><span data-stu-id="3dd4a-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="3dd4a-105">La structure d' **\_ identité WINBIO** contient une valeur d’identification associée à un modèle biométrique.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd4a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dd4a-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="3dd4a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3dd4a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3dd4a-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-109">Spécifie le format des informations d’identité contenues dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="3dd4a-110">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3dd4a-110">This can be one of the following values:</span></span>



| <span data-ttu-id="3dd4a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dd4a-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="3dd4a-112">Signification</span><span class="sxs-lookup"><span data-stu-id="3dd4a-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="3dd4a-113"><dt>**\_type d’ID WINBIO \_ \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4a-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="3dd4a-114">Le modèle n’a pas d’ID associé.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="3dd4a-115"><dt>**\_ \_ caractère générique de type d’ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4a-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="3dd4a-116">La structure correspond à toutes les identités de modèle.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="3dd4a-117"><dt>**\_GUID du \_ type d’ID WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4a-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="3dd4a-118">La structure contient un GUID associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="3dd4a-119"><dt>**\_ID \_ sid type \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4a-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="3dd4a-120">La structure contient le SID de compte associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3dd4a-121">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-122">Union qui peut contenir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3dd4a-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3dd4a-123">**Null**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-124">Contient 1 si le membre de **type** est **WINBIO \_ ID de \_ type \_ null**.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3dd4a-125">**Caractère générique**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-126">Contient 1 si le membre de **type** est un **type d' \_ ID WINBIO \_ \_ générique**.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="3dd4a-127">**TemplateGuid**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-128">Contient une valeur de GUID 128 bits qui identifie le modèle si le membre de **type** est **WINBIO \_ ID de \_ type \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="3dd4a-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-130">Structure qui contient un SID de compte si le membre de **type** est **WINBIO \_ ID \_ type \_ sid**.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="3dd4a-131">**Taille**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-132">Nombre de caractères dans le SID.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="3dd4a-133">**Données**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="3dd4a-134">Tableau de caractères non signés qui contiennent le SID.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="3dd4a-135">La taille maximale actuelle du tableau est de 68 caractères.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dd4a-136">Notes</span><span class="sxs-lookup"><span data-stu-id="3dd4a-136">Remarks</span></span>

<span data-ttu-id="3dd4a-137">Cette structure est utilisée dans les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3dd4a-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="3dd4a-138">**WinBioDeleteTemplate**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="3dd4a-139">**WinBioEnrollCommit**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="3dd4a-140">**WinBioEnumEnrollments**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="3dd4a-141">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="3dd4a-142">**WinBioIdentify**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="3dd4a-143">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="3dd4a-144">**WinBioVerify**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="3dd4a-145">**WinBioVerifyWithCallback**</span><span class="sxs-lookup"><span data-stu-id="3dd4a-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="3dd4a-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3dd4a-146">Requirements</span></span>



| <span data-ttu-id="3dd4a-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3dd4a-147">Requirement</span></span> | <span data-ttu-id="3dd4a-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3dd4a-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd4a-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dd4a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd4a-150">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dd4a-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="3dd4a-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3dd4a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd4a-152">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3dd4a-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3dd4a-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="3dd4a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd4a-154"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dd4a-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd4a-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3dd4a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd4a-156">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="3dd4a-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





