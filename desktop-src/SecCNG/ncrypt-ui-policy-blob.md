---
description: Utilisé avec la \_ propriété de propriété de stratégie d’interface utilisateur NCRYPT \_ \_ pour contenir les informations d’interface utilisateur pour une clé.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Structure de NCRYPT_UI_POLICY_BLOB (ncrypt \_ Provider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528726"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="afba6-103">\_Structure d' \_ \_ objet blob de stratégie d’interface utilisateur NCRYPT</span><span class="sxs-lookup"><span data-stu-id="afba6-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="afba6-104">La structure d' **\_ \_ \_ objet blob de stratégie d’interface utilisateur ncrypt** est utilisée avec la propriété de [**\_ \_ \_ propriété de stratégie**](key-storage-property-identifiers.md) d’interface utilisateur ncrypt pour contenir les informations d’interface utilisateur d’une clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="afba6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="afba6-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="afba6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="afba6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="afba6-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="afba6-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="afba6-108">Numéro de version de la structure.</span><span class="sxs-lookup"><span data-stu-id="afba6-108">The version number of the structure.</span></span> <span data-ttu-id="afba6-109">Ce membre doit contenir 1.</span><span class="sxs-lookup"><span data-stu-id="afba6-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="afba6-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="afba6-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="afba6-111">Ensemble d’indicateurs qui fournissent des informations supplémentaires sur l’interface utilisateur ou des spécifications.</span><span class="sxs-lookup"><span data-stu-id="afba6-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="afba6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="afba6-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="afba6-113">Signification</span><span class="sxs-lookup"><span data-stu-id="afba6-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="afba6-114"><dt>**NCRYPT \_ \_Indicateur de \_ clé \_ Protect UI**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="afba6-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="afba6-115">Affichez l’interface utilisateur de clé forte si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="afba6-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="afba6-116"><dt>**NCRYPT \_ \_Indicateur de \_ \_ protection élevée \_ de force d’interface utilisateur**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="afba6-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="afba6-117">Forcez la protection élevée.</span><span class="sxs-lookup"><span data-stu-id="afba6-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="afba6-118">**cbCreationTitle**</span><span class="sxs-lookup"><span data-stu-id="afba6-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="afba6-119">Longueur, en octets, du titre de création.</span><span class="sxs-lookup"><span data-stu-id="afba6-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="afba6-120">Le titre de création est une chaîne Unicode terminée par le caractère null qui spécifie le texte utilisé comme titre de la boîte de dialogue clé forte lorsque la clé est terminée.</span><span class="sxs-lookup"><span data-stu-id="afba6-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="afba6-121">Le titre de création doit être placé immédiatement après la structure d' **\_ \_ \_ objet blob de stratégie d’interface utilisateur NCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="afba6-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="afba6-122">Si la valeur du membre **cbCreationTitle** est définie sur 0, un titre de création par défaut est utilisé pour le titre de la boîte de dialogue clé forte.</span><span class="sxs-lookup"><span data-stu-id="afba6-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="afba6-123">Ce membre est utilisé uniquement lors de la finalisation de la clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="afba6-124">**cbFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="afba6-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="afba6-125">Longueur, en octets, du nom convivial de la clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="afba6-126">Le nom convivial est une chaîne Unicode se terminant par un caractère null qui contient le texte affiché dans la boîte de dialogue clé forte comme nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="afba6-127">Le nom convivial doit être placé immédiatement après le titre de création dans cet objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="afba6-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="afba6-128">Si la valeur du membre **cbFriendlyName** est définie sur 0, un nom par défaut est utilisé dans la boîte de dialogue clé forte.</span><span class="sxs-lookup"><span data-stu-id="afba6-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="afba6-129">Ce membre est utilisé à la fois lorsque la clé est terminée et lorsque la clé est utilisée.</span><span class="sxs-lookup"><span data-stu-id="afba6-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="afba6-130">**cbDescription**</span><span class="sxs-lookup"><span data-stu-id="afba6-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="afba6-131">Longueur, en octets, de la description de la clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="afba6-132">La description de clé est une chaîne Unicode se terminant par un caractère null qui contient le texte affiché dans la boîte de dialogue clé forte comme description de la clé.</span><span class="sxs-lookup"><span data-stu-id="afba6-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="afba6-133">La valeur de description doit être placée immédiatement après le nom convivial dans cet objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="afba6-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="afba6-134">Si la valeur du membre **cbDescription** est définie sur 0, une description par défaut est utilisée dans la boîte de dialogue clé forte.</span><span class="sxs-lookup"><span data-stu-id="afba6-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="afba6-135">Ce membre est utilisé à la fois lorsque la clé est terminée et lorsque la clé est utilisée.</span><span class="sxs-lookup"><span data-stu-id="afba6-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afba6-136">Notes</span><span class="sxs-lookup"><span data-stu-id="afba6-136">Remarks</span></span>

<span data-ttu-id="afba6-137">Cette structure est incluse dans l' \_ en-tête du fournisseur ncrypt. h.</span><span class="sxs-lookup"><span data-stu-id="afba6-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="afba6-138">Pour utiliser la structure, vous devez télécharger le [Kit de développement du fournisseur de services de chiffrement](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) à partir de Microsoft Connect.</span><span class="sxs-lookup"><span data-stu-id="afba6-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="afba6-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afba6-139">Requirements</span></span>



| <span data-ttu-id="afba6-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afba6-140">Requirement</span></span> | <span data-ttu-id="afba6-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="afba6-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="afba6-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afba6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="afba6-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afba6-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="afba6-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afba6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="afba6-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afba6-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afba6-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="afba6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="afba6-147"><dt>\_Fournisseur ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="afba6-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

