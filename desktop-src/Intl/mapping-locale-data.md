---
description: NLS comprend un certain nombre de fonctions API que vos applications peuvent utiliser pour mapper les données de paramètres régionaux entre les identificateurs de paramètres régionaux et les noms de paramètres régionaux, et répertorier les paramètres régionaux neutres.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mappage des données de paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201796"
---
# <a name="mapping-locale-data"></a><span data-ttu-id="cdf6f-103">Mappage des données de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="cdf6f-103">Mapping Locale Data</span></span>

<span data-ttu-id="cdf6f-104">NLS comprend un certain nombre de fonctions API que vos applications peuvent utiliser pour mapper les données de paramètres régionaux entre les [identificateurs](locale-identifiers.md) de paramètres régionaux et les [noms de paramètres régionaux](locale-names.md), et répertorier les paramètres régionaux neutres.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-104">NLS includes a number of API functions that your applications can use to map locale data between [locale identifiers](locale-identifiers.md) and [locale names](locale-names.md), and list neutral locales.</span></span> <span data-ttu-id="cdf6f-105">Cette rubrique traite de l’utilisation de ces fonctions sur Windows Vista et versions ultérieures, ainsi que sur les systèmes d’exploitation antérieurs à Windows Vista (parfois appelés « systèmes de niveau inférieur »).</span><span class="sxs-lookup"><span data-stu-id="cdf6f-105">This topic discusses the use of these functions on Windows Vista and later and on pre-Windows Vista operating systems (sometimes called "downlevel systems").</span></span>

## <a name="map-locale-data-on-windows-vista-and-later"></a><span data-ttu-id="cdf6f-106">Mapper les données de paramètres régionaux sur Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="cdf6f-106">Map Locale Data on Windows Vista and Later</span></span>

<span data-ttu-id="cdf6f-107">NLS fournit plusieurs fonctions de mappage de paramètres régionaux utilisables par les applications que vous développez pour s’exécuter sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-107">NLS provides several locale mapping functions for use by applications that you develop to run on Windows Vista and later.</span></span> <span data-ttu-id="cdf6f-108">Il comprend également les fonctions que vos applications peuvent utiliser pour énumérer les paramètres régionaux neutres.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-108">It also includes functions that your applications can use to enumerate neutral locales.</span></span>

<span data-ttu-id="cdf6f-109">**Utiliser les fonctions de conversion standard pour le mappage de données**</span><span class="sxs-lookup"><span data-stu-id="cdf6f-109">**Use the Standard Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="cdf6f-110">Pour effectuer un mappage entre un nom de paramètres régionaux et un identificateur de paramètres régionaux, votre application peut appeler la fonction [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) .</span><span class="sxs-lookup"><span data-stu-id="cdf6f-110">To map between a locale name and a locale identifier, your application can call the [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) function.</span></span> <span data-ttu-id="cdf6f-111">L’application utilise [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) pour effectuer un mappage entre un identificateur de paramètres régionaux et un nom de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-111">The application uses [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) to map between a locale identifier and a locale name.</span></span>

<span data-ttu-id="cdf6f-112">**Répertorier les paramètres régionaux neutres**</span><span class="sxs-lookup"><span data-stu-id="cdf6f-112">**List Neutral Locales**</span></span>

<span data-ttu-id="cdf6f-113">Pour énumérer les paramètres régionaux neutres pour Windows 7 et versions ultérieures, votre application peut appeler [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) avec *DwFlags* défini sur [**locale \_ NEUTRALDATA**](locale-neutraldata.md).</span><span class="sxs-lookup"><span data-stu-id="cdf6f-113">To enumerate neutral locales for Windows 7 and later, your application can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) with *dwFlags* set to [**LOCALE\_NEUTRALDATA**](locale-neutraldata.md).</span></span> <span data-ttu-id="cdf6f-114">Elle peut également utiliser [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec *LCTYPE* défini sur [**locale \_ INEUTRAL**](locale-ineutral.md).</span><span class="sxs-lookup"><span data-stu-id="cdf6f-114">It can also use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) with *LCType* set to [**LOCALE\_INEUTRAL**](locale-ineutral.md).</span></span>

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a><span data-ttu-id="cdf6f-115">Mapper les données de paramètres régionaux sur les systèmes d’exploitation antérieurs à Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdf6f-115">Map Locale Data on Pre-Windows Vista Operating Systems</span></span>

<span data-ttu-id="cdf6f-116">NLS comprend une bibliothèque de liens directs (DLL) à utiliser pour les applications que vous développez pour qu’elles s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-116">NLS includes a direct-link library (DLL) to use for applications that you develop to run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="cdf6f-117">La DLL prend en charge les fonctions de conversion et de liste pour le mappage des données.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-117">The DLL supports both conversion and listing functions for data mapping.</span></span>

> [!Note]  
> <span data-ttu-id="cdf6f-118">Les applications qui s’exécutent uniquement sous Windows Vista et les versions ultérieures ne doivent pas utiliser les fonctions de mappage ou d’énumération de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-118">Applications that only run on Windows Vista and later should not use the downlevel mapping or listing functions.</span></span>

 

<span data-ttu-id="cdf6f-119">**Utiliser les fonctions de conversion de niveau inférieur pour le mappage de données**</span><span class="sxs-lookup"><span data-stu-id="cdf6f-119">**Use the Downlevel Conversion Functions for Data Mapping**</span></span>

<span data-ttu-id="cdf6f-120">Votre application ciblée sur un système de bas niveau peut appeler la fonction [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) pour convertir un identificateur de paramètres régionaux en un nom de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-120">Your application targeted at a downlevel system can call the [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) function to convert a locale identifier to a locale name.</span></span> <span data-ttu-id="cdf6f-121">S’il doit convertir un nom de paramètres régionaux en un identificateur de paramètres régionaux, il doit appeler [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span><span class="sxs-lookup"><span data-stu-id="cdf6f-121">If it needs to convert a locale name to a locale identifier, it should call [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).</span></span>

<span data-ttu-id="cdf6f-122">**Utiliser les fonctions de la liste de bas niveau pour énumérer les paramètres régionaux neutres**</span><span class="sxs-lookup"><span data-stu-id="cdf6f-122">**Use the Downlevel Listing Functions to Enumerate Neutral Locales**</span></span>

<span data-ttu-id="cdf6f-123">Votre application doit appeler [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) pour récupérer l’identificateur de paramètres régionaux du parent pour des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="cdf6f-123">Your application should call the [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) to retrieve the locale identifier of the parent for a locale.</span></span> <span data-ttu-id="cdf6f-124">Si l’application doit obtenir le nom des paramètres régionaux du parent pour les paramètres régionaux, elle doit appeler [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span><span class="sxs-lookup"><span data-stu-id="cdf6f-124">If the application needs to get the locale name of the parent for the locale, it should call [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdf6f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdf6f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf6f-126">Utilisation de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="cdf6f-126">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="cdf6f-127">Identificateurs de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="cdf6f-127">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="cdf6f-128">Noms de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="cdf6f-128">Locale Names</span></span>](locale-names.md)
</dt> </dl>

 

 



