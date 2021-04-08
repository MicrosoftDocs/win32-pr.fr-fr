---
title: Méthode Revoke de la classe Win32_TSIssuedLicense
description: Révoque les licences d’accès client par périphérique Services Bureau à distance (RDS \ 160 ; Licences d’accès client par périphérique) qui sont représentées par l' \_ objet Win32 TSIssuedLicense. Il ne s’agit pas d’une fonction statique.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Revoke, méthode Services Bureau à distance
- Revoke, méthode Services Bureau à distance, classe Win32_TSIssuedLicense
- Win32_TSIssuedLicense de la classe Services Bureau à distance, Revoke, méthode
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743621"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="45c2b-107">Méthode Revoke de la \_ classe TSIssuedLicense Win32</span><span class="sxs-lookup"><span data-stu-id="45c2b-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="45c2b-108">Révoque les licences d’accès client Services Bureau à distance par périphérique (CAL par périphérique) qui sont représentées par l’objet [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="45c2b-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="45c2b-109">Il ne s’agit pas d’une fonction statique.</span><span class="sxs-lookup"><span data-stu-id="45c2b-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c2b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45c2b-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="45c2b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45c2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c2b-112">*RevokableCals* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45c2b-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c2b-113">Nombre de licences d’accès client aux services Bureau à distance du même type que l’objet actuel qui peut être révoqué.</span><span class="sxs-lookup"><span data-stu-id="45c2b-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="45c2b-114">*NextRevokeAllowedOn* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="45c2b-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45c2b-115">Date à laquelle l’administrateur peut ensuite tenter de révoquer des licences.</span><span class="sxs-lookup"><span data-stu-id="45c2b-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="45c2b-116">Ce paramètre contient uniquement des données valides lorsque l’appel de la méthode **Revoke** a échoué, car le nombre maximal de révocations a été atteint.</span><span class="sxs-lookup"><span data-stu-id="45c2b-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45c2b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="45c2b-117">Remarks</span></span>

<span data-ttu-id="45c2b-118">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="45c2b-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="45c2b-119">Seules les CAL par périphérique peuvent être révoquées.</span><span class="sxs-lookup"><span data-stu-id="45c2b-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="45c2b-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="45c2b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="45c2b-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="45c2b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45c2b-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="45c2b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="45c2b-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="45c2b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="45c2b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45c2b-124">Requirements</span></span>



| <span data-ttu-id="45c2b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45c2b-125">Requirement</span></span> | <span data-ttu-id="45c2b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="45c2b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c2b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45c2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45c2b-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="45c2b-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="45c2b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45c2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45c2b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45c2b-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="45c2b-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45c2b-131">Namespace</span></span><br/>                | <span data-ttu-id="45c2b-132">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="45c2b-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="45c2b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="45c2b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45c2b-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45c2b-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="45c2b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="45c2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45c2b-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45c2b-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c2b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45c2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c2b-138">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="45c2b-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

