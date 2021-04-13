---
description: Les formes de syntaxe suivantes sont prises en charge pour les transactions SymStore. Le premier paramètre doit toujours être Add ou del. L’ordre des autres paramètres n’a pas d’importance.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Options de Command-Line SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b69cdca9ee74cf01041375f26b2e151dc3ec5d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321754"
---
# <a name="symstore-command-line-options"></a>Options de Command-Line SymStore

Les formes de syntaxe suivantes sont prises en charge pour les transactions SymStore. Le premier paramètre doit toujours être Add ou del. L’ordre des autres paramètres n’a pas d’importance.

**SymStore ajouter** \[ **/l** **/o** **/p** **/r** **/Compress** \] \[ **- : MSG** *message* \] \[ **- : rel** \] \[ **- : norefs** \] **/f** *fichier* **/s** *Store* **/t** *Product* \[ **/v** *version* \] \[ **/c** *Comment* \] \[ **/d** *logfile*\]

**SymStore ajouter** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **- : rel** \] \[ **- : norefs** \] **/g** *partage* **/f** *fichier* **/x** *IndexFile* \[ **/d** *logfile*\]

**SymStore ajouter** \[ **/o** **/Compress** \] \[ **/p** \[ **- : MSG** \| *message* \] \[ **- : rel** \] \[ **- : norefs** \] \] **/y** *IndexFile* **/g** *partage* **/s** *Store* **/t** *Product* \[ **/v** *version* \] \[ **/c** *Comment* \] \[ **/d** *logfile*\]

**requête SymStore** \[ **/o** **/r** \] **/f** *fichier* **/s** *Store* \[ **/d** fichier *Journal*\]

**SymStore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *logfile*\]

**SymStore** **/ ?**



| Paramètre      | Signification                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Force SymStore à ajouter de nouvelles informations d’indexation à un fichier d’index existant. (Cette option est utilisée uniquement avec l’option/x.)                                                                                                                                                                                                                                                                                 |
| /c *Commentaire*   | Spécifie un commentaire pour la transaction.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Force SymStore à créer une version compressée de chaque fichier copié dans le magasin de symboles au lieu d’utiliser une copie non compressée du fichier. Cette option est valide uniquement lors du stockage de fichiers et non des pointeurs, et ne peut pas être utilisée avec l’option/p.                                                                                                                                                              |
| /d *fichier journal*   | Spécifie un fichier journal à utiliser pour la sortie de commande. Si ce n’est pas le cas, les informations de transaction et autres sorties sont envoyées à stdout.                                                                                                                                                                                                                                                                     |
| *fichier* /f      | Spécifie un ou plusieurs chemins d’accès de fichiers (ou répertoires) à ajouter. Si un chemin d’accès de fichier spécifié commence par un symbole « @ », un [fichier réponse](../midl/response-files.md) contenant une liste de fichiers à ajouter (un chemin de fichier par ligne) est attendu.                                                                                                                                             |
| /g *partage*     | Spécifie le serveur et le partage où les fichiers de symboles ont été stockés à l’origine. Lorsqu’il est utilisé avec/f, le *partage* doit être identique au début du spécificateur de *fichier* . Lorsqu’il est utilisé avec/y, *share* doit être l’emplacement des fichiers de symboles d’origine (pas le fichier d’index). Cela vous permet de modifier ultérieurement cette partie du chemin d’accès au cas où vous déplacez les fichiers de symboles sur un serveur et un partage différents. |
| *ID* /i        | Spécifie la chaîne d’ID de la transaction.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Permet au fichier d’être dans un répertoire local plutôt que dans un chemin d’accès réseau. (Cette option est utilisée uniquement avec l’option/p.)                                                                                                                                                                                                                                                                                        |
| /o             | Fait en sorte que SymStore affiche une sortie détaillée.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Fait en sorte que SymStore stocke un pointeur vers le fichier, plutôt que le fichier lui-même.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Force SymStore à ajouter des fichiers ou des répertoires de manière récursive.                                                                                                                                                                                                                                                                                                                                                     |
| /s *magasin*     | Spécifie le répertoire racine pour le magasin de symboles.                                                                                                                                                                                                                                                                                                                                                           |
| /t *produit*   | Spécifie le nom du produit.                                                                                                                                                                                                                                                                                                                                                                           |
| /v *version*   | Spécifie la version du produit.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *IndexFile* | Force SymStore à ne pas stocker les fichiers de symboles réels. Au lieu de cela, SymStore enregistre les informations dans le *IndexFile* qui permettront à SymStore d’accéder ultérieurement aux fichiers de symboles.                                                                                                                                                                                                                         |
| /y *IndexFile* | Force SymStore à lire les données d’un fichier créé avec/x.                                                                                                                                                                                                                                                                                                                                                |
| - : Message MSG  | Ajoute le message spécifié à chaque fichier. (Cette option ne peut être utilisée que si/p est utilisé.)                                                                                                                                                                                                                                                                                                                     |
| - : REL          | Permet aux chemins d’accès dans les pointeurs de fichier d’être relatifs. Cette option implique l’option/l. (Cette option ne peut être utilisée que si/p est utilisé.)                                                                                                                                                                                                                                                                     |
| - : Norefs       | Omet la création de fichiers de pointeur de référence pour les fichiers et les pointeurs stockés. Cette option est valide uniquement lors de la création initiale d’un magasin de symboles si le magasin en cours de modification a été créé avec cette option.                                                                                                                                                                                      |
| /?             | Affiche le texte d’aide de la commande SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



