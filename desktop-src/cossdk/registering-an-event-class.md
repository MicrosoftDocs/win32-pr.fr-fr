---
description: Pour que les abonnés puissent trouver une classe d’événements et s’y abonner, les classes d’événements doivent être inscrites dans le catalogue COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Inscription d’une classe d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748292"
---
# <a name="registering-an-event-class"></a>Inscription d’une classe d’événements

Pour que les abonnés puissent trouver une classe d’événements et s’y abonner, les classes d’événements doivent être inscrites dans le catalogue COM+. COM+ requiert une bibliothèque de types décrivant les interfaces et les méthodes d’événement afin qu’il puisse faire correspondre et connecter correctement les abonnés et les serveurs de publication. La bibliothèque de types doit résider dans ou être accompagnée d’une DLL d’inscription automatique.

Vous pouvez utiliser l’outil d’administration Services de composants ou les fonctions d’administration COM+ pour inscrire une classe d’événements dans le catalogue COM+.

**Pour inscrire une classe d’événements à l’aide de l’outil d’administration Services de composants**

1.  Créer une application COM+.

2.  Ouvrez le dossier de l’application et sélectionnez **composants**.

3.  Dans le menu **Action**, cliquez sur **Nouveau**. (Vous pouvez également sélectionner le dossier **composants** , cliquer avec le bouton droit, pointer sur **nouveau**, puis cliquer sur **composant**.)

4.  Cliquez sur **installer de nouvelles classes d’événements**.

5.  Entrez le chemin d’accès à la DLL du composant de classe d’événements.

6.  Cliquez sur **OK**.

La classe d’événements est enregistrée dans le catalogue COM+ et peut être localisée par les abonnés intéressés par l’obtention des informations fournies par la classe d’événements. Pour plus d’informations sur l’enregistrement de la classe d’événements à l’aide des interfaces d’administration COM+, consultez [**ICOMAdminCatalog :: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription d’un abonnement](registering-a-subscription.md)
</dt> </dl>

 

 



