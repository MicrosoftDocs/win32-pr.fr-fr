---
description: Lorsque vous spécifiez les composants d’une installation, les auteurs de packages doivent suivre les règles générales pour l’Organisation des composants décrites dans Organisation des applications en composants.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Modification du code du composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092289"
---
# <a name="changing-the-component-code"></a>Modification du code du composant

Lorsque vous spécifiez les [composants](windows-installer-components.md) d’une installation, les auteurs de packages doivent suivre les règles générales pour l’Organisation des composants décrites dans [Organisation des applications en composants](organizing-applications-into-components.md). Les auteurs peuvent avoir besoin d’introduire de nouveaux composants ou de modifier des composants existants. Si l’ajout, la suppression ou la modification de ressources crée effectivement un nouveau composant, le code du composant doit également être modifié.

## <a name="creating-a-new-component"></a>Création d’un composant

Introduisez un nouveau composant et affectez-lui un code de composant unique lorsque vous effectuez l’une des modifications suivantes :

-   Toute modification qui n’a pas été affichée par le test pour être compatible avec les versions précédentes du composant. Dans ce cas, vous devez également modifier le nom ou l’emplacement cible de chaque ressource dans le composant.
-   Modification du nom ou de l’emplacement cible d’un fichier, d’une clé de Registre, d’un raccourci ou d’une autre ressource dans le composant. Dans ce cas, vous devez également modifier le nom ou l’emplacement cible de chaque ressource dans le composant.
-   Ajout ou suppression d’un fichier, d’une clé de Registre, d’un raccourci ou d’une autre ressource du composant. Dans ce cas, vous devez également modifier le nom ou l’emplacement cible de chaque ressource dans le composant.
-   Recompilation d’un composant 32 bits dans un composant 64 bits.

Lors de l’introduction d’un nouveau composant, les auteurs doivent effectuer l’une des opérations suivantes pour s’assurer que le composant n’est pas en conflit avec les composants existants :

-   Modifiez le nom ou l’emplacement cible des ressources qui peuvent être installées sous le même nom et l’emplacement cible par un autre composant.
-   Dans le cas contraire, assurez-vous que le nouveau composant n’est jamais installé dans le même dossier qu’un autre composant qui a une ressource sous un nom et un emplacement communs. Cela comprend les versions localisées des fichiers portant le même nom de fichier. Pour plus d’informations, consultez [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md).
-   Lorsque vous modifiez le code d’un composant existant, modifiez également le nom ou l’emplacement cible de chaque fichier, clé de Registre, raccourci et autre ressource dans le composant.

### <a name="creating-a-new-version-of-a-component"></a>Création d’une nouvelle version d’un composant

La nouvelle version d’un composant se voit attribuer le même code de composant qu’un autre composant existant. La modification d’un composant sans modifier le code du composant n’est facultative que dans les cas suivants :

-   Les modifications apportées au composant ont été prouvées par des tests pour une compatibilité descendante avec toutes les versions précédentes du composant.
-   L’auteur peut garantir que la nouvelle version du composant ne sera jamais installée sur un système où elle serait en conflit avec les versions précédentes du composant ou les applications nécessitant une version antérieure. Pour plus d’informations, consultez [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md).

Le code de composant d’une nouvelle version d’un composant ne doit pas être modifié quand deux composants partagent des ressources, tels que des valeurs de Registre, des fichiers ou des raccourcis.

 

 



