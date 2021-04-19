---
description: Arrête le collecteur. Si le collecteur s’exécute en tant que service, l’arrêt du service est la meilleure approche.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Méthode Shutdown de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538627"
---
# <a name="shutdown-method-of-the-control-class"></a><span data-ttu-id="42a1f-104">Méthode Shutdown de la classe Control</span><span class="sxs-lookup"><span data-stu-id="42a1f-104">Shutdown method of the Control class</span></span>

<span data-ttu-id="42a1f-105">Arrête le collecteur.</span><span class="sxs-lookup"><span data-stu-id="42a1f-105">Stops the collector.</span></span> <span data-ttu-id="42a1f-106">Si le collecteur s’exécute en tant que service, l’arrêt du service est la meilleure approche.</span><span class="sxs-lookup"><span data-stu-id="42a1f-106">If the collector is running as a service, stopping the service is the better approach.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a1f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42a1f-107">Syntax</span></span>


```mof
void Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="42a1f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42a1f-108">Parameters</span></span>

<span data-ttu-id="42a1f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="42a1f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42a1f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42a1f-110">Return value</span></span>

<span data-ttu-id="42a1f-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="42a1f-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a1f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42a1f-112">Requirements</span></span>



| <span data-ttu-id="42a1f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42a1f-113">Requirement</span></span> | <span data-ttu-id="42a1f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="42a1f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a1f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a1f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="42a1f-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42a1f-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="42a1f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42a1f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="42a1f-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42a1f-118">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="42a1f-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="42a1f-119">Namespace</span></span><br/>                | <span data-ttu-id="42a1f-120">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="42a1f-120">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="42a1f-121">MOF</span><span class="sxs-lookup"><span data-stu-id="42a1f-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42a1f-122"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42a1f-122"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="42a1f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="42a1f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a1f-124"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42a1f-124"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="42a1f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42a1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a1f-126">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="42a1f-126">**Control**</span></span>](control.md)
</dt> </dl>

 

 




