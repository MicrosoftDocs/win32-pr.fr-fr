---
description: Dans certains cas, les auteurs peuvent décider de rompre les règles de création de composants, comme indiqué dans Organisation des applications en composants et modification du code du composant.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: Que se passe-t-il si les règles des composants sont rompues ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f830fa402da44be992d74adc957d88a19442dcbb51173a87e79fa2266552a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498765"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>Que se passe-t-il si les règles des composants sont rompues ?

Dans certains cas, les auteurs peuvent décider de rompre les règles de création de composants, comme indiqué dans [Organisation des applications en composants](organizing-applications-into-components.md) et [modification du code du composant](changing-the-component-code.md). Les auteurs doivent être conscients des conséquences possibles de cette action et doivent sinon garantir que leurs composants ne sont jamais installés lorsqu’ils peuvent endommager d’autres applications ou composants sur le système de l’utilisateur.

La liste suivante décrit les façons dont les auteurs rompent parfois les règles de composant recommandées et les conséquences possibles.

Un auteur ajoute des ressources à un composant sans modifier le code du composant.

-   Les produits installés avec l’ancien composant n’ont pas d’informations sur les ressources ajoutées dans leur base de données d’installation.
-   Si un nouveau produit contenant les ressources ajoutées et un ancien produit est installé sur le même ordinateur, les ressources peuvent être conservées en arrière-plan si le nouveau produit est désinstallé en premier.
-   Un ancien produit sans les ressources ajoutées ne peut pas réparer la version la plus récente du composant. La réinstallation de l’ancien produit ne restaure pas les ressources ajoutées.

Un auteur supprime les ressources d’un composant sans modifier le code du composant.

-   Les produits installés avec le nouveau composant n’ont pas d’informations sur les ressources supprimées dans leur base de données d’installation.
-   Si un ancien produit, contenant les informations sur les ressources et un nouveau produit, est installé sur le même ordinateur, les ressources peuvent être conservées en arrière-plan si l’ancien produit est désinstallé en premier.
-   Un nouveau produit avec les ressources supprimées ne peut pas réparer l’ancienne version du produit. La réinstallation du nouveau produit ne restaure pas les ressources supprimées.

Un auteur comprend un fichier qui n’est pas compatible avec les versions précédentes sans modifier le code du composant.

Si un fichier incompatible est inclus dans un composant sans modifier le code du composant, le contrôle de [version de fichier par défaut](default-file-versioning.md) entraîne le remplacement du fichier d’origine par le fichier incompatible le plus récent. Cela peut endommager les anciens produits qui ont besoin du fichier d’origine. Il peut également empêcher le programme d’installation de réparer l’ancien produit, car la version du fichier de chemin d’accès de clé d’un composant détermine la version du composant. Si une version plus récente du fichier de chemin d’accès de clé est déjà installée, le programme d’installation n’installe pas une version antérieure du composant. Pour plus d’informations, consultez règles de contrôle de [version de fichier](file-versioning-rules.md). Dans ce cas, le nouveau produit doit être supprimé avant que l’ancien produit puisse être réinstallé.

-   Le contrôle de [version de fichier par défaut](default-file-versioning.md) entraîne le remplacement du fichier d’origine par le programme d’installation le plus récent.
-   Les anciens produits qui ont besoin du fichier d’origine sont endommagés.
-   Il peut également empêcher le programme d’installation de réparer l’ancien produit, car la version du fichier de chemin d’accès de clé d’un composant détermine la version du composant. Si une version plus récente du fichier de chemin d’accès de clé est déjà installée, le programme d’installation n’installe pas l’ancienne version du composant. Pour plus d’informations, consultez règles de contrôle de [version de fichier](file-versioning-rules.md). Dans ce cas, le nouveau produit doit être supprimé avant que l’ancien produit puisse être réinstallé.

Un auteur comprend la même ressource dans deux composants différents.

Si deux composants ont une ressource sous le même nom et le même emplacement et que les deux composants sont installés dans le même dossier, la suppression de l’un ou l’autre des composants supprime la ressource commune, ce qui endommage le composant restant.

-   La désinstallation de l’un des deux composants supprime la ressource et interrompt l’autre composant.
-   Le mécanisme de décompte de références des composants est endommagé.

 

 



