---
description: Le code du package de mise à niveau doit être modifié par rapport à celui du produit d’origine.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Mise à jour des informations récapitulatives pour une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223076"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Mise à jour des informations récapitulatives pour une mise à niveau

Le code du package de mise à niveau doit être modifié par rapport à celui du produit d’origine. Le code du package est stocké dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) . Pour plus d’informations, consultez [codes de package](package-codes.md). Utilisez Msiinfo.exe, ou un autre éditeur, pour modifier les informations récapitulatives de MNP2001.msi comme décrit dans [Ajout d’informations de résumé](adding-summary-information.md).



| Propriété informations de synthèse                                                   | Données                                                                             | Notes                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modèle**](template-summary.md)(plateforme et langue)<br/>         | ; 1033                                                                            | Plateforme et langage utilisé par la base de données. Si la spécification de la plateforme est manquante dans la valeur de la propriété Résumé du [**modèle**](template-summary.md) , le programme d’installation suppose l’architecture Intel. La propriété [**ProductLanguage**](productlanguage.md) de la base de données est généralement utilisée pour cette propriété Summary. L’ID de langue de l’exemple indique que le package utilise l’anglais (États-Unis). |
| [**Numéro de révision**](revision-number-summary.md)(code de package)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Il s’agit du [GUID](guid.md) du code du package qui identifie de façon unique l’exemple de package. Si vous reproduisez cet exemple, utilisez un utilitaire tel que GUIDGEN pour générer un GUID différent pour votre package. Les résultats de GUIDGEN contiennent des caractères minuscules, Notez que vous devez remplacer tous les caractères minuscules par des majuscules pour un code de package valide.                                                     |
| [**Nombre de pages**](page-count-summary.md)(version minimale du programme d’installation)<br/> | 200                                                                              | pour un minimum Windows Installer version 2,0, cette propriété doit être définie sur l’entier 200.                                                                                                                                                                                                                                                                                                         |
| [**Nombre de mots**](word-count-summary.md)(type de source)<br/>            | 0                                                                                | Le type de source globale pour le package est un nom de fichier long et non compressé. Pour plus d’informations, consultez sources compressées [et non compressées](compressed-and-uncompressed-sources.md) , ainsi que la description de la colonne Attributes de la [table file](file-table.md).                                                                                                                               |
| [**Intitulé**](title-summary.md)                                                 | Base de données d’installation                                                            | Informe les utilisateurs que cette base de données est destinée à une installation plutôt qu’à une transformation ou un correctif.                                                                                                                                                                                                                                                                                                          |
| [**Subject**](subject-summary.md)                                             | MNP2001                                                                          | Les explorateurs de fichiers peuvent afficher ce fichier comme produit à installer avec cette base de données.                                                                                                                                                                                                                                                                                                                    |
| [**Mot**](keywords-summary.md)                                           | Programme d’installation, MSI, base de données                                                         | Les explorateurs de fichiers capables d’effectuer des recherches par mot clé peuvent rechercher ces mots.                                                                                                                                                                                                                                                                                                                      |
| [**Auteur**](author-summary.md)                                               | Microsoft Corporation                                                            | Nom du fabricant du produit.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Commentaires**](comments-summary.md)                                           | cette base de données du programme d’installation contient la logique et les données requises pour installer Bloc-notes. | Informe les utilisateurs sur l’objectif de cette base de données.                                                                                                                                                                                                                                                                                                                                                    |
| [**Création de l’application**](creating-application-summary.md)                   | Orca                                                                             | Application utilisée pour créer la base de données d’installation. L’exemple spécifie l’éditeur de base de données Orca comme exemple.                                                                                                                                                                                                                                                                                   |
| [**Sécurité**](security-summary.md)                                           | 0                                                                                | L’exemple de base de données est en lecture-écriture illimité.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continuer](validating-an-installation-upgrade.md)

 

 




