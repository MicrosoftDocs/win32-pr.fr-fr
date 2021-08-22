---
description: Les identificateurs d’événements identifient de manière unique un événement particulier.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificateurs d’événements (journalisation des événements)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951438"
---
# <a name="event-identifiers-event-logging"></a>Identificateurs d’événements (journalisation des événements)

Les identificateurs d’événements identifient de manière unique un événement particulier. Chaque [source d’événement](event-sources.md) peut définir ses propres événements numérotés et les chaînes de description auxquelles elles sont mappées dans son fichier de messages. Les visionneuses d’événements peuvent présenter ces chaînes à l’utilisateur. Ils doivent aider l’utilisateur à comprendre ce qui s’est passé et suggérer les actions à entreprendre. Demandez à la description aux utilisateurs de résoudre leurs propres problèmes, et non aux administrateurs ou aux techniciens du support technique. Pour plus d’informations, consultez [instructions relatives aux messages d’erreur](/windows/desktop/Debug/error-message-guidelines).

## <a name="format"></a>Format

Le diagramme suivant illustre le format d’un identificateur d’événement.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravité
</dt> <dd>

la gravité. La gravité est définie comme suit :

<dl> <dd>00-réussite</dd> <dd>01-informations</dd> <dd>10-AVERTISSEMENT</dd> <dd>11-erreur</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>Secteur
</dt> <dd>

Bit client. Ce bit est défini comme suit :

<dl> <dd>0-code système</dd> <dd>1-code client</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Bit réservé.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Pool
</dt> <dd>

Code d’installation. Cette valeur peut être une valeur \_ null.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Code
</dt> <dd>

Code d’état de la fonctionnalité.

</dd> </dl>

## <a name="message-definitions"></a>Définitions de message

Les messages sont définis dans le fichier de messages d’événements. Les chaînes de description du fichier de messages d’événements sont indexées par identificateur d’événement, ce qui permet à observateur d’événements d’afficher un texte spécifique à l’événement pour tout événement en fonction de l’identificateur d’événement. Toutes les descriptions sont localisées et dépendent de la langue. Pour plus d’informations sur la création d’un fichier de message, consultez [fichiers texte du message](message-text-files.md).

Les chaînes de description peuvent contenir des espaces réservés de chaîne d’insertion, sous la forme%*n*, où %1 indique la première chaîne d’insertion, et ainsi de suite. Par exemple, voici un exemple d’entrée dans le fichier. MC :

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

Dans ce cas, la mémoire tampon retournée par [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contient des chaînes d’insertion. Le membre **NumStrings** de la structure [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indique le nombre de chaînes d’insertion. Le membre **StringOffset** de la structure **EVENTLOGRECORD** indique l’emplacement de la première chaîne d’insertion dans la mémoire tampon. Vous pouvez passer un tableau de \_ PTRS DWORD qui pointent vers l’adresse de chaque chaîne dans la mémoire tampon lors de l’appel de la fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et insèrent les chaînes dans le message.

La chaîne de description peut également contenir des espaces réservés pour les chaînes de paramètres à partir du fichier de messages de paramètres. Les espaces réservés se présentent sous la forme%%*n*, où% %1 est remplacé par la chaîne de paramètre avec l’identificateur 1, et ainsi de suite. Toutefois, il vous revient d’insérer les chaînes de paramètres dans la chaîne de message que [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) retourne. En général, vous appelez **FormatMessage** pour obtenir la chaîne de message de l’événement. Vous analysez ensuite la chaîne de message pour les paramètres%%*n* . Si le message contient un ou plusieurs paramètres, chargez la valeur de Registre **ParameterMessageFile** pour la source. Pour chaque paramètre de la chaîne de message, récupérez l’identificateur et transmettez-le à **FormatMessage** pour obtenir la chaîne de paramètres. Remplacez le paramètre dans la chaîne de message par la chaîne de paramètre renvoyée par **FormatMessage** .

## <a name="insertion-strings"></a>Chaînes d’insertion

Les chaînes d’insertion sont des chaînes facultatives indépendantes du langage utilisées pour remplir les valeurs des espaces réservés dans les chaînes de description. Étant donné que les chaînes ne sont pas localisées, il est essentiel que ces espaces réservés soient utilisés uniquement pour représenter des chaînes indépendantes du langage, telles que des valeurs numériques, des noms de fichiers, des noms d’utilisateur, etc. La longueur de la chaîne ne doit pas dépasser 32 kilo-octets-1 caractères.

Évitez d’utiliser plusieurs chaînes pour créer une description plus grande. Une chaîne d’insertion doit être traitée comme des données, et non du texte. Par exemple, dans l’exemple suivant, pszString1 et pszString2 ne doivent pas être utilisés en tant que chaînes d’insertion pour pszDescription.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

Dans l’exemple suivant, il est approprié d’utiliser soit pszString1, soit pszString2 pour la chaîne d’insertion dans pszDescription.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
