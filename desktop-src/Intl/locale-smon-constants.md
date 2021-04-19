---
description: Paramètres régionaux \_ smon \* constantes
ms.assetid: df7f026b-2f2d-420f-8a14-656734409835
title: Constantes LOCALE_SMON *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932888360cc81e08a1cff1f45082b5fc1b91ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516971"
---
# <a name="locale_smon-constants"></a><span data-ttu-id="0f8e9-103">Paramètres régionaux \_ smon \* constantes</span><span class="sxs-lookup"><span data-stu-id="0f8e9-103">LOCALE\_SMON\* Constants</span></span>

<span data-ttu-id="0f8e9-104">Cette rubrique définit les \_ \* constantes smon de paramètres régionaux utilisées par nls pour représenter des valeurs monétaires.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-104">This topic defines the LOCALE\_SMON\* constants used by NLS in representing monetary values.</span></span>



| <span data-ttu-id="0f8e9-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f8e9-105">Value</span></span>                   | <span data-ttu-id="0f8e9-106">Signification</span><span class="sxs-lookup"><span data-stu-id="0f8e9-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8e9-107">paramètres régionaux \_ SMONDECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="0f8e9-107">LOCALE\_SMONDECIMALSEP</span></span>  | <span data-ttu-id="0f8e9-108">Caractère (s) utilisé (s) comme séparateur décimal monétaire.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-108">Character(s) used as the monetary decimal separator.</span></span> <span data-ttu-id="0f8e9-109">Le nombre maximal de caractères autorisés pour cette chaîne est de quatre, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-109">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="0f8e9-110">Par exemple, si un montant monétaire est affiché sous la forme « $3,40 », tout comme « trois dollars et 40 centimes » s’affiche dans le États-Unis, le séparateur décimal monétaire est « . ».</span><span class="sxs-lookup"><span data-stu-id="0f8e9-110">For example, if a monetary amount is displayed as "$3.40", just as "three dollars and forty cents" is displayed in the United States, then the monetary decimal separator is ".".</span></span>                                                                                                                                             |
| <span data-ttu-id="0f8e9-111">paramètres régionaux \_ SMONGROUPING</span><span class="sxs-lookup"><span data-stu-id="0f8e9-111">LOCALE\_SMONGROUPING</span></span>    | <span data-ttu-id="0f8e9-112">Tailles pour chaque groupe de chiffres monétaires à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-112">Sizes for each group of monetary digits to the left of the decimal.</span></span> <span data-ttu-id="0f8e9-113">Le nombre maximal de caractères autorisés pour cette chaîne est dix, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-113">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="0f8e9-114">Une taille explicite est nécessaire pour chaque groupe, et les tailles sont séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-114">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="0f8e9-115">Si la dernière valeur est égale à 0, la valeur précédente est répétée.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-115">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="0f8e9-116">Par exemple, pour regrouper des milliers, spécifiez 3 ; 0.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-116">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="0f8e9-117">Les langues indiennes groupent les premiers mille, puis regroupent par centaines.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-117">Indic languages group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="0f8e9-118">Par exemple, 12, 34, 56789 est représenté par 3 ; 2 ; 0.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-118">For example 12,34,56,789 is represented by 3;2;0.</span></span> |
| <span data-ttu-id="0f8e9-119">paramètres régionaux \_ SMONTHOUSANDSEP</span><span class="sxs-lookup"><span data-stu-id="0f8e9-119">LOCALE\_SMONTHOUSANDSEP</span></span> | <span data-ttu-id="0f8e9-120">Caractère (s) utilisé (s) comme séparateur monétaire entre des groupes de chiffres à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-120">Character(s) used as the monetary separator between groups of digits to the left of the decimal.</span></span> <span data-ttu-id="0f8e9-121">Le nombre maximal de caractères autorisés pour cette chaîne est de quatre, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-121">The maximum number of characters allowed for this string is four, including a terminating null character.</span></span> <span data-ttu-id="0f8e9-122">En règle générale, les groupes représentent des milliers.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-122">Typically, the groups represent thousands.</span></span> <span data-ttu-id="0f8e9-123">Toutefois, en fonction de la valeur spécifiée pour les paramètres régionaux \_ SMONGROUPING, ils peuvent représenter autre chose.</span><span class="sxs-lookup"><span data-stu-id="0f8e9-123">However, depending on the value specified for LOCALE\_SMONGROUPING, they can represent something else.</span></span>                                                                                                                                 |



 

 

 



