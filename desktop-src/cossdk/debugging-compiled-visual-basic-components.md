---
description: étant donné que, dans de nombreux cas, vous pourrez déboguer uniquement une partie de vos fonctionnalités de composants dans l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic une fois qu’ils ont été compilés. étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: débogage de composants Visual Basic compilés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2dec15f90d14d534221193020417415d11ddec
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882990"
---
# <a name="debugging-compiled-visual-basic-components"></a>débogage de composants Visual Basic compilés

étant donné que, dans de nombreux cas, vous serez en mesure de déboguer uniquement une partie des fonctionnalités de votre composant au sein de l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic après qu’ils ont été compilés. étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.

**pour déboguer un composant Visual Basic dans l’environnement Visual C++**

1.  dans Visual Basic 6,0, ouvrez le projet Visual Basic que vous souhaitez déboguer.

2.  Dans le menu **fichier** , cliquez sur **créer un YourProject.dll**.

3.  dans la boîte de dialogue **créer un Project** , cliquez sur **Options**.

4.  dans la boîte de dialogue **propriétés du Project** , sous l’onglet **compiler** , cliquez sur **compiler en Code natif** et **aucune optimisation** , puis activez la case à cocher **créer des informations de débogage symboliques** .

5.  Cliquez sur **OK**, puis de nouveau sur **OK** pour compiler votre projet.

6.  Déplacez la DLL compilée vers l’emplacement où les applications COM+ sont normalement installées.

    > [!Note]  
    > Si vous ne déplacez pas la DLL, vous pouvez recevoir un message d’erreur vous informant que les informations de débogage symboliques pour la DLL n’ont pas pu être localisées. Si vous avez des difficultés à faire en sorte que le débogueur s’arrête à des points d’arrêt dans votre composant, vérifiez que la DLL se trouve dans le répertoire des packages standard, supprimez le composant de son package, puis ajoutez de nouveau le composant.

     

7.  Démarrez Visual C++.

8.  Dans le menu **fichier** , cliquez sur **ouvrir l’espace de travail**.

9.  Dans la boîte de dialogue **ouvrir l’espace de travail** , définissez **fichiers de type** sur **tous les fichiers ( \* . \* )**, sélectionnez votre composant compilé, puis cliquez sur **ouvrir**.

10. dans le menu **fichier** , cliquez sur **ouvrir** (pas sur **ouvrir l’espace de travail**) et ouvrez le module de Visual Basic (. bas), le formulaire (. frm) ou la classe (. cls) que vous souhaitez déboguer.

11. dans le menu **Project** , cliquez sur **Paramètres**.

12. dans la boîte de dialogue **Project Paramètres** , sous l’onglet **déboguer** , sélectionnez **général** dans la zone **catégorie** .

13. Dans la zone **exécutable pour la session de débogage** , entrez le chemin d’accès complet de Dllhost.exe, suivi d’un argument spécifiant l’ID de processus de l’application com+ contenant le composant. L’ID de processus se trouve sous l’onglet **général** de la boîte de dialogue **Propriétés** de l’application com+. Voici un exemple : C : \\ winnt \\ system32 \\Dllhost.exe/ProcessId : { &lt; ProcessID &gt; }.

14. Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[prise en charge du débogage des Visual Basic COM+ avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[débogage dans l’IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



