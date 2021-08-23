---
description: Chaque point d’analyse a une balise d’identificateur, ce qui vous permet de distinguer efficacement les différents types de points d’analyse, sans avoir à examiner les données définies par l’utilisateur dans le point d’analyse.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Étiquettes de point d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b31d4a1765266295b85c95c0955ae9c51faeb34ae07f3af48288a17a50f2166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015187"
---
# <a name="reparse-point-tags"></a>Étiquettes de point d’analyse

Chaque point d’analyse a une balise d’identificateur, ce qui vous permet de distinguer efficacement les différents types de points d’analyse, sans avoir à examiner les données définies par l’utilisateur dans le point d’analyse. Le système utilise un ensemble de balises prédéfinies et une plage de balises réservées pour Microsoft. Si vous utilisez l’une des balises réservées lors de la définition d’un point d’analyse, l’opération échoue. Les balises qui ne sont pas incluses dans ces plages ne sont pas réservées et sont disponibles pour votre application.

Lorsque vous définissez un point d’analyse, vous devez baliser les données à placer dans le point d’analyse. Une fois que le point d’analyse a été établi, une nouvelle opération set échoue si la balise pour les nouvelles données ne correspond pas à la balise pour les données existantes. Si les balises correspondent, l’opération ensembliste remplace le point d’analyse existant.

Pour récupérer la balise de point d’analyse, utilisez la fonction [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) . Si le membre **dwFileAttributes** contient l’attribut de point d' **analyse d’attribut de fichier \_ \_ \_** , le membre **dwReserved0** spécifie le point d’analyse.

## <a name="tag-contents"></a>Contenu de la balise

Les étiquettes d’analyse sont stockées sous forme de valeurs **DWORD** . Les bits définissent certains attributs, comme indiqué dans le diagramme suivant.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Les 16 bits de poids faible déterminent le type de point d’analyse. Les 16 bits de poids fort ont 12 bits réservés pour une utilisation future et 4 bits qui désignent des attributs spécifiques des balises et les données représentées par le point d’analyse. Le tableau suivant décrit ces bits.



| bit | Description                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft bit. Si ce bit est défini, la balise est la propriété de Microsoft. Toutes les autres balises doivent utiliser la valeur zéro pour ce bit. |
| R   | Réservé doit être égal à zéro pour toutes les balises non-Microsoft.                                                           |
| N   | Bit de substitution de nom. Si ce bit est défini, le fichier ou le répertoire représente une autre entité nommée dans le système. |



 

Les macros suivantes permettent de tester les balises :

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Chaque macro retourne une valeur différente de zéro si le bit associé est défini.

Les éléments suivants sont des valeurs de balise de réanalyse prédéfinies de Microsoft ; ils sont définis dans Winnt. h :

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

Pour garantir l’unicité des balises, Microsoft fournit un mécanisme permettant de distribuer de nouvelles balises. Pour plus d’informations, consultez le [Kit IFS (Installable File System)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



