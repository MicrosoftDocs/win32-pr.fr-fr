---
description: Une utilisation courante des composants transitives consiste à préparer un produit à réinstaller pendant une mise à niveau du système.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Utilisation de composants transitifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103953508"
---
# <a name="using-transitive-components"></a>Utilisation de composants transitifs

Une utilisation courante des composants transitives consiste à préparer un produit à réinstaller pendant une mise à niveau du système. L’auteur du package d’installation de spécifie les composants qui doivent être échangés pendant une mise à niveau du système comme ayant l’attribut transitif. Lorsque l’utilisateur met ultérieurement à niveau le système, le produit doit être réinstallé. Lors de cette réinstallation, le programme d’installation supprime les composants précédents et installe les composants ultérieurs, sans avoir à installer l’intégralité du produit.

**Pour inclure deux composants transitifs dans le package d’installation**

1.  Incluez les deux composants transitifs dans le package d’installation.
2.  Créez les deux composants transitifs dans la [table](component-table.md) des composants de la même façon que les composants normaux. Chaque composant transitif doit avoir son propre GUID unique spécifié dans la colonne ComponentId.
3.  Incluez le bit **msidbComponentAttributesTransitive** dans la colonne attributs de la table des composants pour chaque composant transitif. Si ce bit est défini, le programme d’installation réévalue la valeur de l’instruction dans la colonne condition lors de la réinstallation.

    Si la valeur était précédemment false et a été remplacée par true, le programme d’installation installe le composant.

    Si la valeur était précédemment true et a été remplacée par false, le programme d’installation supprime le composant même si le composant a d’autres produits comme clients.

    > [!Note]  
    > À moins que le bit transitif ne soit défini, le composant reste activé une fois installé, même si l’instruction conditionnelle prend la valeur false lors d’une installation de maintenance ultérieure du produit. Les conditions doivent être basées uniquement sur les États de l’ordinateur. N’utilisez pas avec des conditions basées sur les États utilisateur ou les propriétés définies sur la ligne de commande, car cela peut obliger le programme d’installation à exiger une réinstallation du produit à chaque utilisation par un autre utilisateur.

     

4.  Entrez des expressions conditionnelles complémentaires dans les champs condition de la table de contrôle, de sorte que lorsque la condition sur le premier composant transitif devient false, la condition sur le deuxième composant transitif passe à true. Cela entraîne la suppression du premier composant et l’installation du deuxième composant lors de la réinstallation de l’application.

Une réinstallation du produit est nécessaire pour basculer les composants transitifs. Les auteurs de package doivent donc fournir aux utilisateurs une méthode pour réinstaller le produit et pour définir les modes de la propriété [**REINSTALLMODE**](reinstallmode.md) . Il existe trois façons de déclencher la réinstallation :

-   Exécutez et configurez la réinstallation par le biais de l’interface utilisateur en créant un package qui utilise l' [*interface utilisateur complète*](f-gly.md).
-   Exécutez la réinstallation à partir de la ligne de commande en utilisant **msiexec/f** et sélectionnez les modes dans la liste de l' [option de ligne de commande](command-line-options.md) **/f** .
-   Demander à l’application d’appeler [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) ou [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

Le bit ne doit être utilisé qu’avec des conditions basées sur les États de l’ordinateur. N’utilisez pas avec des conditions basées sur les États utilisateur ou les propriétés définies sur la ligne de commande, car cela peut obliger le programme d’installation à exiger une réinstallation du produit à chaque utilisation par un autre utilisateur.

> [!Note]
> À moins que le bit transitif de la colonne attributs ne soit défini pour un composant, le composant reste activé une fois installé, même si l’instruction conditionnelle dans la colonne condition prend la valeur false lors d’une installation de maintenance ultérieure du produit.
> 
> Dans la plupart des cas, si une application comprend des composants transitifs, Windows Installer nécessite que la source de l’application répare ou met à niveau l’application. Dans ce cas, le CD-ROM de restauration du système fourni par un fabricant d’équipements d’origine ne fonctionne pas et une source d’installation réelle doit être fournie pour l’application.

 

 

 



