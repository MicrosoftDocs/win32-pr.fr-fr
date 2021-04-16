---
description: Désactive cet appareil Plug-and-Play.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Désactivation de la méthode de la classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523396"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="81069-103">Désactivation de la méthode de la \_ classe PnPEntity Win32</span><span class="sxs-lookup"><span data-stu-id="81069-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="81069-104">Désactive cet appareil Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="81069-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="81069-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81069-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="81069-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81069-107">*rebootNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81069-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81069-108">Indique si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="81069-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81069-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81069-109">Requirements</span></span>



| <span data-ttu-id="81069-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81069-110">Requirement</span></span> | <span data-ttu-id="81069-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="81069-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81069-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81069-112">Minimum supported client</span></span><br/> | <span data-ttu-id="81069-113">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81069-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81069-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81069-114">Minimum supported server</span></span><br/> | <span data-ttu-id="81069-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="81069-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="81069-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81069-116">Namespace</span></span><br/>                | <span data-ttu-id="81069-117">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="81069-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81069-118">MOF</span><span class="sxs-lookup"><span data-stu-id="81069-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81069-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81069-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81069-120">DLL</span><span class="sxs-lookup"><span data-stu-id="81069-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81069-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81069-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81069-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81069-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81069-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="81069-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




