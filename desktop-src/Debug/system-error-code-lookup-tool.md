---
description: Décrit comment utiliser l’outil de recherche d’erreurs Microsoft pour rechercher des explications de texte sur les codes d’erreur hexadécimaux dans Windows.
title: Outil de recherche d’erreurs Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514331"
---
# <a name="the-microsoft-error-lookup-tool"></a>Outil de recherche d’erreurs Microsoft

L’outil de recherche d’erreurs Microsoft affiche le texte du message associé à un code d’État hexadécimal (ou autre code). Ce texte est défini dans différents fichiers d’en-tête de code source Microsoft, tels que winerror. h, Setupapi. h, etc.

L’outil est signé numériquement par Microsoft. Voici les informations SHA256 pour le téléchargement de fichiers :  

|Algorithm |Hachage |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Les environnements d’entreprise peuvent limiter les fichiers qui peuvent être exécutés et à partir de où. Avant de télécharger et d’exécuter cet outil, vérifiez les informations suivantes :
> - Avez-vous besoin d’une autorisation ou d’une exception de sécurité pour pouvoir télécharger ou exécuter l’outil ?
> - Pouvez-vous stocker et exécuter cet outil sur votre ordinateur (par exemple, dans votre dossier de documents) ? Ou avez-vous besoin de stocker et d’exécuter l’outil sur un ordinateur spécialisé, tel qu’un serveur de fichiers central ?

## <a name="usage"></a>Utilisation

1. Téléchargez l’outil en sélectionnant [ce lien](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).
1. Si vous n’avez pas spécifié d’emplacement à l’étape 1, accédez à votre dossier de téléchargement, puis copiez ou déplacez le fichier téléchargé (Err_6.4.5.exe) dans le dossier dans lequel vous allez stocker l’outil. Vous n’avez pas besoin de développer ou d’installer le fichier.
   > [!NOTE]
   > Si vous copiez ou déplacez le fichier vers un dossier qui est listé dans la variable **d’environnement PATH** de votre système d’exploitation, il fonctionnera à n’importe quelle invite de commandes.

1. Ouvrez une fenêtre d’invite de commandes. Si nécessaire, remplacez le répertoire par l’emplacement de l’outil de recherche d’erreurs.
1. Exécutez la commande suivante :
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > Dans cette commande, \<*error code*> représente le code hexadécimal que vous souhaitez rechercher.

## <a name="examples"></a>Exemples

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Informations complémentaires

Gardez à l’esprit qu’il s’agit d’un outil « à un point dans le temps ». L’outil de recherche d’erreurs Microsoft décode la plupart des codes d’erreur Microsoft à la date de compilation de l’outil. À mesure que de nouvelles versions de Windows ajoutent de nouveaux codes d’événement et d’erreur, vous devrez peut-être télécharger une nouvelle version de l’outil de recherche d’erreurs. Consultez le centre de téléchargement Microsoft pour obtenir une nouvelle version ou consultez [codes d’erreur](system-error-codes.md).
