---
title: Chaînes de commande
description: Chaînes de commande
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Chaînes de commande MCI, à propos de
- Chaînes de commande MCI, syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381791"
---
# <a name="command-strings"></a><span data-ttu-id="bfcbe-105">Chaînes de commande</span><span class="sxs-lookup"><span data-stu-id="bfcbe-105">Command Strings</span></span>

<span data-ttu-id="bfcbe-106">Pour envoyer une commande de chaîne à un appareil MCI, utilisez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , qui comprend les paramètres de la commande de chaîne et une mémoire tampon pour toutes les informations retournées.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="bfcbe-107">La fonction **mciSendString** retourne la valeur zéro en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="bfcbe-108">Si la fonction échoue, le mot de poids faible de la valeur de retour contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="bfcbe-109">Vous pouvez transmettre ce code d’erreur à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) pour obtenir une description textuelle de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="bfcbe-110">Syntaxe des chaînes de commande</span><span class="sxs-lookup"><span data-stu-id="bfcbe-110">Syntax of Command Strings</span></span>

<span data-ttu-id="bfcbe-111">Les chaînes de commande MCI utilisent une syntaxe de modificateur Verb-Object-modifier cohérente.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="bfcbe-112">Chaque chaîne de commande comprend une commande, un identificateur d’appareil et des arguments de commande.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="bfcbe-113">Les arguments sont facultatifs pour certaines commandes et requis pour d’autres.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="bfcbe-114">Une chaîne de commande se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="bfcbe-114">A command string has the following form:</span></span>

<span data-ttu-id="bfcbe-115">*arguments de l’ID d’appareil de commande \_*</span><span class="sxs-lookup"><span data-stu-id="bfcbe-115">*command device\_id arguments*</span></span>

<span data-ttu-id="bfcbe-116">Ces composants contiennent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfcbe-116">These components contain the following information:</span></span>

-   <span data-ttu-id="bfcbe-117">La *commande* spécifie une commande MCI, telle que [**ouvrir**](open.md), [**Fermer**](close.md)ou [**lire**](play.md).</span><span class="sxs-lookup"><span data-stu-id="bfcbe-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="bfcbe-118">L' *\_ ID d’appareil* identifie une instance d’un pilote MCI.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="bfcbe-119">L' *\_ ID d’appareil* est créé lors de l’ouverture de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="bfcbe-120">Les *arguments* spécifient les indicateurs et les variables utilisés par la commande.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="bfcbe-121">Les indicateurs sont des mots clés reconnus avec la commande MCI.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="bfcbe-122">Les variables sont des nombres ou des chaînes qui s’appliquent à la commande ou à l’indicateur MCI.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="bfcbe-123">Par exemple, la commande **Play** utilise les arguments « from *position* » et « to *position* » pour indiquer les positions de début et de fin de lecture.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="bfcbe-124">Vous pouvez répertorier les indicateurs utilisés avec une commande dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="bfcbe-125">Quand vous utilisez un indicateur auquel une variable est associée, vous devez fournir une valeur pour la variable.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="bfcbe-126">Les arguments de commande non spécifiés (et facultatifs) supposent une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="bfcbe-127">L’exemple de fonction suivant envoie la commande [**Play**](play.md) avec les indicateurs « from » et « to ».</span><span class="sxs-lookup"><span data-stu-id="bfcbe-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="bfcbe-128">Types de données pour les variables de commande</span><span class="sxs-lookup"><span data-stu-id="bfcbe-128">Data Types for Command Variables</span></span>

<span data-ttu-id="bfcbe-129">Vous pouvez utiliser les types de données suivants pour les variables dans une chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="bfcbe-130">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bfcbe-130">**Data type**</span></span>        | <span data-ttu-id="bfcbe-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="bfcbe-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcbe-132">Chaînes</span><span class="sxs-lookup"><span data-stu-id="bfcbe-132">Strings</span></span>              | <span data-ttu-id="bfcbe-133">Les types de données String sont délimités par des espaces blancs de début et de fin et des guillemets.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="bfcbe-134">MCI supprime les guillemets simples d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="bfcbe-135">Pour placer un guillemet dans une chaîne, utilisez un jeu de deux guillemets où vous souhaitez incorporer votre guillemet.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="bfcbe-136">Pour utiliser une chaîne vide, utilisez deux guillemets séparés par des espaces blancs de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="bfcbe-137">Entiers longs signés</span><span class="sxs-lookup"><span data-stu-id="bfcbe-137">Signed long integers</span></span> | <span data-ttu-id="bfcbe-138">Les types de données entiers longs signés sont délimités par des espaces blancs de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="bfcbe-139">Sauf spécification contraire, les entiers peuvent être positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="bfcbe-140">Si vous utilisez des entiers négatifs, vous ne devez pas séparer le signe moins et le premier chiffre par un espace.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="bfcbe-141">Rectangles</span><span class="sxs-lookup"><span data-stu-id="bfcbe-141">Rectangles</span></span>           | <span data-ttu-id="bfcbe-142">Les types de données de rectangle sont une liste triée de quatre valeurs courtes signées.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="bfcbe-143">L’espace blanc délimite ce type de données et sépare chaque entier dans la liste.</span><span class="sxs-lookup"><span data-stu-id="bfcbe-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 