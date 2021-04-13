---
title: Méthode SetPortNumbers de la classe Win32_TSGatewayResourceAuthorizationPolicy
description: Définit les numéros de port qui sont autorisés à se connecter à la ressource par le biais de Bureau à distance passerelle (passerelle des services Bureau à distance).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPortNumbers
- Services Bureau à distance de la méthode SetPortNumbers, classe Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de la classe Services Bureau à distance, méthode SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465978"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="83400-106">Méthode SetPortNumbers de la \_ classe Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="83400-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="83400-107">Définit les numéros de port qui sont autorisés à se connecter à la ressource par le biais de Bureau à distance passerelle (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="83400-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="83400-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83400-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="83400-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83400-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83400-110">*PortNumbers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83400-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83400-111">Liste des numéros de port séparés par des points-virgules autorisés pour cette stratégie d’autorisation des ressources Bureau à distance (RD RAP).</span><span class="sxs-lookup"><span data-stu-id="83400-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="83400-112">Pour autoriser n’importe quel numéro de port, définissez « \* ».</span><span class="sxs-lookup"><span data-stu-id="83400-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83400-113">Notes</span><span class="sxs-lookup"><span data-stu-id="83400-113">Remarks</span></span>

<span data-ttu-id="83400-114">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="83400-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="83400-115">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="83400-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="83400-116">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="83400-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="83400-117">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="83400-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="83400-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83400-118">Requirements</span></span>



| <span data-ttu-id="83400-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83400-119">Requirement</span></span> | <span data-ttu-id="83400-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="83400-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83400-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83400-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83400-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83400-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="83400-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83400-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83400-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83400-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="83400-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83400-125">Namespace</span></span><br/>                | <span data-ttu-id="83400-126">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="83400-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="83400-127">MOF</span><span class="sxs-lookup"><span data-stu-id="83400-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83400-128"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83400-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="83400-129">DLL</span><span class="sxs-lookup"><span data-stu-id="83400-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83400-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83400-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="83400-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83400-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83400-132">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="83400-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

