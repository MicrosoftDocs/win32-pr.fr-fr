---
title: Chaînes MOF
description: Une chaîne est un type de données qui contient une chaîne de caractères généralement conçue comme du texte explicite.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863794"
---
# <a name="mof-strings"></a><span data-ttu-id="7d588-103">Chaînes MOF</span><span class="sxs-lookup"><span data-stu-id="7d588-103">MOF strings</span></span>

<span data-ttu-id="7d588-104">Une chaîne est un type de données qui contient une chaîne de caractères généralement conçue comme du texte explicite.</span><span class="sxs-lookup"><span data-stu-id="7d588-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="7d588-105">MOF décrit deux types de chaînes, qui utilisent pour contenir un ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="7d588-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="7d588-106">MOF comporte également une série de règles qui décrivent l’utilisation de guillemets dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="7d588-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="7d588-107">Le tableau suivant répertorie les types de données de chaîne pour MOF.</span><span class="sxs-lookup"><span data-stu-id="7d588-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="7d588-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="7d588-108">Data type</span></span>  | <span data-ttu-id="7d588-109">Type Automation</span><span class="sxs-lookup"><span data-stu-id="7d588-109">Automation type</span></span> | <span data-ttu-id="7d588-110">Description</span><span class="sxs-lookup"><span data-stu-id="7d588-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d588-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="7d588-111">**char16**</span></span> | <span data-ttu-id="7d588-112">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="7d588-112">**VT\_I2**</span></span>      | <span data-ttu-id="7d588-113">Caractère Unicode 16 bits unique au format UCS-2 (Universal Character Set 2)</span><span class="sxs-lookup"><span data-stu-id="7d588-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="7d588-114">**string**</span><span class="sxs-lookup"><span data-stu-id="7d588-114">**string**</span></span> | <span data-ttu-id="7d588-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7d588-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="7d588-116">Chaîne de caractères Unicode</span><span class="sxs-lookup"><span data-stu-id="7d588-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="7d588-117">Pour écrire des chaînes pour MOF, suivez les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d588-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="7d588-118">Entourez les constantes à un caractère avec des guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="7d588-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="7d588-119">Si vous n’utilisez pas de guillemets simples avec des constantes à caractère unique, vous devez utiliser la représentation entière de la valeur du caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d588-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="7d588-120">Si vous le souhaitez, vous pouvez spécifier le caractère littéralement avec la \\ séquence d’échappement x du American National Standards Institute (ANSI) C standard, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7d588-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="7d588-121">Comme MOF est basé sur Unicode, vous pouvez également spécifier des valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d588-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="7d588-122">Sachez que les constantes à caractère unique au format ANSI C sont entourées de guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="7d588-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="7d588-123">Entourez les chaînes de caractères avec des guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="7d588-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="7d588-124">Concaténer des chaînes de guillemets successifs avec un ou plusieurs espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="7d588-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="7d588-125">Utilisez une séquence d’échappement commençant par une barre oblique inverse pour incorporer des guillemets dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="7d588-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="7d588-126">L’exemple suivant décrit comment initialiser des propriétés de chaîne et un paramètre de chaîne :</span><span class="sxs-lookup"><span data-stu-id="7d588-126">The following example describes how to initialize string properties and a string parameter:</span></span>

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




