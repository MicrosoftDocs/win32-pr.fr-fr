---
description: Les identificateurs d’événements identifient de manière unique un événement particulier.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificateurs d’événements (journalisation des événements)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527273"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="e19c1-103">Identificateurs d’événements (journalisation des événements)</span><span class="sxs-lookup"><span data-stu-id="e19c1-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="e19c1-104">Les identificateurs d’événements identifient de manière unique un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="e19c1-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="e19c1-105">Chaque [source d’événement](event-sources.md) peut définir ses propres événements numérotés et les chaînes de description auxquelles elles sont mappées dans son fichier de messages.</span><span class="sxs-lookup"><span data-stu-id="e19c1-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="e19c1-106">Les visionneuses d’événements peuvent présenter ces chaînes à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e19c1-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="e19c1-107">Ils doivent aider l’utilisateur à comprendre ce qui s’est passé et suggérer les actions à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="e19c1-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="e19c1-108">Demandez à la description aux utilisateurs de résoudre leurs propres problèmes, et non aux administrateurs ou aux techniciens du support technique.</span><span class="sxs-lookup"><span data-stu-id="e19c1-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="e19c1-109">Pour plus d’informations, consultez [instructions relatives aux messages d’erreur](/windows/desktop/Debug/error-message-guidelines).</span><span class="sxs-lookup"><span data-stu-id="e19c1-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="e19c1-110">Format</span><span class="sxs-lookup"><span data-stu-id="e19c1-110">Format</span></span>

<span data-ttu-id="e19c1-111">Le diagramme suivant illustre le format d’un identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="e19c1-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="e19c1-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravité</span><span class="sxs-lookup"><span data-stu-id="e19c1-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="e19c1-113">la gravité.</span><span class="sxs-lookup"><span data-stu-id="e19c1-113">Severity.</span></span> <span data-ttu-id="e19c1-114">La gravité est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="e19c1-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="e19c1-115">00-réussite</span><span class="sxs-lookup"><span data-stu-id="e19c1-115">00 - Success</span></span></dd> <dd><span data-ttu-id="e19c1-116">01-informations</span><span class="sxs-lookup"><span data-stu-id="e19c1-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="e19c1-117">10-AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="e19c1-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="e19c1-118">11-erreur</span><span class="sxs-lookup"><span data-stu-id="e19c1-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="e19c1-119"><span id="C"></span><span id="c"></span>Secteur</span><span class="sxs-lookup"><span data-stu-id="e19c1-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="e19c1-120">Bit client.</span><span class="sxs-lookup"><span data-stu-id="e19c1-120">Customer bit.</span></span> <span data-ttu-id="e19c1-121">Ce bit est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="e19c1-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="e19c1-122">0-code système</span><span class="sxs-lookup"><span data-stu-id="e19c1-122">0 - System code</span></span></dd> <dd><span data-ttu-id="e19c1-123">1-code client</span><span class="sxs-lookup"><span data-stu-id="e19c1-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="e19c1-124"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="e19c1-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="e19c1-125">Bit réservé.</span><span class="sxs-lookup"><span data-stu-id="e19c1-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="e19c1-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Pool</span><span class="sxs-lookup"><span data-stu-id="e19c1-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="e19c1-127">Code d’installation.</span><span class="sxs-lookup"><span data-stu-id="e19c1-127">Facility code.</span></span> <span data-ttu-id="e19c1-128">Cette valeur peut être une valeur \_ null.</span><span class="sxs-lookup"><span data-stu-id="e19c1-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="e19c1-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="e19c1-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="e19c1-130">Code d’état de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e19c1-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="e19c1-131">Définitions de message</span><span class="sxs-lookup"><span data-stu-id="e19c1-131">Message Definitions</span></span>

<span data-ttu-id="e19c1-132">Les messages sont définis dans le fichier de messages d’événements.</span><span class="sxs-lookup"><span data-stu-id="e19c1-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="e19c1-133">Les chaînes de description du fichier de messages d’événements sont indexées par identificateur d’événement, ce qui permet à observateur d’événements d’afficher un texte spécifique à l’événement pour tout événement en fonction de l’identificateur d’événement.</span><span class="sxs-lookup"><span data-stu-id="e19c1-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="e19c1-134">Toutes les descriptions sont localisées et dépendent de la langue.</span><span class="sxs-lookup"><span data-stu-id="e19c1-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="e19c1-135">Pour plus d’informations sur la création d’un fichier de message, consultez [fichiers texte du message](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="e19c1-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="e19c1-136">Les chaînes de description peuvent contenir des espaces réservés de chaîne d’insertion, sous la forme%*n*, où %1 indique la première chaîne d’insertion, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e19c1-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="e19c1-137">Par exemple, voici un exemple d’entrée dans le fichier. MC :</span><span class="sxs-lookup"><span data-stu-id="e19c1-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="e19c1-138">Dans ce cas, la mémoire tampon retournée par [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contient des chaînes d’insertion.</span><span class="sxs-lookup"><span data-stu-id="e19c1-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="e19c1-139">Le membre **NumStrings** de la structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indique le nombre de chaînes d’insertion.</span><span class="sxs-lookup"><span data-stu-id="e19c1-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="e19c1-140">Le membre **StringOffset** de la structure **EVENTLOGRECORD** indique l’emplacement de la première chaîne d’insertion dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e19c1-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="e19c1-141">Vous pouvez passer un tableau de \_ PTRS DWORD qui pointent vers l’adresse de chaque chaîne dans la mémoire tampon lors de l’appel de la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et insèrent les chaînes dans le message.</span><span class="sxs-lookup"><span data-stu-id="e19c1-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="e19c1-142">La chaîne de description peut également contenir des espaces réservés pour les chaînes de paramètres à partir du fichier de messages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e19c1-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="e19c1-143">Les espaces réservés se présentent sous la forme%%*n*, où% %1 est remplacé par la chaîne de paramètre avec l’identificateur 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e19c1-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="e19c1-144">Toutefois, il vous revient d’insérer les chaînes de paramètres dans la chaîne de message que [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) retourne.</span><span class="sxs-lookup"><span data-stu-id="e19c1-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="e19c1-145">En général, vous appelez **FormatMessage** pour obtenir la chaîne de message de l’événement.</span><span class="sxs-lookup"><span data-stu-id="e19c1-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="e19c1-146">Vous analysez ensuite la chaîne de message pour les paramètres%%*n* .</span><span class="sxs-lookup"><span data-stu-id="e19c1-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="e19c1-147">Si le message contient un ou plusieurs paramètres, chargez la valeur de Registre **ParameterMessageFile** pour la source.</span><span class="sxs-lookup"><span data-stu-id="e19c1-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="e19c1-148">Pour chaque paramètre de la chaîne de message, récupérez l’identificateur et transmettez-le à **FormatMessage** pour obtenir la chaîne de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e19c1-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="e19c1-149">Remplacez le paramètre dans la chaîne de message par la chaîne de paramètre renvoyée par **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="e19c1-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="e19c1-150">Chaînes d’insertion</span><span class="sxs-lookup"><span data-stu-id="e19c1-150">Insertion Strings</span></span>

<span data-ttu-id="e19c1-151">Les chaînes d’insertion sont des chaînes facultatives indépendantes du langage utilisées pour remplir les valeurs des espaces réservés dans les chaînes de description.</span><span class="sxs-lookup"><span data-stu-id="e19c1-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="e19c1-152">Étant donné que les chaînes ne sont pas localisées, il est essentiel que ces espaces réservés soient utilisés uniquement pour représenter des chaînes indépendantes du langage, telles que des valeurs numériques, des noms de fichiers, des noms d’utilisateur, etc.</span><span class="sxs-lookup"><span data-stu-id="e19c1-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="e19c1-153">La longueur de la chaîne ne doit pas dépasser 32 kilo-octets-1 caractères.</span><span class="sxs-lookup"><span data-stu-id="e19c1-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="e19c1-154">Évitez d’utiliser plusieurs chaînes pour créer une description plus grande.</span><span class="sxs-lookup"><span data-stu-id="e19c1-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="e19c1-155">Une chaîne d’insertion doit être traitée comme des données, et non du texte.</span><span class="sxs-lookup"><span data-stu-id="e19c1-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="e19c1-156">Par exemple, dans l’exemple suivant, pszString1 et pszString2 ne doivent pas être utilisés en tant que chaînes d’insertion pour pszDescription.</span><span class="sxs-lookup"><span data-stu-id="e19c1-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="e19c1-157">Dans l’exemple suivant, il est approprié d’utiliser soit pszString1, soit pszString2 pour la chaîne d’insertion dans pszDescription.</span><span class="sxs-lookup"><span data-stu-id="e19c1-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
