---
description: Comparez l’argument à la configuration active du collecteur.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Méthode IsConfigurationEqual de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747788"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="a6bce-103">Méthode IsConfigurationEqual de la classe Control</span><span class="sxs-lookup"><span data-stu-id="a6bce-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="a6bce-104">Comparez l’argument à la configuration active du collecteur.</span><span class="sxs-lookup"><span data-stu-id="a6bce-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6bce-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="a6bce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6bce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6bce-107">*Configuration* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="a6bce-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6bce-108">Configuration à comparer à la configuration active.</span><span class="sxs-lookup"><span data-stu-id="a6bce-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6bce-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6bce-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a6bce-110">0</span><span class="sxs-lookup"><span data-stu-id="a6bce-110">0</span></span>

<span data-ttu-id="a6bce-111">Échec</span><span class="sxs-lookup"><span data-stu-id="a6bce-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a6bce-112">1</span><span class="sxs-lookup"><span data-stu-id="a6bce-112">1</span></span>

<span data-ttu-id="a6bce-113">Succès</span><span class="sxs-lookup"><span data-stu-id="a6bce-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6bce-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6bce-114">Requirements</span></span>



| <span data-ttu-id="a6bce-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6bce-115">Requirement</span></span> | <span data-ttu-id="a6bce-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6bce-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bce-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6bce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6bce-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6bce-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6bce-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6bce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6bce-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a6bce-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="a6bce-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a6bce-121">Namespace</span></span><br/>                | <span data-ttu-id="a6bce-122">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="a6bce-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="a6bce-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a6bce-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6bce-124"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6bce-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6bce-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a6bce-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6bce-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6bce-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a6bce-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6bce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6bce-128">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="a6bce-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




