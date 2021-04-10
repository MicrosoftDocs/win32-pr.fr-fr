---
description: La méthode GetLangFromLangID récupère une chaîne explicite lorsqu’elle reçoit un ID de langue primaire.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Méthode GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846314"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="8219f-103">Méthode GetLangFromLangID</span><span class="sxs-lookup"><span data-stu-id="8219f-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="8219f-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8219f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8219f-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8219f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8219f-106">La `GetLangFromLangID` méthode récupère une chaîne explicite lorsqu’elle reçoit un ID de langue primaire.</span><span class="sxs-lookup"><span data-stu-id="8219f-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="8219f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8219f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8219f-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span><span class="sxs-lookup"><span data-stu-id="8219f-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="8219f-109">Spécifie l’ID de langue primaire sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="8219f-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8219f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8219f-110">Return Value</span></span>

<span data-ttu-id="8219f-111">Retourne une représentation sous forme de chaîne de la langue qui peut être affichée dans l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="8219f-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="8219f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8219f-112">Remarks</span></span>

<span data-ttu-id="8219f-113">Bien que cette méthode soit nommée `GetLangFromLangID` , le paramètre que vous transmettez est en fait l’ID de langue principal, et non l’ID de langue.</span><span class="sxs-lookup"><span data-stu-id="8219f-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="8219f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8219f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8219f-115">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="8219f-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="8219f-116">**GetDVDTextLanguageLCID**</span><span class="sxs-lookup"><span data-stu-id="8219f-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



