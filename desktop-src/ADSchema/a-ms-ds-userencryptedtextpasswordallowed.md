---
title: ms-DS-attribut-Text-Encrypted-Text-Password-allowed
description: Indique si Active Directory stockera le mot de passe dans le format de chiffrement réversible.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de l’attribut ms-DS-Encrypted-Text-Password-allowed-Password
- Schéma AD de l’attribut ms-DS-UserEncryptedTextPasswordAllowed
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479757"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a><span data-ttu-id="4e33a-105">ms-DS-attribut-Text-Encrypted-Text-Password-allowed</span><span class="sxs-lookup"><span data-stu-id="4e33a-105">ms-DS-User-Encrypted-Text-Password-Allowed attribute</span></span>

<span data-ttu-id="4e33a-106">Indique si Active Directory stockera le mot de passe dans le format de chiffrement réversible.</span><span class="sxs-lookup"><span data-stu-id="4e33a-106">Indicates whether Active Directory will store the password in the reversible encryption format.</span></span> <span data-ttu-id="4e33a-107">True si le mot de passe est stocké dans le format de chiffrement réversible ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="4e33a-107">True if the password is stored in the reversible encryption format; otherwise, False.</span></span>

> [!Note]  
> <span data-ttu-id="4e33a-108">Cet attribut n’est pas utilisé par [services AD LDS (Active Directory Lightweight Directory Services)](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) et est uniquement inclus pour l’exhaustivité/la parité avec UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="4e33a-108">This attribute is not used by [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) and is only included for completeness/parity with userAccountControl.</span></span> <span data-ttu-id="4e33a-109">AD LDS ne stocke pas les mots de passe avec un chiffrement réversible, quelle que soit la valeur de cet attribut sur un objet donné ou si la stratégie de sécurité de l’ordinateur se rapporte à un chiffrement réversible sur l’ordinateur lui-même.</span><span class="sxs-lookup"><span data-stu-id="4e33a-109">AD LDS does not store passwords with reversible encryption, regardless of this attribute's value on any given object or the computer security policy pertaining to reversible encryption on the computer itself.</span></span>

 



| <span data-ttu-id="4e33a-110">Entrée</span><span class="sxs-lookup"><span data-stu-id="4e33a-110">Entry</span></span> | <span data-ttu-id="4e33a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e33a-111">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="4e33a-112">CN</span><span class="sxs-lookup"><span data-stu-id="4e33a-112">CN</span></span>                | <span data-ttu-id="4e33a-113">ms-DS-User-Encrypted-Text-Password-allowed</span><span class="sxs-lookup"><span data-stu-id="4e33a-113">ms-DS-User-Encrypted-Text-Password-Allowed</span></span> |
| <span data-ttu-id="4e33a-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="4e33a-114">Ldap-Display-Name</span></span> | <span data-ttu-id="4e33a-115">ms-DS-UserEncryptedTextPasswordAllowed</span><span class="sxs-lookup"><span data-stu-id="4e33a-115">ms-DS-UserEncryptedTextPasswordAllowed</span></span>     |
| <span data-ttu-id="4e33a-116">Taille</span><span class="sxs-lookup"><span data-stu-id="4e33a-116">Size</span></span>              | \-                                         |
| <span data-ttu-id="4e33a-117">Mettre à jour le privilège</span><span class="sxs-lookup"><span data-stu-id="4e33a-117">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="4e33a-118">Fréquence des mises à jour</span><span class="sxs-lookup"><span data-stu-id="4e33a-118">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="4e33a-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4e33a-119">Attribute-Id</span></span>      | <span data-ttu-id="4e33a-120">1.2.840.113556.1.4.1856</span><span class="sxs-lookup"><span data-stu-id="4e33a-120">1.2.840.113556.1.4.1856</span></span>                    |
| <span data-ttu-id="4e33a-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="4e33a-121">System-Id-Guid</span></span>    | <span data-ttu-id="4e33a-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span><span class="sxs-lookup"><span data-stu-id="4e33a-122">5a87c7f2-93c5-454c-a8c5-8cb09613292e</span></span>       |
| <span data-ttu-id="4e33a-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e33a-123">Syntax</span></span>            | [<span data-ttu-id="4e33a-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e33a-124">**Boolean**</span></span>](s-boolean.md)               |



## <a name="implementations"></a><span data-ttu-id="4e33a-125">Implémentations</span><span class="sxs-lookup"><span data-stu-id="4e33a-125">Implementations</span></span>

-   [<span data-ttu-id="4e33a-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4e33a-126">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="4e33a-127">ADAM</span><span class="sxs-lookup"><span data-stu-id="4e33a-127">ADAM</span></span>



| <span data-ttu-id="4e33a-128">Entrée</span><span class="sxs-lookup"><span data-stu-id="4e33a-128">Entry</span></span> | <span data-ttu-id="4e33a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e33a-129">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4e33a-130">ID de lien</span><span class="sxs-lookup"><span data-stu-id="4e33a-130">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4e33a-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e33a-131">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4e33a-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e33a-132">System-Only</span></span>            | <span data-ttu-id="4e33a-133">Faux</span><span class="sxs-lookup"><span data-stu-id="4e33a-133">False</span></span>                                                             |
| <span data-ttu-id="4e33a-134">Est de valeur unique</span><span class="sxs-lookup"><span data-stu-id="4e33a-134">Is-Single-Valued</span></span>       | <span data-ttu-id="4e33a-135">Vrai</span><span class="sxs-lookup"><span data-stu-id="4e33a-135">True</span></span>                                                              |
| <span data-ttu-id="4e33a-136">Est indexé</span><span class="sxs-lookup"><span data-stu-id="4e33a-136">Is Indexed</span></span>             | <span data-ttu-id="4e33a-137">Faux</span><span class="sxs-lookup"><span data-stu-id="4e33a-137">False</span></span>                                                             |
| <span data-ttu-id="4e33a-138">Dans le catalogue global</span><span class="sxs-lookup"><span data-stu-id="4e33a-138">In Global Catalog</span></span>      | <span data-ttu-id="4e33a-139">Faux</span><span class="sxs-lookup"><span data-stu-id="4e33a-139">False</span></span>                                                             |
| <span data-ttu-id="4e33a-140">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="4e33a-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e33a-141">O :BAG : BAD : S :</span><span class="sxs-lookup"><span data-stu-id="4e33a-141">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4e33a-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e33a-142">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4e33a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e33a-143">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4e33a-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e33a-144">Search-Flags</span></span>           | <span data-ttu-id="4e33a-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e33a-145">0x00000000</span></span>                                                        |
| <span data-ttu-id="4e33a-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e33a-146">System-Flags</span></span>           | <span data-ttu-id="4e33a-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e33a-147">0x00000010</span></span>                                                        |
| <span data-ttu-id="4e33a-148">Classes utilisées dans</span><span class="sxs-lookup"><span data-stu-id="4e33a-148">Classes used in</span></span>        | [<span data-ttu-id="4e33a-149">**ms-DS-Bindable-objet**</span><span class="sxs-lookup"><span data-stu-id="4e33a-149">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4e33a-150">Notes</span><span class="sxs-lookup"><span data-stu-id="4e33a-150">Remarks</span></span>

<span data-ttu-id="4e33a-151">Dans ADAM, cet attribut remplace l’indicateur de [**\_ mot de \_ \_ \_ passe de \_ texte chiffré de publicités UF**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) de l’attribut [**UserAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="4e33a-151">In ADAM, this attribute replaces the [**ADS\_UF\_ENCRYPTED\_TEXT\_PASSWORD\_ALLOWED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

