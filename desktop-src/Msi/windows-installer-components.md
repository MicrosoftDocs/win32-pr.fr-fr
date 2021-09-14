---
description: Un composant est une partie de l’application ou du produit à installer.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Composants du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009559"
---
# <a name="windows-installer-components"></a>Windows Composants du programme d’installation

Un composant est une partie de l’application ou du produit à installer. Exemples de composants : fichiers uniques, groupe de fichiers associés, objets COM, inscription, clés de Registre, raccourcis, ressources, bibliothèques regroupées dans un répertoire ou parties partagées de code, telles que MFC ou DAO.

Le service d’installation installe ou supprime un composant en tant qu’élément cohérent unique. Il effectue le suivi de chaque composant par le GUID d’ID de composant respectif spécifié dans la colonne ComponentId de la [table des composants](component-table.md).

> [!Note]  
> Deux composants qui partagent le même ID de composant sont traités comme plusieurs instances du même composant, quel que soit leur contenu réel. Une seule instance de n’importe quel composant est installée sur l’ordinateur d’un utilisateur. Plusieurs fonctionnalités ou applications peuvent donc partager certains composants.

 

Étant donné que les composants sont généralement partagés, l’auteur d’un package d’installation doit respecter des règles strictes lors de la spécification des composants d’une fonctionnalité ou d’une application. cela est essentiel pour le bon fonctionnement du mécanisme de décompte de références Windows Installer. Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).

En résumé, ces règles sont les suivantes :

-   Chaque composant doit être stocké dans un dossier unique.
-   Aucun fichier, entrée de Registre, raccourci ou autre ressource ne doit être fourni en tant que membre de plusieurs composants. Cela s’applique à tous les produits, versions de produits et entreprises.

Pour plus d’informations sur l’utilisation des composants, consultez.

-   [Installation d’un composant manquant](installing-a-missing-component.md)
-   [Installation des composants permanents, des fichiers, des polices, des clés de Registre](installing-permanent-components-files-fonts-registry-keys.md)
-   [Utilisation des composants qualifiés](using-qualified-components.md)
-   [Utilisation de composants transitifs](using-transitive-components.md)
-   [Utilisation des fonctionnalités et des composants](working-with-features-and-components.md)
-   [Création d’un package volumineux](authoring-a-large-package.md)
-   [Vérification de l’installation des fonctionnalités, des composants, des fichiers](checking-the-installation-of-features-components-files.md)
-   [Recherche d’une fonctionnalité ou d’un composant endommagé](searching-for-a-broken-feature-or-component.md)
-   [Publication de produits, de fonctionnalités et de composants](publishing-products-features-and-components.md)

 

 



