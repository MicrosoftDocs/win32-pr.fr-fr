---
description: Chaque paramètre régional est associé à un type de calendrier par défaut (type de données CALTYPE). Les paramètres régionaux peuvent également avoir un autre type de calendrier. Pour plus d’informations sur les types de calendriers, consultez informations sur le type de calendrier.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Date et calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867937"
---
# <a name="date-and-calendar"></a><span data-ttu-id="a3295-105">Date et calendrier</span><span class="sxs-lookup"><span data-stu-id="a3295-105">Date and Calendar</span></span>

<span data-ttu-id="a3295-106">Chaque [paramètre régional](locales-and-languages.md) est associé à un type de calendrier par défaut (type de données CALTYPE).</span><span class="sxs-lookup"><span data-stu-id="a3295-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="a3295-107">Les paramètres régionaux peuvent également avoir un autre type de calendrier.</span><span class="sxs-lookup"><span data-stu-id="a3295-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="a3295-108">Pour plus d’informations sur les types de calendriers, consultez [informations sur le type de calendrier](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="a3295-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="a3295-109">Pour utiliser un autre type de calendrier pour des paramètres régionaux, votre application doit définir la constante [ \_ IOPTIONALCALENDAR des paramètres régionaux](locale-ioptionalcalendar.md) sur l’autre type de calendrier pour les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="a3295-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="a3295-110">La plupart des paramètres régionaux utilisent le calendrier grégorien standard et un nombre défini de formats de date.</span><span class="sxs-lookup"><span data-stu-id="a3295-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="a3295-111">Ces choix par défaut pour les formats de date sont disponibles pour l’affichage à l’aide de la fonction [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .</span><span class="sxs-lookup"><span data-stu-id="a3295-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="a3295-112">Certains paramètres régionaux requièrent des considérations particulières lors de la création d’une liste complète de choix de format.</span><span class="sxs-lookup"><span data-stu-id="a3295-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="a3295-113">Certains de ces paramètres régionaux requièrent l’insertion de chaînes de texte dans la chaîne de format de date, tandis que d’autres nécessitent une méthode de calcul entièrement différente des valeurs.</span><span class="sxs-lookup"><span data-stu-id="a3295-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="a3295-114">Une application répond à ces exigences spéciales par l’ajout de certains types d’informations de paramètres régionaux et de types de calendrier.</span><span class="sxs-lookup"><span data-stu-id="a3295-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="a3295-115">Pour plus d’informations sur l’implémentation de dates et de calendriers dans vos applications, consultez [récupération des informations de date et d’heure](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="a3295-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3295-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3295-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3295-117">À propos de la prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="a3295-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="a3295-118">Informations sur le type de calendrier</span><span class="sxs-lookup"><span data-stu-id="a3295-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="a3295-119">Récupération des informations de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="a3295-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="a3295-120">**EnumDateFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="a3295-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="a3295-121">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="a3295-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



