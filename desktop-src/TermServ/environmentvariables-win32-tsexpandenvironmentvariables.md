---
title: Méthode EnvironmentVariables de la classe Win32_TSExpandEnvironmentVariables
description: Développe les variables d’environnement définies par le système. | Méthode EnvironmentVariables de la classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnvironmentVariables
- Services Bureau à distance de la méthode EnvironmentVariables, classe Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables de la classe Services Bureau à distance, méthode EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543010"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="d6d14-107">Méthode EnvironmentVariables de la \_ classe Win32 TSExpandEnvironmentVariables</span><span class="sxs-lookup"><span data-stu-id="d6d14-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="d6d14-108">Développe les variables d’environnement définies par le système.</span><span class="sxs-lookup"><span data-stu-id="d6d14-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6d14-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="d6d14-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6d14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d14-111">*OriginalString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6d14-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d14-112">Chaîne qui contient les variables d’environnement à développer.</span><span class="sxs-lookup"><span data-stu-id="d6d14-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="d6d14-113">*ExpandedString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6d14-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d14-114">Chaîne avec les variables d’environnement développées.</span><span class="sxs-lookup"><span data-stu-id="d6d14-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6d14-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d6d14-115">Remarks</span></span>

<span data-ttu-id="d6d14-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d6d14-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d6d14-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6d14-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6d14-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6d14-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d6d14-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d6d14-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6d14-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d6d14-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d14-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6d14-121">Requirements</span></span>



| <span data-ttu-id="d6d14-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6d14-122">Requirement</span></span> | <span data-ttu-id="d6d14-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6d14-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d14-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d14-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d14-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d14-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d6d14-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6d14-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d14-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6d14-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6d14-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6d14-128">Namespace</span></span><br/>                | <span data-ttu-id="d6d14-129">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d6d14-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d6d14-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d6d14-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6d14-131"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6d14-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d6d14-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d14-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d14-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d14-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d14-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d14-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d14-135">**\_TSExpandEnvironmentVariables Win32**</span><span class="sxs-lookup"><span data-stu-id="d6d14-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

