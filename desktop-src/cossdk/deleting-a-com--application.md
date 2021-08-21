---
description: À mesure que des applications existantes deviennent obsolètes ou ne sont plus utilisées, vous devrez peut-être les supprimer.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Suppression d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8332cd59ecde4115daa43ea97bc87d4354338e3ea94073317bfa293102deb78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047507"
---
# <a name="deleting-a-com-application"></a>Suppression d’une application COM+

À mesure que des applications existantes deviennent obsolètes ou ne sont plus utilisées, vous devrez peut-être les supprimer.

**Pour supprimer une application COM+**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur pour lequel vous souhaitez supprimer une application.

2.  Ouvrez le dossier **applications com+** pour l’ordinateur spécifié afin d’afficher toutes les applications.

3.  Sélectionnez l’application que vous souhaitez supprimer.

4.  Si vous avez sélectionné une application serveur, arrêtez l’application. Vous pouvez arrêter une application en la sélectionnant dans l’outil d’administration Services de composants, en cliquant avec le bouton droit, puis en cliquant sur **arrêter**. Si vous avez sélectionné une application de bibliothèque, assurez-vous que tous les processus qui utilisent actuellement cette application de bibliothèque sont arrêtés.

5.  Dans le menu **Action**, cliquez sur **Supprimer**. Vous pouvez également cliquer avec le bouton droit sur le nom de l’application, puis cliquer sur **supprimer**. Vous pouvez également supprimer une application en la sélectionnant dans l’outil d’administration Services de composants et en appuyant sur la touche **Suppr** , ou vous pouvez sélectionner l’application, cliquer avec le bouton droit, puis cliquer sur **supprimer**.

6.  Cliquez sur **Oui** lorsque vous êtes invité à confirmer votre action.

en outre, si une application serveur ou un proxy d’application a été installé sur un ordinateur à l’aide de Windows Installer (comme décrit dans la section « installation d’Applications COM+ » du Guide d’Administration des Services de composants), vous pouvez la supprimer via l’utilitaire ajout/suppression de programmes du panneau de configuration de Microsoft Windows. ou vous pouvez supprimer une application serveur installée ou un proxy d’application à l’aide de la syntaxe de ligne de commande Windows Installer :

nom de l’application **msiexec-x** *\_ * * * .msi**

Ces méthodes sont particulièrement utiles pour supprimer des applications COM+ sur des ordinateurs clients qui n’exécutent pas l’outil d’administration Services de composants.

La suppression de l’application supprime également tous les composants contenus dans l’application. Si ces composants dépendent de ressources supplémentaires (connexions à la base de données, fichiers de données ou de texte, configuration de la racine virtuelle IIS, etc.), ces ressources doivent être supprimées par des mécanismes autres que l’outil d’administration Services de composants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Copier des composants](copying-components.md)
</dt> <dt>

[Création d’une application COM+](creating-a-new-com--application.md)
</dt> <dt>

[Importation de composants](importing-components.md)
</dt> <dt>

[Installation de nouveaux composants](installing-new-components.md)
</dt> <dt>

[Déplacement des composants](moving-components.md)
</dt> <dt>

[Suppression d’un composant d’une application COM+](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



