---
description: vous pouvez utiliser l’outil d’administration Services de composants pour importer dans des applications spécifiques des composants qui ont déjà été inscrits sur votre ordinateur en tant que composants COM dans le registre Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importation de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69385e14759716e775ce608307b3ef12828e5f628539e58a1d214d6c11506e66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953979"
---
# <a name="importing-components"></a>Importation de composants

vous pouvez utiliser l’outil d’administration Services de composants pour importer dans des applications spécifiques des composants qui ont déjà été inscrits sur votre ordinateur en tant que composants COM dans le registre Windows. L’importation d’un composant n’installe pas les informations d’interface ou de méthode requises pour définir les propriétés de l’interface ou pour configurer l’accès au composant à partir d’un client distant. Par conséquent, si possible, vous devez installer plutôt que d’importer des composants non configurés.

> [!Note]  
> Lorsque vous importez un composant dans une application COM+, COM+ ne remplit pas les informations d’interface et de méthode du composant. Lors de l’exportation d’un proxy d’application, COM+ ne fournit pas d’informations de marshaling (bibliothèques de types ou proxy/stubs) pour une partie ou l’ensemble des interfaces. L’exportation de proxys d’application contenant des composants importés échouera ou entraînera l’émission d’un avertissement.

 

**Pour importer un composant dans une application COM+**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur qui héberge l’application COM+.

2.  Ouvrez le dossier **applications com+** pour cet ordinateur, puis sélectionnez l’application dans laquelle vous souhaitez installer le composant.

3.  Ouvrez le dossier de l’application et sélectionnez **composants**.

4.  Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **composant**. Vous pouvez également cliquer avec le bouton droit sur le dossier **composants** , pointer sur **nouveau**, puis cliquer sur **composant**.

5.  Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **importer ou installer un composant** , cliquez sur **importer des composants qui sont déjà inscrits**.

6.  Dans la boîte de dialogue **choisir les composants à importer** , activez la case à cocher **Détails** pour afficher des informations complètes sur les composants déjà inscrits. Sélectionnez le ou les composants que vous souhaitez importer dans la liste affichée, puis cliquez sur **suivant**.

7.  Cliquez sur **Terminer**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Copier des composants](copying-components.md)
</dt> <dt>

[Création d’une application COM+](creating-a-new-com--application.md)
</dt> <dt>

[Suppression d’une application COM+](deleting-a-com--application.md)
</dt> <dt>

[Installation de nouveaux composants](installing-new-components.md)
</dt> <dt>

[Déplacement des composants](moving-components.md)
</dt> <dt>

[Suppression d’un composant d’une application COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



