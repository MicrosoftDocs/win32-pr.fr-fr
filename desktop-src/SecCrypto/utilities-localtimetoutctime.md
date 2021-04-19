---
description: Convertit l’heure locale de l’ordinateur en temps universel coordonné (heure de Greenwich).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Méthode Utilities. LocalTimeToUTCTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531591"
---
# <a name="utilitieslocaltimetoutctime-method"></a><span data-ttu-id="a4b51-103">Méthode Utilities. LocalTimeToUTCTime</span><span class="sxs-lookup"><span data-stu-id="a4b51-103">Utilities.LocalTimeToUTCTime method</span></span>

<span data-ttu-id="a4b51-104">\[La méthode **LocalTimeToUTCTime** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="a4b51-104">\[The **LocalTimeToUTCTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="a4b51-105">La méthode **LocalTimeToUTCTime** convertit l’heure locale de l’ordinateur en temps universel coordonné (heure de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="a4b51-105">The **LocalTimeToUTCTime** method converts the computer's local time to Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b51-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4b51-106">Syntax</span></span>


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a><span data-ttu-id="a4b51-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4b51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b51-108">*Localtime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4b51-108">*LocalTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b51-109">Heure locale à convertir en temps universel coordonné.</span><span class="sxs-lookup"><span data-stu-id="a4b51-109">The local time to be converted to Coordinated Universal Time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b51-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4b51-110">Return value</span></span>

<span data-ttu-id="a4b51-111">Temps universel coordonné qui correspond à l’heure locale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a4b51-111">The Coordinated Universal Time that corresponds to the specified local time.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b51-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b51-112">Remarks</span></span>

<span data-ttu-id="a4b51-113">Alors que le système utilise le temps universel coordonné en interne, les applications affichent généralement l’heure locale, qui correspond à la date et à l’heure du fuseau horaire local de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a4b51-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b51-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b51-114">Requirements</span></span>



| <span data-ttu-id="a4b51-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4b51-115">Requirement</span></span> | <span data-ttu-id="a4b51-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4b51-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b51-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a4b51-117">Redistributable</span></span><br/> | <span data-ttu-id="a4b51-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4b51-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a4b51-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b51-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="a4b51-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b51-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b51-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4b51-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b51-122">**Services**</span><span class="sxs-lookup"><span data-stu-id="a4b51-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




