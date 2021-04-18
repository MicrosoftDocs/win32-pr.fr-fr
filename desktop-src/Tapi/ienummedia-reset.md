---
description: La méthode reset réinitialise le début de la séquence d’énumération.
ms.assetid: 338e0614-8f18-4ee2-8697-66ff3898f813
title: 'IEnumMedia :: Reset, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14624d5a048df2f5bc80205f34f262068c53da74
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106529235"
---
# <a name="ienummediareset-method"></a><span data-ttu-id="4454c-103">IEnumMedia :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="4454c-103">IEnumMedia::Reset method</span></span>

<span data-ttu-id="4454c-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4454c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4454c-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="4454c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4454c-106">La méthode **Reset** réinitialise le début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="4454c-106">The **Reset** method resets to the beginning of enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4454c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4454c-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="4454c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4454c-108">Parameters</span></span>
<span data-ttu-id="4454c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4454c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4454c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4454c-110">Return value</span></span>
<span data-ttu-id="4454c-111">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4454c-111">This method can return one of these values.</span></span>

| <span data-ttu-id="4454c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4454c-112">Value</span></span> | <span data-ttu-id="4454c-113">Signification</span><span class="sxs-lookup"><span data-stu-id="4454c-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="4454c-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4454c-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4454c-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4454c-115">Method succeeded.</span></span> <br/>         |
