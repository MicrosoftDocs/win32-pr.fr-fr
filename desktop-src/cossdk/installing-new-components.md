---
description: pour ajouter des composants au dossier composants d’une application com+, vous pouvez soit utiliser l’assistant installation de composant com+, soit faire glisser .dll fichiers qui contiennent les composants à partir de l’explorateur de Windows et les déposer dans l’application.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Installation de nouveaux composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292071"
---
# <a name="installing-new-components"></a>Installation de nouveaux composants

pour ajouter des composants au dossier **composants** d’une application com+, vous pouvez soit utiliser l’assistant installation de composant com+, soit faire glisser .dll fichiers qui contiennent les composants à partir de l’explorateur de Windows et les déposer dans l’application.

Si vous utilisez l’Assistant Installation de composant COM+, vous pouvez installer un nouveau composant, qui inscrit le composant sur l’ordinateur, ou importer des composants qui ont déjà été inscrits. Des composants peuvent être ajoutés à des applications vides ou à des applications existantes.

**Pour ajouter un composant à une application COM+**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur qui héberge l’application COM+.

2.  Ouvrez le dossier **applications com+** pour cet ordinateur, puis sélectionnez l’application dans laquelle vous souhaitez installer le ou les composants.

3.  Ouvrez le dossier de l’application et sélectionnez **composants**.

4.  Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **composant**. Vous pouvez également cliquer avec le bouton droit sur le dossier **composants** , pointer sur **nouveau**, puis cliquer sur **composant**.

5.  Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **importer ou installer un composant** , cliquez sur **installer de nouveaux composants** .

6.  Dans la boîte de dialogue **installer les nouveaux composants** , cliquez sur **Ajouter** pour rechercher le composant que vous souhaitez ajouter.

7.  Dans la boîte de dialogue **Sélectionner les fichiers à installer** , tapez le nom du fichier du composant à installer ou sélectionnez un nom de fichier dans la liste affichée. Cliquez sur **Ouvrir**.

    Une fois que vous avez ajouté les fichiers, la boîte de dialogue **installer les nouveaux composants** affiche les fichiers que vous avez ajoutés et leurs composants associés. Si vous activez la case à cocher **Détails** , vous obtenez plus d’informations sur le contenu du fichier et les composants qui ont été trouvés.

    > [!Note]  
    > Les composants COM non configurés doivent avoir une bibliothèque de types. Si COM+ ne trouve pas la bibliothèque de types de votre composant, votre composant n’apparaîtra pas dans la liste. Vous pouvez également supprimer un fichier de la liste **fichiers à installer** en le sélectionnant et en cliquant sur **supprimer**.

     

8.  Cliquez sur **suivant**, puis sur **Terminer** pour installer le composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Copier des composants](copying-components.md)
</dt> <dt>

[Création d’une application COM+](creating-a-new-com--application.md)
</dt> <dt>

[Suppression d’une application COM+](deleting-a-com--application.md)
</dt> <dt>

[Importation de composants](importing-components.md)
</dt> <dt>

[Déplacement des composants](moving-components.md)
</dt> <dt>

[Suppression d’un composant d’une application COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



