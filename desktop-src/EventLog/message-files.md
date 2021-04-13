---
description: Chaque source d’événement doit inscrire des fichiers de messages contenant des chaînes de description pour chaque identificateur d’événement, catégorie d’événement et paramètre.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Fichiers de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528744"
---
# <a name="message-files"></a><span data-ttu-id="cd599-103">Fichiers de messages</span><span class="sxs-lookup"><span data-stu-id="cd599-103">Message Files</span></span>

<span data-ttu-id="cd599-104">Chaque [source d’événement](event-sources.md) doit inscrire des fichiers de messages contenant des chaînes de description pour chaque [identificateur d’événement](event-identifiers.md), [catégorie d’événement](event-categories.md)et [paramètre](event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="cd599-104">Each [event source](event-sources.md) should register message files that contain description strings for each [event identifier](event-identifiers.md), [event category](event-categories.md), and [parameter](event-identifiers.md).</span></span> <span data-ttu-id="cd599-105">Inscrivez ces fichiers dans les valeurs de Registre **EventMessageFile**, **CategoryMessageFile** et **ParameterMessageFile** pour la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="cd599-105">Register these files in the **EventMessageFile**, **CategoryMessageFile**, and **ParameterMessageFile** registry values for the event source.</span></span>

<span data-ttu-id="cd599-106">Vous pouvez créer un fichier de message qui contient les descriptions des identificateurs d’événements, des catégories et des paramètres, ou créer trois fichiers de message distincts.</span><span class="sxs-lookup"><span data-stu-id="cd599-106">You can create one message file that contains descriptions for the event identifiers, categories, and parameters, or create three separate message files.</span></span> <span data-ttu-id="cd599-107">Les identificateurs de message de tous vos messages doivent être uniques si vous spécifiez les messages dans un ou trois fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd599-107">The message identifiers for all of your messages should be unique whether you specify the messages in one file or three files.</span></span> <span data-ttu-id="cd599-108">Plusieurs applications peuvent partager le même fichier de messages.</span><span class="sxs-lookup"><span data-stu-id="cd599-108">Several applications can share the same message file.</span></span> <span data-ttu-id="cd599-109">Pour plus d’informations sur les fichiers de messages, consultez [**compilateur de messages**](/windows/desktop/WES/message-compiler--mc-exe-).</span><span class="sxs-lookup"><span data-stu-id="cd599-109">For more information on message files, see [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span></span> <span data-ttu-id="cd599-110">Pour plus d’informations sur la syntaxe d’un fichier de message, consultez [fichiers texte du message](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="cd599-110">For details on the syntax of a message file, see [Message Text Files](message-text-files.md).</span></span>

## <a name="example-message-file"></a><span data-ttu-id="cd599-111">Exemple de fichier de message</span><span class="sxs-lookup"><span data-stu-id="cd599-111">Example Message File</span></span>

<span data-ttu-id="cd599-112">Voici un exemple de fichier de message.</span><span class="sxs-lookup"><span data-stu-id="cd599-112">The following is an example message file.</span></span>

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

<span data-ttu-id="cd599-113">L’application d’affichage des événements peut utiliser la procédure suivante pour accéder aux [chaînes de message](event-identifiers.md) dans la dll de message.</span><span class="sxs-lookup"><span data-stu-id="cd599-113">The event-viewing application can use the following procedure to gain access to the [message strings](event-identifiers.md) in the message DLL.</span></span>

<span data-ttu-id="cd599-114">**Pour obtenir des chaînes de description**</span><span class="sxs-lookup"><span data-stu-id="cd599-114">**To obtain description strings**</span></span>

1.  <span data-ttu-id="cd599-115">Appelez la fonction [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) pour ouvrir la source de l’événement.</span><span class="sxs-lookup"><span data-stu-id="cd599-115">Call the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function to open the event source.</span></span>
2.  <span data-ttu-id="cd599-116">Appelez la fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) pour obtenir le contenu de la valeur **EventMessageFile** pour la source de l’événement, qui est le nom de la dll du message.</span><span class="sxs-lookup"><span data-stu-id="cd599-116">Call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function to obtain the contents of the **EventMessageFile** value for the event source, which is the name of the message DLL.</span></span>
3.  <span data-ttu-id="cd599-117">Appelez la fonction [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pour charger la dll de message déterminée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="cd599-117">Call the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message DLL determined by step 2.</span></span>
4.  <span data-ttu-id="cd599-118">Appelez la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) avec l’identificateur de message pour obtenir la description à partir de la dll.</span><span class="sxs-lookup"><span data-stu-id="cd599-118">Call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the message identifier to obtain the description from the DLL.</span></span> <span data-ttu-id="cd599-119">(Notez que les identificateurs de messages sont définis dans le. Fichier H généré par le compilateur de messages.) La fonction **FormatMessage** remplace les chaînes d’insertion à l’aide des valeurs d’argument que vous transmettez, mais elle ne remplace pas les chaînes d’insertion de paramètres. vous devez remplacer les chaînes d’insertion de paramètres vous-même avant d’afficher la chaîne.</span><span class="sxs-lookup"><span data-stu-id="cd599-119">(Note that the messages identifiers are defined in the .H file generated by the message compiler.) The **FormatMessage** function will replace the insertion strings using the argument values that you pass but it will not replace the parameter insertion strings; you must replace the parameter insertion strings yourself before displaying the string.</span></span>

 

 
