---
title: Méthode Delete de la classe Win32_TSAccount
description: La méthode Delete supprime l’utilisateur, le groupe ou le compte d’ordinateur spécifié.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Supprimer la méthode Services Bureau à distance
- Delete, méthode Services Bureau à distance, classe Win32_TSAccount
- Win32_TSAccount de la classe Services Bureau à distance, méthode Delete
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385155"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="68605-106">Méthode Delete de la \_ classe TSAccount Win32</span><span class="sxs-lookup"><span data-stu-id="68605-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="68605-107">La méthode **Delete** supprime l’utilisateur, le groupe ou le compte d’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="68605-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="68605-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68605-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="68605-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68605-109">Parameters</span></span>

<span data-ttu-id="68605-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="68605-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68605-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68605-111">Return value</span></span>

<span data-ttu-id="68605-112">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="68605-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="68605-113">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="68605-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="68605-114">Notes</span><span class="sxs-lookup"><span data-stu-id="68605-114">Remarks</span></span>

<span data-ttu-id="68605-115">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="68605-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="68605-116">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="68605-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="68605-117">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="68605-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="68605-118">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="68605-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="68605-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68605-119">Requirements</span></span>



| <span data-ttu-id="68605-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68605-120">Requirement</span></span> | <span data-ttu-id="68605-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="68605-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68605-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68605-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68605-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68605-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68605-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68605-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68605-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68605-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68605-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68605-126">Namespace</span></span><br/>                | <span data-ttu-id="68605-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="68605-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="68605-128">MOF</span><span class="sxs-lookup"><span data-stu-id="68605-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68605-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68605-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="68605-130">DLL</span><span class="sxs-lookup"><span data-stu-id="68605-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68605-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68605-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68605-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68605-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68605-133">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="68605-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

