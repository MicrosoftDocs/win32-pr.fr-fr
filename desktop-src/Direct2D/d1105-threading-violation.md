---
title: Violation de Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Une interface de location a été accessible simultanément à partir de plusieurs threads.
keywords:
- Violation de Threading D1105 Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106529044"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="ec50d-104">D1105 : violation de thread</span><span class="sxs-lookup"><span data-stu-id="ec50d-104">D1105: Threading Violation</span></span>

<span data-ttu-id="ec50d-105">Une \[ *interface* \] d’interface de location de thread a été accessible simultanément à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="ec50d-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="ec50d-106">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="ec50d-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="ec50d-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="ec50d-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="ec50d-108">Adresse de l’interface qui a été accessible par plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="ec50d-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="ec50d-109">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="ec50d-109">Possible Causes</span></span>

<span data-ttu-id="ec50d-110">Utilisation d’une instance d’objet à partir de la même fabrique à thread unique à partir de deux threads différents.</span><span class="sxs-lookup"><span data-stu-id="ec50d-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




