---
description: L’exemple de fichier de message suivant montre comment créer et utiliser un fichier texte de message qui définit des messages dans plusieurs langues.
ms.assetid: 403eaccc-07a3-4368-a39a-18c706c65537
title: Exemple de fichier texte de message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e4247b1e39ef94c006262f282d8d830af11851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525008"
---
# <a name="sample-message-text-file"></a><span data-ttu-id="2222a-103">Exemple de fichier texte de message</span><span class="sxs-lookup"><span data-stu-id="2222a-103">Sample Message Text File</span></span>

<span data-ttu-id="2222a-104">L’exemple de fichier de message suivant montre comment créer et utiliser un fichier texte de message qui définit des messages dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="2222a-104">The following sample message file shows how to create and use a message text file that defines messages in multiple languages.</span></span>

## <a name="sample-message-file"></a><span data-ttu-id="2222a-105">Exemple de fichier de message</span><span class="sxs-lookup"><span data-stu-id="2222a-105">Sample Message File</span></span>

<span data-ttu-id="2222a-106">Cet exemple de fichier de message, Sample.mc, contient un bloc de commentaires, suivi d’une section d’en-tête, suivi de messages en deux langues.</span><span class="sxs-lookup"><span data-stu-id="2222a-106">This sample message file, Sample.mc, contains a comment block, followed by a header section, followed by messages in two languages.</span></span> <span data-ttu-id="2222a-107">Vous devez utiliser un éditeur compatible Unicode pour prendre en charge simultanément les caractères utilisés dans différents langages écrits.</span><span class="sxs-lookup"><span data-stu-id="2222a-107">You must use a Unicode-compatible editor to simultaneously support the characters used in different written languages.</span></span> <span data-ttu-id="2222a-108">Pour plus d’informations et pour obtenir une description détaillée de la syntaxe des fichiers. MC, consultez [fichiers texte des messages](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="2222a-108">For more information and a detailed description of the syntax of .mc files, see [Message Text Files](message-text-files.md).</span></span>

``` syntax
; // ***** Sample.mc *****
; // This is the header section.

MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
Warning=0x2:STATUS_SEVERITY_WARNING
Error=0x3:STATUS_SEVERITY_ERROR
)

FacilityNames=(System=0x0:FACILITY_SYSTEM
Runtime=0x2:FACILITY_RUNTIME
Stubs=0x3:FACILITY_STUBS
Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)
LanguageNames=(Japanese=0x411:MSG00411)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x2
Severity=Warning
Facility=Io
SymbolicName=MSG_BAD_PARM1
Language=English
Cannot reconnect to the server.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x3
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2 which is in error.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x5
Severity=Informational
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1!d! attempts with %2!d!%% success%! Disconnect from 
the server and try again later.
.

Language=Japanese
<Japanese message string goes here>
.
```

 

 



