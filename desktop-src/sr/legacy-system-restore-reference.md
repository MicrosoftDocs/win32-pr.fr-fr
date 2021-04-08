---
title: Référence de restauration du système héritée
description: Cette documentation décrit les détails d’implémentation du référentiel utilisé par une version héritée de la restauration du système. Elle ne s’applique pas à l’implémentation de la restauration du système sur Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839342"
---
# <a name="legacy-system-restore-reference"></a>Référence de restauration du système héritée

\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]

Cette documentation décrit les détails d’implémentation du référentiel utilisé par une version héritée de la restauration du système. Elle ne s’applique pas à l’implémentation de la restauration du système sur Windows Vista.

## <a name="system-restore-repository-structure"></a>Structure du référentiel de restauration du système

Windows XP avec SP2 contient un référentiel pour la restauration du système dans le dossier suivant :% SYSTEMDRIVE% \\ System Volume Information. Ce référentiel contient des informations sur les points de restauration, qui sont essentiellement un instantané du système à un moment donné.

Le référentiel est structuré comme suit :

**System Volume Information**    ** \_ Restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n** *     ** \_ Restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n***

Pour déterminer \_ le dossier Restore {*GUID*} à utiliser, lisez le **GUID** spécifié dans le fichier suivant : SYSTEMROOT% \\ system32 \\ Restore \\MachineGUID.txt.

Dans chaque \_ dossier Restore {*GUID*}, le \_ fichier Driver. cfg contient des informations provenant d’une structure de **\_ \_ configuration persistante SR** définie comme suit :

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>Fichiers contenus dans chaque dossier RP *n*

Chaque dossier RP *n* contient un dossier d’instantanés qui contient les éléments suivants :

-   Instantané des ruches du Registre
-   Dossier de référentiel qui contient un instantané de l’espace de stockage WMI
-   Instantané de la base de données COM+
-   Instantané de la base de données IIS

Chaque dossier RP *n* contient un fichier RP. log qui contient des informations générales sur le point de restauration de la structure [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .

Chaque dossier RP *n* peut contenir des fichiers utilisés pour suivre les modifications d’un point de restauration. Le premier fichier est nommé « change. log », le fichier suivant est nommé « change. log. 1 », et ainsi de suite. Chaque fichier journal de modification contient les structures suivantes :

-   [**\_ \_ en-tête du journal des modifications**](change-log-header.md)
-   [**Modifier \_ \_Entrée du journal**](change-log-entry.md)1
-   [**Modifier \_ \_Entrée de journal**](change-log-entry.md)2
-   ...
-   [**Modifier \_ \_Entrée de journal**](change-log-entry.md)*n*

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Structures de restauration du système héritées](legacy-system-restore-structures.md)
</dt> </dl>

 

 




