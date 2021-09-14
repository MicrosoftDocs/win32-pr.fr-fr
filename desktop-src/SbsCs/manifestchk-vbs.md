---
description: le Manifestchk.vbs de fichier VBScript est un outil de validation fourni dans le kit de développement logiciel (SDK) de Microsoft Windows qui valide les fichiers de manifeste de l’application et de l’assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118946"
---
# <a name="manifestchkvbs"></a>Manifestchk.vbs

le Manifestchk.vbs de fichier VBScript est un outil de validation fourni dans le kit de développement logiciel (SDK) de Microsoft Windows qui valide les fichiers de manifeste de l’application et de l’assembly.

l’exécution de cet exemple requiert Windows Script Host. pour plus d’informations sur Windows script host, consultez la section Windows script host de l’SDK Windows. Windows Script Host est en fait deux hôtes. CScript.exe est la version qui vous permet d’exécuter des scripts à partir de l’invite de commandes. CScript.exe fournit des commutateurs de ligne de commande pour définir les propriétés de script.

Le format de ligne de commande est le suivant :

**Cscript//nologo manifestchk.vbs/s :** *\[ lecteur : \] \[ chemin d’accès \] schemafilename* **/m :** *\[ lecteur : \] \[ chemin \] ManifestFileName* **\[ /q \] /t :** *option*

Les indicateurs définis pour Manifestchk.vbs sont décrits dans le tableau suivant.



| Indicateur | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /s   | Spécifie le nom du fichier de schéma du manifeste pour la validation des manifestes. Consultez le schéma dans le [schéma de fichier manifeste](manifest-file-schema.md).                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| /m   | Spécifie le nom du fichier manifeste à valider.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| /q   | Supprime toutes les sorties de la console.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| /t   | Spécifie le type de fichier manifeste. Les valeurs valides sont : AM valide le [schéma de fichier manifeste](manifest-file-schema.md) d’un manifeste d' [assembly](assembly-manifests.md) ou d’un [manifeste d’application](application-manifests.md)<br/> Le PC valide le [schéma du fichier de configuration](publisher-configuration-file-schema.md) du serveur de publication d’un fichier de configuration d' [éditeur](publisher-configuration-files.md)<br/> AC validez le schéma de fichier de configuration d’application d’un [fichier de configuration d’application](application-configuration-files.md).<br/> |



 

Si l’indicateur/q n’est pas spécifié, Manifestchk.vbs affiche des informations détaillées sur la première erreur rencontrée dans le fichier et affiche un message indiquant si le processus de validation a réussi ou non.

Cet utilitaire vérifie les éléments suivants :

-   Une ligne de commande valide.
-   cette MSXML version 3 est installée.
-   Que le manifeste utilise du XML bien formé.
-   Que le manifeste accepte le schéma fourni. Notez que Manifestchk.vbs vérifie le fichier manifeste en fonction de ce qui est spécifié dans le schéma fourni. Pour obtenir un exemple de schéma de manifeste, consultez [schéma de fichier manifeste](manifest-file-schema.md).

Cscript.exe retourne la valeur 0 si le processus de validation a réussi et 1 s’il n’a pas réussi. Elle retourne 2 s’il y a une erreur dans un argument de ligne de commande.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement d’assembly côte à côte](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




