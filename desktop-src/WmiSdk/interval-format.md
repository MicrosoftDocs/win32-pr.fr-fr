---
description: Définit des intervalles de date et d’heure avec un format similaire à la syntaxe de date et d’heure en scindant la chaîne en champs pour les jours, les heures, les minutes, les secondes et les microsecondes.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Format d’intervalle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526313"
---
# <a name="interval-format"></a><span data-ttu-id="85fda-103">Format d’intervalle</span><span class="sxs-lookup"><span data-stu-id="85fda-103">Interval Format</span></span>

<span data-ttu-id="85fda-104">WMI définit des intervalles de date et d’heure avec un format similaire à la syntaxe de date et d’heure en scindant la chaîne en champs pour les jours, les heures, les minutes, les secondes et les microsecondes.</span><span class="sxs-lookup"><span data-stu-id="85fda-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="85fda-105">L’exemple suivant montre le format d’un intervalle de date/heure.</span><span class="sxs-lookup"><span data-stu-id="85fda-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="85fda-106">Le tableau suivant répertorie les champs de l’intervalle de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="85fda-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="85fda-107">Champ</span><span class="sxs-lookup"><span data-stu-id="85fda-107">Field</span></span>    | <span data-ttu-id="85fda-108">Description</span><span class="sxs-lookup"><span data-stu-id="85fda-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fda-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="85fda-109">dddddddd</span></span> | <span data-ttu-id="85fda-110">Huit chiffres qui représentent un nombre de jours (00000000 à 99999999).</span><span class="sxs-lookup"><span data-stu-id="85fda-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="85fda-111">HH</span><span class="sxs-lookup"><span data-stu-id="85fda-111">HH</span></span>       | <span data-ttu-id="85fda-112">Heure à deux chiffres de la journée qui utilise l’horloge de 24 heures (00 à 23).</span><span class="sxs-lookup"><span data-stu-id="85fda-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="85fda-113">MM</span><span class="sxs-lookup"><span data-stu-id="85fda-113">MM</span></span>       | <span data-ttu-id="85fda-114">Minutes à deux chiffres dans l’heure (00 à 59).</span><span class="sxs-lookup"><span data-stu-id="85fda-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="85fda-115">SS</span><span class="sxs-lookup"><span data-stu-id="85fda-115">SS</span></span>       | <span data-ttu-id="85fda-116">Nombre de secondes à deux chiffres dans la minute (00 à 59).</span><span class="sxs-lookup"><span data-stu-id="85fda-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="85fda-117">mmmmmm</span><span class="sxs-lookup"><span data-stu-id="85fda-117">mmmmmm</span></span>   | <span data-ttu-id="85fda-118">Nombre de microsecondes de six chiffres dans le deuxième (000000 à 999999).</span><span class="sxs-lookup"><span data-stu-id="85fda-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="85fda-119">Votre implémentation n’est pas requise pour prendre en charge l’évaluation à l’aide de ce champ, mais ce champ doit toujours être présent pour préserver la nature de la chaîne de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="85fda-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="85fda-120">Les intervalles ont toujours un «  : 000 » de fin comme quatre derniers caractères.</span><span class="sxs-lookup"><span data-stu-id="85fda-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="85fda-121">En outre, contrairement à la date et à l’heure, vous ne pouvez pas utiliser d’astérisques pour indiquer les champs inutilisés.</span><span class="sxs-lookup"><span data-stu-id="85fda-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="85fda-122">En outre, toutes les propriétés de [type \_ DateTime DateTime](cim-datetime.md) qui représentent des intervalles doivent être marquées avec le qualificateur standard [SubType](standard-wmi-qualifiers.md) , avec le qualificateur défini sur « Interval ».</span><span class="sxs-lookup"><span data-stu-id="85fda-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="85fda-123">La chaîne suivante représente un intervalle de 1 jour, 12 heures, 0 minute et 32 secondes.</span><span class="sxs-lookup"><span data-stu-id="85fda-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="85fda-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85fda-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85fda-125">Format de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="85fda-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="85fda-126">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="85fda-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="85fda-127">\_DateTime CIM</span><span class="sxs-lookup"><span data-stu-id="85fda-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



