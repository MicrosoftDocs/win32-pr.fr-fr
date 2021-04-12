---
description: Vous pouvez localiser des propriétés statiques à l’aide de mappages de valeurs partielles.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localiser des propriétés statiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323442"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="2f840-103">Localiser des propriétés statiques</span><span class="sxs-lookup"><span data-stu-id="2f840-103">Localizing Static Properties</span></span>

<span data-ttu-id="2f840-104">Vous pouvez localiser des propriétés statiques à l’aide de mappages de valeurs partielles.</span><span class="sxs-lookup"><span data-stu-id="2f840-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="2f840-105">La procédure suivante décrit comment les propriétés statiques peuvent être localisées à l’aide de mappages de valeurs partielles avec des expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="2f840-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="2f840-106">**Pour utiliser des mappages de valeurs afin de localiser des propriétés statiques**</span><span class="sxs-lookup"><span data-stu-id="2f840-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="2f840-107">Créez un fichier MOF maître (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="2f840-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="2f840-108">L’exemple de code suivant peut être utilisé pour créer un fichier MOF maître (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="2f840-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="2f840-109">Créez les versions indépendantes de la langue et spécifiques à la langue du fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="2f840-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="2f840-110">Tapez la commande suivante à l’invite de commandes pour créer les versions indépendantes de la langue et de la langue du fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="2f840-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="2f840-111">Le compilateur MOF génère les fichiers MOF propres au langage et aux langages, LnVm. mof et LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="2f840-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="2f840-112">Les valeurs de l’anglais américain pour la propriété [numbers](numbers.md) sont placées dans le fichier. MFL pour l’espace de noms anglais américain.</span><span class="sxs-lookup"><span data-stu-id="2f840-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="2f840-113">L’exemple de code suivant affiche le contenu du fichier LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="2f840-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="2f840-114">Compilez les deux fichiers MOF et stockez les informations de classe dans le référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="2f840-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="2f840-115">Tapez la commande suivante à l’invite de commandes pour compiler les deux fichiers MOF.</span><span class="sxs-lookup"><span data-stu-id="2f840-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="2f840-116">Localisez le fichier MFL pour d’autres paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2f840-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="2f840-117">L’exemple de code suivant montre le contenu d’un fichier MFL pour l’espace de noms français.</span><span class="sxs-lookup"><span data-stu-id="2f840-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="2f840-118">Le résultat net est que le nom d’affichage et la valeur de la propriété [numbers](numbers.md) dépendent des paramètres régionaux de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="2f840-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="2f840-119">Si l’utilisateur spécifie des paramètres régionaux qui n’ont pas été fournis, les données de qualificateur par défaut proviennent de l’espace de noms anglais (MS \_ 409).</span><span class="sxs-lookup"><span data-stu-id="2f840-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="2f840-120">L’implication de cette conception est que chaque valeur de chaîne est utilisée comme identificateur de recherche, qui ne peut pas être localisé.</span><span class="sxs-lookup"><span data-stu-id="2f840-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="2f840-121">Lorsque vous définissez ce schéma, vous devez vous assurer que la valeur que le fournisseur place dans est indépendante des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2f840-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="2f840-122">WMI ne fournit pas actuellement la prise en charge au moment de l’exécution pour le mappage des valeurs aux chaînes définies par les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="2f840-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="2f840-123">L’interprétation de la syntaxe suggérée est la responsabilité de l’application.</span><span class="sxs-lookup"><span data-stu-id="2f840-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



