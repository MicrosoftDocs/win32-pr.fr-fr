---
title: Méthode SetProfilePath de la classe Win32_TerminalServiceSetting
description: La méthode SetProfilePath définit la propriété ProfilePath de la classe.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetProfilePath
- Services Bureau à distance de la méthode SetProfilePath, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384543"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="62645-106">Méthode SetProfilePath de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="62645-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="62645-107">La méthode **SetProfilePath** définit la propriété **profilePath** de la classe.</span><span class="sxs-lookup"><span data-stu-id="62645-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="62645-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62645-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="62645-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62645-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62645-110">*ProfilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62645-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62645-111">Nouvelle valeur de la propriété **profilePath** , qui spécifie le chemin d’accès du profil pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="62645-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62645-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62645-112">Return value</span></span>

<span data-ttu-id="62645-113">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="62645-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="62645-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="62645-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="62645-115">Notes</span><span class="sxs-lookup"><span data-stu-id="62645-115">Remarks</span></span>

<span data-ttu-id="62645-116">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="62645-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="62645-117">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62645-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="62645-118">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="62645-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="62645-119">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="62645-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="62645-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62645-120">Requirements</span></span>



| <span data-ttu-id="62645-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62645-121">Requirement</span></span> | <span data-ttu-id="62645-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="62645-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62645-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62645-123">Minimum supported client</span></span><br/> | <span data-ttu-id="62645-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62645-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62645-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62645-125">Minimum supported server</span></span><br/> | <span data-ttu-id="62645-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62645-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62645-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62645-127">Namespace</span></span><br/>                | <span data-ttu-id="62645-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="62645-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="62645-129">MOF</span><span class="sxs-lookup"><span data-stu-id="62645-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62645-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62645-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="62645-131">DLL</span><span class="sxs-lookup"><span data-stu-id="62645-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62645-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62645-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62645-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62645-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62645-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="62645-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

