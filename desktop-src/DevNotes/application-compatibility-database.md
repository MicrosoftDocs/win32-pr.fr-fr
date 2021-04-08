---
description: L’infrastructure de compatibilité utilise une base de données pour identifier les problèmes de compatibilité des applications et leurs solutions.
ms.assetid: 3b35b758-18ca-40dd-8882-35d9b458264c
title: Base de données de compatibilité des applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba33ab3a8de702f2e620b7607f4d2b6904e6165
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747965"
---
# <a name="application-compatibility-database"></a>Base de données de compatibilité des applications

L’infrastructure de compatibilité utilise une base de données pour identifier les problèmes de compatibilité des applications et leurs solutions. Cette base de données est un fichier binaire indexé avec une extension. sdb. L’infrastructure de compatibilité fournit une interface de programmation pour accéder à la base de données.

Les problèmes de compatibilité peuvent être traités application par application au moment de l’exécution. Chaque application spécifiée dans la base de données contient un ou plusieurs composants qui ont besoin d’une solution. Les composants sont des fichiers exécutables qui sont généralement décrits à l’aide de leurs attributs de fichier (par exemple, checksum).

Le processus de recherche de base de données et de détermination des solutions pour chaque application est appelé *correspondance*. Les attributs de fichier et la présence de fichiers associés dans le dossier ou sous-dossier contenant le fichier. exe peuvent être utilisés pour créer une correspondance unique. Les fichiers associés sont appelés *fichiers correspondants*.

Une *balise* est un identificateur unique pour les entrées et les attributs de la base de données. Le *type de balise* indique le format des données associées à la [**balise**](tag.md). Par exemple, **le \_ nom de la balise** est de type **tag \_ \_ STRINGREF**; les données pour **tag \_ Name** sont une chaîne de nom. Un *TagId* est un pointeur vers une entrée dans une base de données particulière. Un *TAGREF* est un pointeur vers une entrée qui peut être utilisée sur plusieurs bases de données.

Les *attributs de fichier* sont des métadonnées associées à un fichier sur le disque. Ces attributs incluent le nom du fichier, la taille du fichier, la somme de contrôle, la version et la date. Ces attributs sont utilisés pour déterminer si un fichier chargé par le système correspond à une entrée de base de données. Par conséquent, ces attributs de fichier sont également appelés *attributs correspondants*.

## <a name="solutions"></a>Solutions

Les solutions les plus courantes appliquées aux composants d’une application sont AppHelp et AppFix.

Avec AppHelp, une notification de message localisée personnalisée s’affiche, généralement lorsque l’application est installée ou démarrée. Il contient un bref texte qui explique le problème de compatibilité et offre la possibilité de continuer à exécuter l’application. Toutefois, certaines applications échouent considérablement et peuvent être exécutées ; AppHelp ne donne pas à l’utilisateur la possibilité de continuer à exécuter ces applications.

Avec AppFix, les raccordements sont installés pour les API appelées par les composants de l’application. Ces points de raccordement pointent vers des fonctions stub qui peuvent être appelées à la place des fonctions système (également appelées « *Shiming*»). Les fonctions stub effectuent les opérations nécessaires pour permettre à l’application de s’exécuter sur la version installée de Windows. Chaque fonction stub peut éventuellement appeler la fonction système après avoir terminé son travail. Une *couche* ou un *mode* de compatibilité contient un ou plusieurs shims et indicateurs.

## <a name="in-this-section"></a>Dans cette section

-   [**\_données APPHELP**](apphelp-data.md)
-   [**ATTRINFO**](attrinfo.md)
-   [**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
-   [**Rechercher des \_ informations**](find-info.md)
-   [**INDEXID contient**](indexid.md)
-   [**TYPE de chemin \_**](path-type.md)
-   [**SdbBeginWriteListTag**](sdbbeginwritelisttag.md)
-   [**SdbCloseDatabase**](sdbclosedatabase.md)
-   [**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
-   [**SdbCommitIndexes**](sdbcommitindexes.md)
-   [**SdbCreateDatabase**](sdbcreatedatabase.md)
-   [**SdbDeclareIndex**](sdbdeclareindex.md)
-   [**SdbEndWriteListTag**](sdbendwritelisttag.md)
-   [**SdbFindFirstDWORDIndexedTag**](sdbfindfirstdwordindexedtag.md)
-   [**SdbFindFirstTag**](sdbfindfirsttag.md)
-   [**SdbFindNextTag**](sdbfindnexttag.md)
-   [**SdbFormatAttribute**](sdbformatattribute.md)
-   [**SdbFreeFileAttributes**](sdbfreefileattributes.md)
-   [**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
-   [**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
-   [**SdbGetFileAttributes**](sdbgetfileattributes.md)
-   [**SdbGetFirstChild**](sdbgetfirstchild.md)
-   [**SdbGetIndex**](sdbgetindex.md)
-   [**SdbGetMatchingExe**](sdbgetmatchingexe.md)
-   [**SdbGetNextChild**](sdbgetnextchild.md)
-   [**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
-   [**SdbGetTagFromTagID**](sdbgettagfromtagid.md)
-   [**SdbInitDatabase**](sdbinitdatabase.md)
-   [**SdbIsStandardDatabase**](sdbisstandarddatabase.md)
-   [**SdbMakeIndexKeyFromString**](sdbmakeindexkeyfromstring.md)
-   [**SdbOpenApphelpDetailsDatabase**](sdbopenapphelpdetailsdatabase.md)
-   [**SdbOpenApphelpResourceFile**](sdbopenapphelpresourcefile.md)
-   [**SdbOpenDatabase**](sdbopendatabase.md)
-   [**SdbQueryDataExTagID**](sdbquerydataextagid.md)
-   [**SDBQUERYRESULT**](sdbqueryresult.md)
-   [**SdbReadApphelpDetailsData**](sdbreadapphelpdetailsdata.md)
-   [**SdbReadBinaryTag**](sdbreadbinarytag.md)
-   [**SdbReadDWORDTag**](sdbreaddwordtag.md)
-   [**SdbReadQWORDTag**](sdbreadqwordtag.md)
-   [**SdbReadStringTag**](sdbreadstringtag.md)
-   [**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
-   [**SdbReleaseDatabase**](sdbreleasedatabase.md)
-   [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
-   [**SdbStartIndexing**](sdbstartindexing.md)
-   [**SdbStopIndexing**](sdbstopindexing.md)
-   [**SdbTagRefToTagID**](sdbtagreftotagid.md)
-   [**SdbTagToString**](sdbtagtostring.md)
-   [**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
-   [**SdbWriteBinaryTag**](sdbwritebinarytag.md)
-   [**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
-   [**SdbWriteDWORDTag**](sdbwritedwordtag.md)
-   [**SdbWriteNULLTag**](sdbwritenulltag.md)
-   [**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
-   [**SdbWriteStringTag**](sdbwritestringtag.md)
-   [**SdbWriteWORDTag**](sdbwritewordtag.md)
-   [**Types de bases de données shim**](shim-database-types.md)
-   [**ShimFlushCache**](shimflushcache.md)
-   [**Référence**](tag.md)
-   [**Types de BALISes**](tag-types.md)
-   [**TAGID**](tagid.md)
-   [**TAGREF**](tagref.md)

 

 



