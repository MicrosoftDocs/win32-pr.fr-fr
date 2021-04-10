---
description: Lire la configuration active du collecteur.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Méthode GetConfiguration de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950408"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="96949-103">Méthode GetConfiguration de la classe Control</span><span class="sxs-lookup"><span data-stu-id="96949-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="96949-104">Lire la configuration active du collecteur.</span><span class="sxs-lookup"><span data-stu-id="96949-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="96949-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96949-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="96949-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96949-107">*TimestampLow* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96949-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96949-108">Lorsque cette méthode est retournée, ce paramètre contient les bits de poids faible d’un horodatage qui indique quand la configuration a été définie.</span><span class="sxs-lookup"><span data-stu-id="96949-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="96949-109">*TimestampHigh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96949-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96949-110">Lorsque cette méthode est retournée, ce paramètre contient les bits de poids fort d’un horodatage qui indique quand la configuration a été définie.</span><span class="sxs-lookup"><span data-stu-id="96949-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96949-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96949-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="96949-112">0</span><span class="sxs-lookup"><span data-stu-id="96949-112">0</span></span>

<span data-ttu-id="96949-113">Échec</span><span class="sxs-lookup"><span data-stu-id="96949-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="96949-114">1</span><span class="sxs-lookup"><span data-stu-id="96949-114">1</span></span>

<span data-ttu-id="96949-115">Succès</span><span class="sxs-lookup"><span data-stu-id="96949-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96949-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96949-116">Requirements</span></span>



| <span data-ttu-id="96949-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96949-117">Requirement</span></span> | <span data-ttu-id="96949-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="96949-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96949-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96949-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96949-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="96949-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="96949-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96949-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96949-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="96949-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="96949-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96949-123">Namespace</span></span><br/>                | <span data-ttu-id="96949-124">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="96949-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="96949-125">MOF</span><span class="sxs-lookup"><span data-stu-id="96949-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96949-126"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96949-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="96949-127">DLL</span><span class="sxs-lookup"><span data-stu-id="96949-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96949-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96949-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="96949-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96949-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96949-130">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="96949-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




