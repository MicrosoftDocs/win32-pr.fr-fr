---
description: Chaque source d’événement doit inscrire des fichiers de messages contenant des chaînes de description pour chaque identificateur d’événement, catégorie d’événement et paramètre.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Fichiers de messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951408"
---
# <a name="message-files"></a>Fichiers de messages

Chaque [source d’événement](event-sources.md) doit inscrire des fichiers de messages contenant des chaînes de description pour chaque [identificateur d’événement](event-identifiers.md), [catégorie d’événement](event-categories.md)et [paramètre](event-identifiers.md). Inscrivez ces fichiers dans les valeurs de Registre **EventMessageFile**, **CategoryMessageFile** et **ParameterMessageFile** pour la source de l’événement.

Vous pouvez créer un fichier de message qui contient les descriptions des identificateurs d’événements, des catégories et des paramètres, ou créer trois fichiers de message distincts. Les identificateurs de message de tous vos messages doivent être uniques si vous spécifiez les messages dans un ou trois fichiers. Plusieurs applications peuvent partager le même fichier de messages. Pour plus d’informations sur les fichiers de messages, consultez [**compilateur de messages**](/windows/desktop/WES/message-compiler--mc-exe-). Pour plus d’informations sur la syntaxe d’un fichier de message, consultez [fichiers texte du message](message-text-files.md).

## <a name="example-message-file"></a>Exemple de fichier de message

Voici un exemple de fichier de message.

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

L’application d’affichage des événements peut utiliser la procédure suivante pour accéder aux [chaînes de message](event-identifiers.md) dans la dll de message.

**Pour obtenir des chaînes de description**

1.  Appelez la fonction [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) pour ouvrir la source de l’événement.
2.  Appelez la fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) pour obtenir le contenu de la valeur **EventMessageFile** pour la source de l’événement, qui est le nom de la dll du message.
3.  Appelez la fonction [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) pour charger la dll de message déterminée à l’étape 2.
4.  Appelez la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) avec l’identificateur de message pour obtenir la description à partir de la dll. (Notez que les identificateurs de messages sont définis dans le. Fichier H généré par le compilateur de messages.) La fonction **FormatMessage** remplace les chaînes d’insertion à l’aide des valeurs d’argument que vous transmettez, mais elle ne remplace pas les chaînes d’insertion de paramètres. vous devez remplacer les chaînes d’insertion de paramètres vous-même avant d’afficher la chaîne.

 

 
