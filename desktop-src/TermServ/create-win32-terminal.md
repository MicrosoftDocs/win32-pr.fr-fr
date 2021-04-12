---
title: Créer une méthode de la classe Win32_Terminal
description: Crée un terminal avec les paramètres par défaut qui peuvent être personnalisés à l’aide des propriétés et des méthodes des \_ classes TerminalSetting Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Créer une méthode Services Bureau à distance
- Create Method Services Bureau à distance, Win32_Terminal Class
- Win32_Terminal de la classe Services Bureau à distance, Create, méthode
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464591"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="60ca7-106">Créer une méthode de la \_ classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="60ca7-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="60ca7-107">La méthode **Create** crée un terminal avec les paramètres par défaut qui peuvent être personnalisés à l’aide des propriétés et des méthodes des classes [**\_ TerminalSetting Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca7-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="60ca7-108">La fonction retourne zéro en cas de réussite et une erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="60ca7-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ca7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60ca7-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="60ca7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60ca7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ca7-111">*NewTerminalName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60ca7-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca7-112">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="60ca7-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="60ca7-113">*Transport* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60ca7-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca7-114">Transport pour le terminal.</span><span class="sxs-lookup"><span data-stu-id="60ca7-114">Transport for the terminal.</span></span> <span data-ttu-id="60ca7-115">Il s’agit d’une propriété de la classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca7-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="60ca7-116">*TerminalProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60ca7-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca7-117">Protocole pour le terminal.</span><span class="sxs-lookup"><span data-stu-id="60ca7-117">Protocol for the terminal.</span></span> <span data-ttu-id="60ca7-118">Il s’agit d’une propriété de la classe [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca7-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ca7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60ca7-119">Return value</span></span>

<span data-ttu-id="60ca7-120">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="60ca7-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="60ca7-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="60ca7-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ca7-122">Notes</span><span class="sxs-lookup"><span data-stu-id="60ca7-122">Remarks</span></span>

<span data-ttu-id="60ca7-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="60ca7-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60ca7-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="60ca7-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60ca7-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="60ca7-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60ca7-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60ca7-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ca7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60ca7-127">Requirements</span></span>



| <span data-ttu-id="60ca7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60ca7-128">Requirement</span></span> | <span data-ttu-id="60ca7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ca7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60ca7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ca7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="60ca7-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60ca7-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60ca7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ca7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="60ca7-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60ca7-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60ca7-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60ca7-134">Namespace</span></span><br/>                | <span data-ttu-id="60ca7-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="60ca7-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="60ca7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="60ca7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60ca7-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60ca7-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="60ca7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="60ca7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60ca7-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60ca7-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ca7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60ca7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ca7-141">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="60ca7-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

