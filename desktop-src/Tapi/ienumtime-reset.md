---
description: La méthode reset réinitialise le début de la séquence d’énumération.
ms.assetid: a9131da1-051d-493c-939d-07801fda2d49
title: 'IEnumTime :: Reset, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9615fbc07edfb93c2377a7455d94b5fcd8ccd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113606"
---
# <a name="ienumtimereset-method"></a><span data-ttu-id="1d8d1-103">IEnumTime :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="1d8d1-103">IEnumTime::Reset method</span></span>

<span data-ttu-id="1d8d1-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1d8d1-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1d8d1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1d8d1-106">La méthode **Reset** réinitialise le début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-106">The **Reset** method resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d8d1-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="1d8d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d8d1-108">Parameters</span></span>
<span data-ttu-id="1d8d1-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d8d1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d8d1-110">Return value</span></span>
<span data-ttu-id="1d8d1-111">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-111">This method can return one of these values.</span></span>

| <span data-ttu-id="1d8d1-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d8d1-112">Value</span></span> | <span data-ttu-id="1d8d1-113">Signification</span><span class="sxs-lookup"><span data-stu-id="1d8d1-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="1d8d1-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d8d1-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1d8d1-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="1d8d1-115">Method succeeded.</span></span> <br/>         |
