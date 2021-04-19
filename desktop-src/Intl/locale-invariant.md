---
description: paramètres régionaux \_ INvariants
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513392"
---
# <a name="locale_invariant"></a><span data-ttu-id="ca1f1-103">paramètres régionaux \_ INvariants</span><span class="sxs-lookup"><span data-stu-id="ca1f1-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="ca1f1-104">**Windows XP :** Paramètres régionaux utilisés pour les fonctions au niveau du système d’exploitation qui requièrent des résultats cohérents et indépendants des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="ca1f1-105">Par exemple, les paramètres régionaux indifférent sont utilisés lorsqu’une application compare des chaînes de caractères à l’aide de la fonction [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et attend un résultat cohérent, quels que soient les paramètres régionaux de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="ca1f1-106">Les paramètres des paramètres régionaux invariants sont similaires à ceux de l’anglais (États-Unis), mais ne doivent pas être utilisés pour afficher des données mises en forme.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="ca1f1-107">En règle générale, une application n’utilise pas d' \_ invariant de paramètres régionaux, car elle s’attend à ce que les résultats d’une action dépendent des règles régissant chacun des paramètres régionaux individuels.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="ca1f1-108">La valeur de la \_ variable locale INVARIANT est 0x007F.</span><span class="sxs-lookup"><span data-stu-id="ca1f1-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
