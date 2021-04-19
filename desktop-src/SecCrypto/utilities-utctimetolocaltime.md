---
description: Convertit le temps universel coordonné (heure de Greenwich) en heure locale de l’ordinateur.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Méthode Utilities. UTCTimeToLocalTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545321"
---
# <a name="utilitiesutctimetolocaltime-method"></a><span data-ttu-id="fd171-103">Méthode Utilities. UTCTimeToLocalTime</span><span class="sxs-lookup"><span data-stu-id="fd171-103">Utilities.UTCTimeToLocalTime method</span></span>

<span data-ttu-id="fd171-104">\[La méthode **UTCTimeToLocalTime** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="fd171-104">\[The **UTCTimeToLocalTime** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="fd171-105">La méthode **UTCTimeToLocalTime** convertit le temps universel coordonné (heure de Greenwich) en heure locale de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd171-105">The **UTCTimeToLocalTime** method converts Coordinated Universal Time (Greenwich Mean Time) to the computer's local time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd171-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd171-106">Syntax</span></span>


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a><span data-ttu-id="fd171-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd171-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd171-108">*UTCTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd171-108">*UTCTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd171-109">Temps universel coordonné à convertir en heure locale de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd171-109">The Coordinated Universal Time to be converted to the computer's local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd171-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd171-110">Return value</span></span>

<span data-ttu-id="fd171-111">Heure locale qui correspond au temps universel coordonné spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd171-111">The local time that corresponds to the specified Coordinated Universal Time.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd171-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fd171-112">Remarks</span></span>

<span data-ttu-id="fd171-113">Alors que le système utilise le temps universel coordonné en interne, les applications affichent généralement l’heure locale, qui correspond à la date et à l’heure du fuseau horaire local de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd171-113">While the system uses Coordinated Universal Time internally, applications generally display the local time, which is the date and time of day for the computer's local time zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd171-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd171-114">Requirements</span></span>



| <span data-ttu-id="fd171-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd171-115">Requirement</span></span> | <span data-ttu-id="fd171-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd171-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd171-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fd171-117">Redistributable</span></span><br/> | <span data-ttu-id="fd171-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd171-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd171-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fd171-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="fd171-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd171-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd171-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd171-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd171-122">**Services**</span><span class="sxs-lookup"><span data-stu-id="fd171-122">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




