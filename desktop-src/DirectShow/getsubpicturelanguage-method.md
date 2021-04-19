---
description: La méthode GetSubpictureLanguage récupère la langue du flux de sous-image spécifié.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Méthode GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515304"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="7d226-103">Méthode GetSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="7d226-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="7d226-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7d226-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7d226-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7d226-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7d226-106">La `GetSubpictureLanguage` méthode récupère la langue du flux de sous-image spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d226-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="7d226-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d226-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d226-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="7d226-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="7d226-109">Spécifie le numéro de flux de sous-image dont vous souhaitez récupérer la langue de texte sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="7d226-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d226-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d226-110">Return Value</span></span>

<span data-ttu-id="7d226-111">Retourne une chaîne explicite identifiant la langue du flux audio dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="7d226-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



