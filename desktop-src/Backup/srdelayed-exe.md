---
title: Srdelayed.exe
description: Les applications qui effectuent des opérations de restauration de l’état du système au début du démarrage du système d’exploitation peuvent ne pas pouvoir utiliser les fonctions de gestion de fichiers pour déplacer, supprimer ou définir le nom abrégé de certains fichiers système.
ms.assetid: cedeb48e-bc1d-48d1-9bee-0b8b0132c3e5
keywords:
- Sauvegarde Srdelayed.exe
- Sauvegarde de récupération de l’état du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdf95ff77fd17a578b85e6037c71146666eae9522d066bc1c4629fb9a2c24e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835537"
---
# <a name="srdelayedexe"></a>Srdelayed.exe

Les applications qui effectuent des opérations de restauration de l’état du système au début du démarrage du système d’exploitation peuvent ne pas pouvoir utiliser les fonctions de gestion de fichiers pour déplacer, supprimer ou définir le nom abrégé de certains fichiers système. Srdelayed.exe est un fichier exécutable, fourni avec la fonctionnalité de Sauvegarde Windows Server (WSB) dans Windows Server 2008, qui peut permettre aux applications de récupération de l’état du système de déplacer, supprimer et définir le nom abrégé des fichiers système.

L’outil srdelayed est conçu pour les applications de récupération de l’état du système. elle ne remplace pas les fonctions de gestion de fichiers. Cet outil doit être utilisé uniquement lorsque l’application ne peut pas déplacer, supprimer ou définir le nom abrégé d’un fichier système à l’aide des fonctions [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa), [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)et [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea) . Pendant une restauration et un redémarrage de l’état du système, Srdelayed.exe est utilisé par la restauration du système et l’outil de ligne de commande wbadmin.exe pour déplacer, supprimer et définir le nom abrégé de certains fichiers système. Srdelayed peut donc être utile pour les développeurs qui requièrent la possibilité de restaurer ces fichiers système dans leurs propres applications de récupération de l’état du système.

Srdelayed peut effectuer les opérations suivantes :

-   Opération de déplacement de fichier similaire à la fonction [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) avec **le \_ délai MOVEFILE jusqu’à l’indicateur de \_ \_ redémarrage**
-   Opération de suppression de fichier similaire à la fonction [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea)
-   Une opération set Short Name similaire à la fonction [**SetFileShortName**](/windows/desktop/api/winbase/nf-winbase-setfileshortnamea)

Pour utiliser srdelayed, votre application nécessite le chemin d’accès complet à l’emplacement du fichier Srdelayed.exe et le chemin d’accès complet à un fichier texte Unicode que vous avez créé pour contenir les informations nécessaires à l’outil pour effectuer toutes les opérations de gestion de fichiers demandées. Votre application est chargée de s’assurer que ce fichier texte ne contient pas de demandes redondantes pour une opération et qu’il gère tout ordonnancement des opérations de gestion des fichiers. Par exemple, étant donné qu’un dossier doit être vide pour être supprimé, votre application doit s’assurer que le fichier texte spécifie la suppression de tous les fichiers contenus dans le dossier avant de demander la suppression du dossier.

Si l’entrée **SetupExecute** n’existe pas encore dans le registre, votre application doit créer une entrée de type **reg \_ \_ multisz** nommée **SetupExecute** sous la clé de Registre suivante : **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager**.

Votre application doit utiliser le format suivant pour définir la valeur de **SetupExecute** sur le chemin d’accès complet à l’emplacement du fichier Srdelayed.exe et le chemin d’accès complet à l’emplacement du fichier texte. Préfixe « \\ \\ ?? \\ » pour le chemin d’accès du fichier texte, comme suit :

*Chemin d’accès complet à Srdelayed.exe* \\ \\ ? \\ *Chemin d’accès complet au fichier texte*  


Par exemple, la valeur suivante pour **SetupExecute** indique que le Srdelayed.exe se trouve dans le dossier system32 et que le fichier texte est nommé DelayedOperations :

C : \\ Windows \\ System32 \\srdelayed.exe \\ \\ ?? \\ C : \\ temp \\ DelayedOperations  


Les espaces dans le chemin d’accès et le nom doivent être encodés au format hexadécimal. Par exemple, pour les *fichiers programme*, encodez le chemin d’accès en tant que « \\ \\ ?? \\ C :Program%20Files \\a.dll».

Lorsque le registre ou le système est restauré lors du redémarrage, votre application doit s’assurer que **SetupExecute** est écrit dans la ruche de Registre correcte. La récupération du Registre est effectuée avant l’exécution de Srdelayed.exe. L’application doit écrire des **SetupExecute** dans la version Récupérée du Registre, car il s’agit de la version qui est lue.

## <a name="format-for-the-srdelayed-input-file"></a>Format du fichier d’entrée srdelayed

Toutes les informations dont srdelayed a besoin pour effectuer des opérations de gestion de fichiers sont spécifiées sous la forme d’une chaîne de caractères Unicode dans un fichier texte Unicode. La chaîne de caractères Unicode est partitionnée en enregistrements qui sont eux-mêmes chacun partitionnés en quatre champs. Chaque enregistrement spécifie un fichier de déplacement unique, un fichier de suppression ou une opération de définition de nom abrégé. Les quatre champs de chaque enregistrement contiennent les paramètres de l’opération. Srdelayed.exe effectue chaque opération dans l’ordre dans lequel leurs enregistrements se produisent dans la chaîne. Votre application doit rechercher les enregistrements en double dans ce fichier et supprimer les doublons.

La chaîne suivante illustre le format d’un fichier demandant deux opérations et composé de deux enregistrements. Chaque champ de paramètre se termine par un seul caractère L' \\ 0 '. Un enregistrement est composé de quatre champs consécutifs. Un seul caractère de L' ' \\ 0 'supplémentaire est ajouté à la fin de tous les enregistrements.

`<ParamA1>L'\0'<ParamA2>L'\0'<ParamA3>L'\0'<ParamA4>L'\0'<ParamB1>L'\0'<ParamB2>L'\0'<ParamB3>L'\0'<ParamB4>L'\0'L'\0'`  
`|-----------------------RecordA------------------------|------------------------RecordB------------------------|`  


La signification des premier, deuxième, troisième et quatrième champs de paramètre varie selon que l’enregistrement décrit une opération de déplacement, de suppression ou de définition de noms courts.

## <a name="format-for-a-move-file-record"></a>Format pour un enregistrement de fichier de déplacement

Le champ 1 identifie cela comme une demande de déplacement d’un fichier. La valeur de ce champ est toujours L "MoveFile" et respecte la casse.

Le champ 2 spécifie l’emplacement source du fichier. L’opération de déplacement de fichier srdelayed ne prend pas en charge le déplacement d’un dossier. Un fichier doit être spécifié dans ce champ. La valeur de ce champ est le chemin d’accès complet du fichier ajouté à « \\ \\ ?? \\ », sauf si le chemin d’accès contient un identificateur global unique (Guid) qui utilise « \\ \\ ? \\ » comme préfixe. Supprimez « \\ \\ ? \\ » avant d’ajouter à « \\ \\ ?? \\ ».

Le champ 3 spécifie la destination du fichier. L’opération de déplacement de fichier fonctionne uniquement dans un volume. La source et la destination doivent se trouver sur le même volume. La valeur de ce champ est le chemin d’accès complet du fichier ajouté à « \\ \\ ?? \\ », sauf si le chemin d’accès contient un identificateur global unique (Guid) qui utilise « \\ \\ ? \\ » comme préfixe. Supprimez « \\ \\ ? \\ » avant d’ajouter à « \\ \\ ?? \\ ».

Le champ 4 reçoit les informations d’état de srdelayed. La valeur de ce champ doit être définie sur L "NotExecuted" pour un nouvel enregistrement.

L’exemple suivant référence le fichier par chemin d’accès de lecteur. Si le chemin d’accès et le nom de la source sont C : \\ Stage \\a.dll, cet enregistrement demande que srdelayed le déplace vers C : \\ temp \\a.dll.

MoveFile \\ \\ ?? \\ C : \\ étape \\a.dll \\ \\ ?? \\ C : \\ temp \\a.dll NotExecuted  


L’exemple suivant fait référence au fichier par le chemin d’accès du GUID de volume. Si le chemin d’accès et le nom de la source sont \\ \\ ? \\ Le volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ Stage \\a.dll, ces demandes d’enregistrement que srdelayed le déplacer vers \\ \\ ? \\a.dll du volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\

 MoveFile \\ \\ ?? \\ Le volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ Stage \\a.dll \\ \\ ?? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\a.dll NotExecuted  


## <a name="format-for-a-delete-file-record"></a>Format pour un enregistrement de fichier de suppression

Le champ 1 identifie cela comme une demande de suppression d’un fichier. La valeur de ce champ est toujours L "DeleteFile" et respecte la casse.

Le champ 2 n’est pas utilisé. La valeur de ce champ doit être définie sur L "non utilisé".

Le champ 3 spécifie le fichier à supprimer. Un dossier doit être vide pour pouvoir être supprimé. Utilisez supprimer les opérations de fichier pour supprimer tous les fichiers du dossier avant de supprimer le dossier. La valeur de ce champ est le chemin d’accès complet du fichier ajouté à « \\ \\ ?? \\ », sauf si le chemin d’accès contient un identificateur global unique (Guid) qui utilise « \\ \\ ? \\ » comme préfixe. Supprimez « \\ \\ ? \\ » avant d’ajouter à « \\ \\ ?? \\ ».

Le champ 4 reçoit les informations d’état de srdelayed. La valeur de ce champ doit être définie sur L "NotExecuted" pour un nouvel enregistrement.

L’exemple suivant référence le fichier par chemin d’accès de lecteur. Si le chemin d’accès et le nom sont C : \\ temp \\b.dll, cet enregistrement demande que srdelayed supprime le fichier.

DeleteFile inutilisé \\ \\ ?? \\ C : \\ temp \\b.dll NotExecuted  


L’exemple suivant fait référence au fichier par GUID de volume. Si le chemin d’accès et le nom sont \\ \\ ? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\b.dll, cet enregistrement demande que srdelayed supprime le fichier.

DeleteFile inutilisé \\ \\ ?? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\b.dll\\ NotExecuted  


## <a name="format-for-set-short-name-record"></a>Format de l’enregistrement de Short-Name défini

Le champ 1 identifie cela comme une demande de définition du nom abrégé d’un fichier. La valeur de ce champ est toujours L « SetFileShortName » et respecte la casse.

Le champ 2 spécifie le nom abrégé.

Champ champ 3 spécifie le chemin d’accès et le nom long pour recevoir le nom abrégé. La valeur de ce champ est le chemin d’accès et le nom long du fichier ajouté à « \\ \\ ?? \\ », sauf si le chemin d’accès contient un identificateur global unique (Guid) qui utilise « \\ \\ ? \\ » comme préfixe. Supprimez « \\ \\ ? \\ » avant d’ajouter à « \\ \\ ?? \\ ».

Le champ 4 reçoit les informations d’état de srdelayed. La valeur de ce champ doit être définie sur L "NotExecuted" pour un nouvel enregistrement.

L’exemple suivant référence le fichier par chemin d’accès de lecteur. Si le chemin d’accès et le nom du fichier sont C : \\ temp \\ShortFileName.dll, cet enregistrement demande que le fichier reçoive un nom abrégé, shortn ~1.dll.

SetFileShortName shortn ~1.dll \\ \\ ?? \\ C : \\ temp \\ShortFileName.dll NotExecuted  


L’exemple suivant fait référence au fichier par GUID de volume. Si le chemin d’accès et le nom du fichier sont \\ \\ ? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ , cet enregistrement demande que le fichier reçoive un nom abrégé, shortn ~1.dll.

SetFileShortName shortn ~1.dll \\ \\ ?? \\ Volume {26a21bda-A627-11D7-9931-806e6f6e6963} \\ temp \\ShortFileName.dll\\ NotExecuted  


## <a name="srdelayed-operations-status"></a>État des opérations srdelayed

Srdelayed écrit la chaîne L "SC =*xxxxxxx*" dans le quatrième champ de chaque enregistrement du fichier texte, où *xxxxxxx* est un hexadécimal qui indique l’état de l’opération demandée. La valeur zéro indique que l’opération a réussi.

Srdelayed crée une clé de registre nommée **SystemRestore** sous **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** pour consigner le résultat de l’opération de restauration entière. Si srdelayed effectue toutes les opérations demandées avec succès, le nom RestoreStatusResult est écrit sous cette clé avec une valeur égale à zéro. Si srdelayed n’est pas en mesure d’effectuer l’une des opérations demandées, les noms RestoreStatusResult et RestoreStatusDetails sont écrits sous cette clé avec des valeurs autres que zéro. Le nom RestoreStatusDetails est écrit sous cette clé uniquement si srdelayed n’est pas en mesure d’effectuer les opérations demandées. Si une opération de définition du nom abrégé d’un fichier échoue, srdelayed continue à l’opération suivante. Srdelayed considère les opérations de déplacement de fichier et de suppression de fichier comme critiques et ne continue pas en cas d’échec d’une opération de déplacement ou de suppression.

 

 