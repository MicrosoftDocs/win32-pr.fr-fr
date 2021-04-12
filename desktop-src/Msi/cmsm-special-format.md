---
description: Certaines valeurs utilisées avec les modules de fusion configurables nécessitent une gestion de texte spéciale.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Format spécial CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202202"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="c29df-103">Format spécial CMSM</span><span class="sxs-lookup"><span data-stu-id="c29df-103">CMSM Special Format</span></span>

<span data-ttu-id="c29df-104">Certaines valeurs utilisées avec les modules de fusion configurables nécessitent une gestion de texte spéciale.</span><span class="sxs-lookup"><span data-stu-id="c29df-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="c29df-105">Une chaîne de texte décrite comme étant dans « CMSM Special format » traite le point-virgule (;) et est égal à (=) caractères comme caractères réservés utilisés par l’outil de fusion du client ou Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="c29df-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="c29df-106">Le format spécial CMSM est actuellement utilisé aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="c29df-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="c29df-107">Colonne de ligne de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="c29df-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="c29df-108">Colonne de valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="c29df-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="c29df-109">La colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque le champ de valeurs par champ est la valeur dans la colonne format.</span><span class="sxs-lookup"><span data-stu-id="c29df-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="c29df-110">La colonne ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque Text est la valeur dans la colonne format et enum est la valeur dans la colonne Type.</span><span class="sxs-lookup"><span data-stu-id="c29df-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="c29df-111">Colonne DefaultValue de la [table ModuleConfiguration](moduleconfiguration-table.md) lorsque key est la valeur de la colonne format.</span><span class="sxs-lookup"><span data-stu-id="c29df-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="c29df-112">Éléments configurables dans le format de clé utilisé par la [**méthode ProvideTextData**](configuremodule-providetextdata.md).</span><span class="sxs-lookup"><span data-stu-id="c29df-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="c29df-113">Pour entrer des points-virgules littéraux ou des caractères équivalents dans une valeur au format spécial CMSM, faites précéder le caractère d’une barre oblique inverse (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="c29df-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="c29df-114">Une barre oblique inverse littérale peut être représentée par deux barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="c29df-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="c29df-115">Un caractère unique préfixé par une barre oblique inverse unique est converti en caractère unique, même si l’échappement du caractère n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c29df-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="c29df-116">Si un point-virgule ou un caractère égal n’est pas précédé d’une barre oblique inverse mais qu’il n’a pas encore de comportement défini dans le contexte de la valeur, la chaîne résultante n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c29df-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="c29df-117">Par exemple, la colonne DefaultValue de la table ModuleConfiguration est au format spécial CMSM pour tous les éléments clés, car le point-virgule est le délimiteur de colonne.</span><span class="sxs-lookup"><span data-stu-id="c29df-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="c29df-118">Bien que le caractère égal n’ait aucune signification particulière dans cette chaîne, les caractères littéraux doivent toujours être placés dans une séquence d’échappement dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="c29df-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



