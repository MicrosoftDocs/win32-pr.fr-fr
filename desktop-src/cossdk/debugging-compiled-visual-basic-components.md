---
description: Étant donné que, dans de nombreux cas, vous pourrez déboguer uniquement une partie de vos fonctionnalités de composants dans l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic une fois qu’ils ont été compilés. Étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Débogage de composants Visual Basic compilés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110642"
---
# <a name="debugging-compiled-visual-basic-components"></a>Débogage de composants Visual Basic compilés

Étant donné que, dans de nombreux cas, vous serez en mesure de déboguer uniquement une partie des fonctionnalités de votre composant au sein de l’environnement Microsoft Visual Basic, il y aura des situations dans lesquelles vous devrez déboguer des composants générés avec Visual Basic après qu’ils ont été compilés. Étant donné que l’environnement de Visual Basic ne l’active pas, vous devez utiliser à la place l’environnement Microsoft Visual C++.

**Pour déboguer un composant Visual Basic dans l’environnement Visual C++**

1.  Dans Visual Basic 6,0, ouvrez le projet Visual Basic que vous souhaitez déboguer.

2.  Dans le menu **fichier** , cliquez sur **créer un YourProject.dll**.

3.  Dans la boîte de dialogue **créer un projet** , cliquez sur **options**.

4.  Dans la boîte de dialogue **Propriétés du projet** , sous l’onglet **compiler** , cliquez sur **compiler en code natif** et **aucune optimisation** , puis activez la case à cocher **créer des informations de débogage symboliques** .

5.  Cliquez sur **OK**, puis de nouveau sur **OK** pour compiler votre projet.

6.  Déplacez la DLL compilée vers l’emplacement où les applications COM+ sont normalement installées.

    > [!Note]  
    > Si vous ne déplacez pas la DLL, vous pouvez recevoir un message d’erreur vous informant que les informations de débogage symboliques pour la DLL n’ont pas pu être localisées. Si vous avez des difficultés à faire en sorte que le débogueur s’arrête à des points d’arrêt dans votre composant, vérifiez que la DLL se trouve dans le répertoire des packages standard, supprimez le composant de son package, puis ajoutez de nouveau le composant.

     

7.  Démarrez Visual C++.

8.  Dans le menu **fichier** , cliquez sur **ouvrir l’espace de travail**.

9.  Dans la boîte de dialogue **ouvrir l’espace de travail** , définissez **fichiers de type** sur **tous les fichiers ( \* . \* )**, sélectionnez votre composant compilé, puis cliquez sur **ouvrir**.

10. Dans le menu **fichier** , cliquez sur **ouvrir** (pas sur **ouvrir l’espace de travail**) et ouvrez le module de Visual Basic (. bas), le formulaire (. frm) ou la classe (. CLS) que vous souhaitez déboguer.

11. Dans le menu **projet** , cliquez sur **paramètres**.

12. Dans la boîte de dialogue **paramètres du projet** , sous l’onglet **Déboguer** , sélectionnez **général** dans la zone **catégorie** .

13. Dans la zone **exécutable pour la session de débogage** , entrez le chemin d’accès complet de Dllhost.exe, suivi d’un argument spécifiant l’ID de processus de l’application com+ contenant le composant. L’ID de processus se trouve sous l’onglet **général** de la boîte de dialogue **Propriétés** de l’application com+. Voici un exemple : C : \\ winnt \\ system32 \\Dllhost.exe/ProcessId : { <processID> }.

14. Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du débogage des Visual Basic COM+ avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Débogage dans l’IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



