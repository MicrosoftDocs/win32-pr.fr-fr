---
description: Active cette Plug-and-Play appareil.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Activer la méthode de la classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512888"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="88cbb-103">Activer la méthode de la \_ classe Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="88cbb-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="88cbb-104">Active cette Plug-and-Play appareil.</span><span class="sxs-lookup"><span data-stu-id="88cbb-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88cbb-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="88cbb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88cbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88cbb-107">*rebootNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="88cbb-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88cbb-108">Indique si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="88cbb-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88cbb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88cbb-109">Requirements</span></span>



| <span data-ttu-id="88cbb-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88cbb-110">Requirement</span></span> | <span data-ttu-id="88cbb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="88cbb-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88cbb-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cbb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="88cbb-113">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88cbb-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="88cbb-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cbb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="88cbb-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="88cbb-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="88cbb-116">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="88cbb-116">Namespace</span></span><br/>                | <span data-ttu-id="88cbb-117">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="88cbb-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88cbb-118">MOF</span><span class="sxs-lookup"><span data-stu-id="88cbb-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88cbb-119"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88cbb-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88cbb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="88cbb-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88cbb-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cbb-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cbb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88cbb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cbb-123">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="88cbb-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




