---
description: cette rubrique décrit les éléments que Windows index de recherche.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: Ce qui est inclus dans l’index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbffec8aba8a985faca112eac434b669d22eff82d94d6b4eaf5588585ced771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463322"
---
# <a name="what-is-included-in-the-index"></a>Ce qui est inclus dans l’index

cette rubrique décrit les éléments que Windows index de recherche.

Cette rubrique est organisée comme suit :

-   [Indexé par défaut](#indexed-by-default)
-   [Formats de fichier pris en charge](#file-formats-supported)
-   [Exclusions de fichiers](#file-exclusions)
-   [Exclusions de dossiers](#folder-exclusions)
-   [Exclusions de lecteur](#drive-exclusions)
-   [Rubriques connexes](#related-topics)

 

## <a name="indexed-by-default"></a>Indexé par défaut

les filtres et les gestionnaires de protocole sont inclus dans Windows recherche pour indexer les types de contenu suivants :

-   dans Windows Vista et versions ultérieures, les éléments de messagerie microsoft Outlook et microsoft Outlook Express de l’utilisateur sont indexés pendant l’exécution de l’application de messagerie.
-   les fichiers hors connexion dans le cache côté client (CSC) sont indexés par Windows recherche locale.
-   Windows La recherche prend en charge la collecte des adresses de démarrage de fichiers sur les volumes NTFS et FAT32. NTFS prend en charge l’indexation basée sur les notifications et FAT32 prend en charge une analyse incrémentielle au démarrage, puis répond aux notifications.
-   Windows Vista et versions ultérieures continuent à exposer une propriété par dossier/par fichier pour activer l’indexation : l’option «**pour la recherche rapide, autoriser le service d’indexation à indexer ce dossier**» dans la boîte de dialogue des **Propriétés** . La définition de l’indicateur de bit FANCI garantit que les propriétés de base du protocole, telles que l’URL, le nom de fichier et la taille, sont indexées, mais que ni les gestionnaires de filtre ni les gestionnaires de propriétés ne sont exécutés.
-   Le contenu de texte est indexé, mais la ponctuation n’est pas.

## <a name="file-formats-supported"></a>Formats de fichier pris en charge

Windows La recherche a des gestionnaires de protocole, des gestionnaires de propriétés et des gestionnaires de filtre pour indexer automatiquement les formats suivants :

-   Fichiers multimédias : tous les types de fichiers multimédias
-   **HTML** (nlhtml.dll) :. ascx,. asp,. aspx,. CSS,. hhc, .htm, .html,. htt,. htw,. htx,. odc,. stm
-   **HTML MIME** (mimefilt.dll) :. mht,. mhtml
-   **Office** (offfilt.dll) : .doc,. dot,. pot,. pps, .ppt,. xlb,. xlc, .xls,. xlt
-   **Texte** (query.dll) :. asm,. asx, .bat,. c,. cmd,. cpp,. cxx,. def,. dic,. h,. HPP,. hxx,. idl,. idq,. inf, .ini,. inx, .js,. log,. m3u,. RC,. reg,. rtf, .txt,. URL,. vbs,. WTX
-   **XML** (xmlfilt.dll) : .xml,. Xsl
-   **OneNote**:. One
-   **Journal des tablettes** (jntfiltr.dll) :. jnt

Les propriétés sont indexées pour tous les fichiers à l’exception du stockage structuré. sur Windows Vista et versions ultérieures, de nombreuses propriétés de fichiers multimédias sont indexées. Toutefois, le contenu n’est pas indexé si les fichiers sont protégés par la gestion des droits numériques (DRM).

> [!Note]  
> Le filtre HTML n’indexe pas les commentaires HTML.

 

## <a name="file-exclusions"></a>Exclusions de fichiers

Lorsqu’un type de fichier n’est associé à aucun filtre, ou lorsqu’un fichier n’a pas d’extension, les propriétés système des fichiers de ce type sont indexées, mais le contenu du fichier n’est pas indexé.

en outre, Windows Search n’indexe pas le contenu des fichiers sous la gestion des droits relatifs à l’information (IRM) ou la gestion des droits numériques (DRM).

sur Windows Vista (uniquement), les fichiers suivants sont exclus de l’indexation par défaut :

-   Fichiers marqués comme masqués ou système.
-   Fichiers avec les extensions suivantes :

    .386,. APS,. AudioCD,. bin,. BK1,. BK2,. bkf,. bsc,. BTR,. chk,. ci,. CRWL,. dbg,. DCT,. DeskLink,. dir,. dl \_ , .dll,. drv,. DVD,. evt,. ex \_ , .exe,. exp,. EYB,. FND,. FNT,. Dossier,. fon,. ghi,. gthr,. hqx,. ICM,. IDB,. idx,. ilk,. IMC,. in \_ , .ini,. INV,. JBF,. latex,. lib,. local,. M14,. Mac,. manifest,. map,. MAPIMail,. MMF,. Movie,. mV,. mydocs,. NCB,. obj,. OC \_ ,. ocx,. pch,. pdb,. PF,. PMA,. PMC,. PML,. PMR,. res,. RMP,. RPC,. rsp,. SBR,. SC2,. sit,. SR,. Sy,. sym, .sys,. tlb,. trc,. TTC,. ttf,. VBX,.,. \_ \_ WLL,. WLT,. XIX,. Z96,. ZFSendToTarget.

## <a name="folder-exclusions"></a>Exclusions de dossiers

> [!TIP]
> Les noms de dossiers ne respectent pas la casse.

 

Les dossiers suivants sont exclus de l’indexation par défaut :



| Modèle d’exclusion de dossier                                                              | effet dans le Windows 7 | effet dans Windows Vista | Description                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% Système%* \\ ProgramData \\ des \\ données Microsoft Search \\\\                                    | **Excluded**        | Aucun effet               | Données de l’indexeur sur le lecteur système.                                                                                                                                                                                          |
| *% Système%* \\ Users \\ *nom_utilisateur* \\ AppData\\                                              | **Excluded**        | Aucun effet               | Données d’application de l’utilisateur (y compris les données temporaires) sur le lecteur système.<br/> Pour chaque utilisateur qui se connecte au système, un modèle d’exclusion spécifique est ajouté, qui exclut les données d’application de l’index.<br/> |
| *% Système%* \\ users \\ \* \\ AppData \\ Local \\ Microsoft \\ Windows \\ fichiers Internet temporaires\\ | **Excluded**        | Aucun effet               | emplacement par défaut de Windows fichiers internet temporaires internet Explorer sur le lecteur système.<br/> Si l’emplacement des fichiers Internet temporaires d’Internet Explorer est modifié, ces fichiers peuvent être indexés.<br/>    |
| *% Système%* \\ Windows \\ CSC\\                                                            | **Excluded**        | Aucun effet               | si l’indexation est activée pour le répertoire système Windows, le dossier CSC (sur le lecteur système) est toujours exclu de l’indexation.                                                                                           |
| *% Système%* \\ \\ \* Windows \\ Modèle\\                                                       | **Excluded**        | Aucun effet               | Windows les données temporaires sur le lecteur système.                                                                                                                                                                                     |
| *% Système%* \\ Windows.\*\\                                                              | **Excluded**        | Aucun effet               | anciennes installations de Windows sur le lecteur système.                                                                                                                                                                             |
| *% Système%* \\ ProgramData\\                                                             | **Excluded**        | **Excluded**            | Notez que le sous-dossier du menu Démarrer partagé est indexé.                                                                                                                                                                     |
| *% Système%* \\ Utilisateurs \\ \* \\ AppData\\                                                      | **Excluded**        | **Excluded**            | Données d’application des utilisateurs (y compris les données temporaires).                                                                                                                                                                              |
| *% Système%* \\ \\ \* \\ \\ \\ Temp local des utilisateurs AppData\\                                         | **Excluded**        | **Excluded**            | Données temporaires des utilisateurs. Si l’indexation est activée pour les données d’application utilisateur, les données temporaires de l’utilisateur sont toujours exclues de l’indexation par défaut.                                                                                           |
| *% Système%* \\ Windows\\                                                                 | **Excluded**        | **Excluded**            | Fichiers de système d’exploitation sur le lecteur système.                                                                                                                                                                                |
| *% Système%* \\ $Recycle bin\\                                                            | **Excluded**        | **Excluded**            | Emplacement des fichiers dans la corbeille.                                                                                                                                                                                      |
| *% Système%* \\ Build\\                                                                   | Aucun effet           | **Excluded**            | Sur le lecteur système.                                                                                                                                                                                                       |
| *% Système%* \\ Référentiel installé\\                                                    | Aucun effet           | **Excluded**            | Sur le lecteur système.                                                                                                                                                                                                       |
| *% Système%* \\ Fichiers programme\\                                                           | Aucun effet           | **Excluded**            | Sur le lecteur système.                                                                                                                                                                                                       |
| *% Système%* \\ Fichiers programme (x86)\\                                                     | Aucun effet           | **Excluded**            | Sur le lecteur système.                                                                                                                                                                                                       |
| \*\\Modèle\\\*                                                                          | Aucun effet           | **Excluded**            | Windows des données temporaires et d’autres dossiers portant le nom « temp ».                                                                                                                                                                  |
| *% Système%* \\ Utilisateurs \\ par défaut\\                                                          | Aucun effet           | **Excluded**            | Emplacement des données de profil utilisateur par défaut sur le lecteur système.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Aucun effet           | **Excluded**            | les anciennes installations de Windows et les autres dossiers dont les noms commencent par « Windows ».                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusions de lecteur

sur Windows 7 et Windows Vista, les lecteurs amovibles ne sont pas indexés par défaut.

> [!Note]  
> Si les lecteurs amovibles sont signalés comme des lecteurs fixes, vous pouvez les ajouter à indexer même s’ils sont réellement amovibles. les informations sont conservées dans l’index et Windows recherche effectue une analyse incrémentielle pour rapprocher les résultats de l’indexation lorsque le disque amovible est reconnecté. Étant donné que les disques mémoire flash USB sont signalés comme étant amovibles, ils ne peuvent pas être indexés.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[indexation, interrogation et notifications dans Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[processus d’indexation dans Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[interrogation du processus dans Windows la recherche](querying-process--windows-search-.md)
</dt> <dt>

[processus de notifications dans Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Configuration requise pour la mise en forme des URL](url-formatting-requirements.md)
</dt> </dl>

 

 




