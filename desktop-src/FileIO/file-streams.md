---
description: Dans le système de fichiers NTFS, les flux contiennent les données écrites dans un fichier et qui fournissent plus d’informations sur un fichier que les attributs et les propriétés.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Flux de fichiers (systèmes de fichiers locaux)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755164"
---
# <a name="file-streams-local-file-systems"></a>Flux de fichiers (systèmes de fichiers locaux)

Un flux est une séquence d’octets. Dans le système de fichiers NTFS, les flux contiennent les données écrites dans un fichier et qui fournissent plus d’informations sur un fichier que les attributs et les propriétés. Par exemple, vous pouvez créer un flux qui contient des mots clés de recherche ou l’identité du compte d’utilisateur qui crée un fichier.

Chaque flux associé à un fichier a sa propre taille d’allocation, sa propre taille réelle et sa longueur de données valides :

-   La taille d’allocation correspond à la quantité d’espace disque réservée pour un flux.
-   La taille réelle est le nombre d’octets utilisés par un appelant.
-   La longueur de données valide (VDL) est le nombre d’octets qui sont initialisés à partir de la taille d’allocation pour le flux.

Chaque flux conserve également son propre État pour la compression, le chiffrement et la plus faible. L’attribut de fichier épars de l’attribut de fichier sur le fichier est défini dans le membre **dwFileAttributes** de la structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) retournée par les fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) si l’un des flux a déjà été fragmenté. **\_ \_ \_** [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa), [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa), [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda), [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)et [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) retournent l’État épars du flux de données par défaut si aucun flux n’est spécifié.

Aucun fichier n’est associé à un flux. Les heures de fichier d’un fichier sont mises à jour lorsqu’un flux de fichier est mis à jour.

Les verrous opportunistes sont conservés par flux. Les modes de partage sont également gérés par flux. Lorsque l’accès en suppression est demandé sur un fichier, le système d’exploitation vérifie l’accès en suppression sur tous les flux ouverts dans un fichier. Si un autre processus a ouvert un flux sans l’autorisation de **\_ \_ Suppression de partage de fichiers** , vous ne pouvez pas ouvrir le fichier pour l’accès en suppression.

Si un fichier en cours de copie a un flux de données et que le redirecteur réseau est utilisé, le fichier peut être copié uniquement si le client dispose à la fois de l’autorisation lecture et de l’autorisation attributs de lecture.

## <a name="naming-conventions-for-streams"></a>Conventions d’affectation des noms pour les flux

Lorsqu’il est spécifié à partir de la ligne de commande de l’interpréteur de commandes Windows, le nom complet d’un flux est «*nom_fichier*:*nom du flux*: type de *flux*», comme dans l’exemple suivant : « myfile. dat : STREAM1 : $Data ».

Les caractères valides pour un nom de fichier sont également valides pour le nom du flux, y compris les espaces. Pour plus d’informations, consultez [attribution d’un nom à un fichier](naming-a-file.md). Le type de flux (également appelé code de type d’attribut) est interne au système de fichiers NTFS. Par conséquent, les utilisateurs ne peuvent pas créer de nouveaux types de flux, mais ils peuvent ouvrir des types de système de fichiers NTFS existants. Les valeurs du spécificateur de type de flux commencent toujours par le symbole dollar ($). Pour obtenir la liste des types de flux, voir ci-dessous.

Par défaut, le flux de données par défaut est sans nom. Pour spécifier entièrement le flux de données par défaut, utilisez «*filename*:: $Data », où $Data est le type de flux. Il s’agit de l’équivalent de «*filename*». Vous pouvez créer un flux nommé dans le fichier à l’aide des [conventions d’affectation des noms de fichiers](naming-a-file.md). Notez que « $DATA » est un nom de flux légal. Par exemple, le nom complet d’un flux nommé « $DATA » sur un fichier nommé «*Sample*» serait «*Sample*: $Data : $Data ». Si vous avez créé un flux nommé « bar » dans le même fichier, son nom complet est «*Sample*: bar : $Data ».

Lorsque vous créez et utilisez des fichiers qui ont des noms à un seul caractère, préfixez le nom de fichier par un point suivi d’une barre oblique inverse (. \) ou utilisez un nom de chemin d’accès qualifié complet. Cela est dû au fait que Windows traite les noms de fichiers à un seul caractère comme des lettres de lecteur. Quand une lettre de lecteur est spécifiée avec un chemin d’accès relatif, un signe deux-points sépare la lettre de lecteur du chemin d’accès. En cas d’ambiguïté quant au fait qu’un nom à un seul caractère est une lettre de lecteur ou un nom de fichier, Windows part du principe qu’il s’agit d’une lettre de lecteur si la chaîne qui suit le signe deux-points est un chemin d’accès valide, même si la lettre de lecteur n’est pas valide.

## <a name="stream-types"></a>Types de flux

Voici la liste des types de flux NTFS, également appelés codes de type d’attribut. Certains types de flux sont internes au système de fichiers NTFS et leur format n’est pas documenté.



| Type de flux                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :: $ATTRIBUTE \_ liste         | Contient une liste de tous les attributs qui composent le fichier et identifie l’emplacement de chaque attribut.                                                                                                                                                                                                                                                                                                                                          |
| :: $BITMAP                  | Bitmap utilisée par les index pour gérer l’espace libre de l’arborescence b pour un répertoire. L’arborescence binaire (b-Tree) est gérée par blocs de 4 Ko (quelle que soit la taille du cluster), ce qui permet de gérer l’allocation de ces segments. Ce type de flux est présent sur chaque répertoire.                                                                                                                                                                                           |
| :: $DATA                    | Flux de données. Le flux de données par défaut n’a pas de nom. Les flux de données peuvent être énumérés à l’aide des fonctions [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) et [**FindNextStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) .                                                                                                                                                                                                                                                |
| :: $EA                      | Contient des données d’attributs étendus.|
| :: \_ informations $EA         | Contient des informations de prise en charge sur les attributs étendus.                                                                                                                                                                                                                                                                                                                                                                                      |
| :: $FILE \_ nom              | Nom du fichier, en caractères Unicode. Cela comprend le nom abrégé du fichier, ainsi que les liens physiques.                                                                                                                                                                                                                                                                                                                                 |
| :: $INDEX \_ allocation       | Type de flux d’un répertoire. Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux. Ce flux représente le répertoire lui-même et contient toutes les données du répertoire. Les modifications apportées aux flux de ce type sont enregistrées dans le journal des modifications NTFS. Le nom de flux par défaut d’un $INDEX \_ type de flux d’allocation est $I 30 donc «*dirname*», «*dirname*:: $index \_ allocation » et «*dirname*: $I 30 : $index \_ allocation » sont tous équivalents. |
| :: $INDEX \_ racine             | Ce flux représente la racine de l’arborescence binaire (b-Tree) d’un index. Ce type de flux est présent sur chaque répertoire.                                                                                                                                                                                                                                                                                                                                           |
| :: $LOGGED \_ flux de l’utilitaire \_ | Semblable à :: $DATA mais les opérations sont journalisées dans le journal des modifications NTFS. Utilisé par EFS et le [NTFS transactionnel (TxF)](transactional-ntfs-portal.md). La paire «  :*StreamName*: $*STREAMTYPE*» pour EFS est «  : $EFS : $logged \_ Stream Utility \_ » et pour TxF est «  : $TxF \_ Data : $logged \_ Stream Utility \_ ».                                                                                                                                                    |
| :: $OBJECT \_ ID              | ID de 16 octets permettant d’identifier le fichier du service de suivi des liaisons.                                                                                                                                                                                                                                                                                                                                                                           |
| :: $REPARSE \_ point          | Données du [point d’analyse](reparse-points.md) .|



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des flux](using-streams.md)
</dt> </dl>

 

 



