---
description: Windows Le programme d’installation installe et supprime une application ou un produit dans des parties appelées composants.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organisation des applications en composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1398bbbacbdb15df148576ebf0904f7aec98354a4d417681a81f2195535f08d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129189"
---
# <a name="organizing-applications-into-components"></a>Organisation des applications en composants

Windows Le programme d’installation installe et supprime une application ou un produit dans des parties appelées [composants](windows-installer-components.md). Les composants sont des collections de ressources qui sont toujours installées ou supprimées comme une unité du système d’un utilisateur. Une ressource peut être un fichier, une clé de Registre, un raccourci ou tout autre fichier qui peut être installé. Un [GUID](guid.md)de code de composant unique est attribué à chaque composant.

Les auteurs des packages d’installation doivent uniquement créer des composants et des versions de composants qui peuvent être installés et supprimés sans endommager d’autres composants. En outre, la suppression d’un composant ne doit pas conserver derrière les ressources orphelines sur l’ordinateur de l’utilisateur, telles que les fichiers inutilisés, les clés de registre ou les raccourcis. Pour ce faire, les auteurs doivent respecter les règles générales suivantes lors de l’Organisation des ressources en composants :

-   Ne créez jamais deux composants qui installent une ressource sous le même nom et dans l’emplacement cible. Si une ressource doit être dupliquée dans plusieurs composants, modifiez son nom ou son emplacement cible dans chaque composant. Cette règle doit être appliquée entre les applications, les produits, les versions de produits et les sociétés.
-   Notez que la règle précédente signifie que deux composants ne doivent pas avoir le même fichier de chemin d’accès de clé. La valeur du chemin d’accès de la clé pointe vers un fichier ou dossier particulier appartenant au composant que le programme d’installation utilise pour détecter le composant. Si deux composants ont le même fichier de chemin d’accès de clé, le programme d’installation ne peut pas distinguer le composant installé. Toutefois, deux composants peuvent partager un dossier de chemin d’accès de clé.
-   Ne créez pas une version d’un composant qui n’est pas compatible avec toutes les versions précédentes du composant. Le composant peut être partagé par d’autres applications, produits, versions de produits et sociétés. Au lieu de cela, créez un nouveau composant.
-   Ne créez pas de composants contenant des ressources qui devront être installés dans plusieurs répertoires sur le système de l’utilisateur. Le programme d’installation installe toutes les ressources d’un composant dans le même répertoire. Il n’est pas possible d’installer des ressources dans des sous-répertoires.
-   N’incluez pas plus d’un serveur COM par composant. Si un composant contient un serveur COM, il doit s’agir du chemin d’accès à la clé du composant.
-   Ne spécifiez pas plusieurs fichiers par composant en tant que cible pour le menu **Démarrer** ou un raccourci sur le bureau.

Lorsque vous organisez une application en composants, les auteurs de package peuvent avoir besoin d’ajouter, de supprimer ou de modifier les ressources d’une installation existante. Dans ce cas, l’auteur doit décider s’il faut fournir les ressources en introduisant un nouveau composant ou en modifiant les composants existants et en les remplaçant par une nouvelle version du composant. Comme un code de composant unique doit être affecté lors de l’introduction d’un nouveau composant, les auteurs doivent déterminer si leurs modifications requièrent la modification du code du composant. Pour plus d’informations, consultez [modification du code du composant](changing-the-component-code.md), [que se passe-t-il si les règles des composants sont rompues ?](what-happens-if-the-component-rules-are-broken.md)et [définition des composants du programme d’installation](defining-installer-components.md).

 

 



