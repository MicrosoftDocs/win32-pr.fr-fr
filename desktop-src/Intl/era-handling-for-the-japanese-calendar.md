---
description: Gestion d’ères pour le calendrier japonais
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gestion d’ères pour le calendrier japonais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867926"
---
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="ca67d-103">Gestion d’ères pour le calendrier japonais</span><span class="sxs-lookup"><span data-stu-id="ca67d-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="ca67d-104">De nombreux calendriers ont des ères, comme AD/BC ou CE/BCE.</span><span class="sxs-lookup"><span data-stu-id="ca67d-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="ca67d-105">Dans le calendrier japonais, les années sont décrites par nengō, une combinaison du numéro d’année et du nom de l’ère.</span><span class="sxs-lookup"><span data-stu-id="ca67d-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="ca67d-106">Par exemple, 2009 est Heisei 21.</span><span class="sxs-lookup"><span data-stu-id="ca67d-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="ca67d-107">Dans le passé, les noms des ères Japonais changent fréquemment, mais à présent, la modification du japonais ne change que sur la succession du impérial.</span><span class="sxs-lookup"><span data-stu-id="ca67d-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="ca67d-108">Windows et Microsoft .NET ont pris en charge historiquement les quatre ères modernes dans le cadre de cette stratégie : Meiji, Taishō, Shōwa et Heisei.</span><span class="sxs-lookup"><span data-stu-id="ca67d-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="ca67d-109">Avec Windows 7, Windows Server 2008 R2 et le .NET Framework 4, Microsoft reconnaît que des ères supplémentaires peuvent être ajoutées à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ca67d-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="ca67d-110">Sur ces versions de Windows, les données de l’ère sont stockées dans le Registre sous la clé :</span><span class="sxs-lookup"><span data-stu-id="ca67d-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="ca67d-111">HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ les \\ calendriers nls \\ japonais \\ ères</span><span class="sxs-lookup"><span data-stu-id="ca67d-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="ca67d-112">Si nécessaire, des ères supplémentaires peuvent être ajoutées à cette clé par le biais du processus de Windows Update normal.</span><span class="sxs-lookup"><span data-stu-id="ca67d-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="ca67d-113">Cette clé peut être affichée à l’aide de l’éditeur du Registre (Regedit.exe).</span><span class="sxs-lookup"><span data-stu-id="ca67d-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="ca67d-114">Voici un exemple de la clé et des valeurs fournies dans Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="ca67d-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="ca67d-115">Le nom de chaque valeur d’ère correspond à la date de début de l’ère dans le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="ca67d-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="ca67d-116">La valeur contient le nom de l’ère en japonais, le nom abrégé en japonais, le nom en anglais et un nom abrégé en anglais :</span><span class="sxs-lookup"><span data-stu-id="ca67d-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="ca67d-117">« YYYY MM JJ » = « JE \_ AJE \_ EE \_ AEE »</span><span class="sxs-lookup"><span data-stu-id="ca67d-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="ca67d-118">« YYYY MM JJ » est la date grégorienne du début de l’ère dans l’année, le mois, le formulaire de jour où Year est 4 chiffres, Day est 2 chiffres et month est également 2 chiffres.</span><span class="sxs-lookup"><span data-stu-id="ca67d-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="ca67d-119">Un espace sépare chaque partie de la date.</span><span class="sxs-lookup"><span data-stu-id="ca67d-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="ca67d-120">« JE suis » est le nom japonais de l’ère et est suivi d’un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ca67d-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="ca67d-121">« AJE » est le nom abrégé de l’ère, en japonais, et est suivi d’un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ca67d-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="ca67d-122">« EE » est le nom anglais de l’ère japonaise et est suivi d’un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ca67d-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="ca67d-123">« AEE » est le nom anglais abrégé de l’ère japonaise.</span><span class="sxs-lookup"><span data-stu-id="ca67d-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="ca67d-124">L’un des points à prendre en compte pour les développeurs d’applications est la possibilité que des ères supplémentaires soient ajoutées par Windows Update ou d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="ca67d-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="ca67d-125">Dans ce cas, l’application peut rencontrer plus que les quatre ères attendues pour le calendrier japonais.</span><span class="sxs-lookup"><span data-stu-id="ca67d-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="ca67d-126">À des fins de test, les testeurs peuvent ajouter une ère supplémentaire au registre ; Toutefois, cela doit être limité aux ordinateurs de test uniquement, car il affecte le comportement de l’ordinateur entier.</span><span class="sxs-lookup"><span data-stu-id="ca67d-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="ca67d-127">Voici un exemple d’une telle clé qui peut être utilisée pour le test.</span><span class="sxs-lookup"><span data-stu-id="ca67d-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="ca67d-128">Cette modification peut être effectuée à l’aide de l’éditeur du Registre.</span><span class="sxs-lookup"><span data-stu-id="ca67d-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="ca67d-129">(Il s’agit d’un exemple pour une utilisation de test uniquement et n’est pas destiné à prédire les ajouts ultérieurs.)</span><span class="sxs-lookup"><span data-stu-id="ca67d-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="ca67d-130">Notez que cela affecte uniquement les ordinateurs qui exécutent Windows 7 et versions ultérieures ou .NET Framework 4 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ca67d-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="ca67d-131">Les développeurs d’applications sont encouragés à tester leurs applications avec des ères de test supplémentaires pour s’assurer que leurs applications continuent de fonctionner si des ères supplémentaires sont ajoutées à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ca67d-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca67d-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca67d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca67d-133">Récupération des informations de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="ca67d-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="ca67d-134">Identificateurs de calendrier</span><span class="sxs-lookup"><span data-stu-id="ca67d-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



