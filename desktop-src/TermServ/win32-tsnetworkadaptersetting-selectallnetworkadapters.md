---
title: Méthode SelectAllNetworkAdapters de la classe Win32_TSNetworkAdapterSetting
description: La méthode SelectAllNetworkAdapters sélectionne toutes les cartes réseau.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectAllNetworkAdapters
- Services Bureau à distance de la méthode SelectAllNetworkAdapters, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317322"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="76814-106">Méthode SelectAllNetworkAdapters de la \_ classe Win32 TSNetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="76814-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="76814-107">La méthode **SelectAllNetworkAdapters** sélectionne toutes les cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="76814-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="76814-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76814-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="76814-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76814-109">Parameters</span></span>

<span data-ttu-id="76814-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="76814-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76814-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76814-111">Return value</span></span>

<span data-ttu-id="76814-112">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="76814-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="76814-113">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="76814-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="76814-114">Notes</span><span class="sxs-lookup"><span data-stu-id="76814-114">Remarks</span></span>

<span data-ttu-id="76814-115">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="76814-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="76814-116">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="76814-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="76814-117">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="76814-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="76814-118">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="76814-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="76814-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76814-119">Requirements</span></span>



| <span data-ttu-id="76814-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76814-120">Requirement</span></span> | <span data-ttu-id="76814-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="76814-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76814-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76814-122">Minimum supported client</span></span><br/> | <span data-ttu-id="76814-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76814-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76814-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76814-124">Minimum supported server</span></span><br/> | <span data-ttu-id="76814-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76814-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76814-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76814-126">Namespace</span></span><br/>                | <span data-ttu-id="76814-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="76814-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="76814-128">MOF</span><span class="sxs-lookup"><span data-stu-id="76814-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76814-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76814-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="76814-130">DLL</span><span class="sxs-lookup"><span data-stu-id="76814-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76814-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76814-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76814-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76814-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76814-133">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="76814-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

