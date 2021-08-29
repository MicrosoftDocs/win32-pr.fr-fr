---
description: Pour que les abonnés puissent trouver une classe d’événements et s’y abonner, les classes d’événements doivent être inscrites dans le catalogue COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Inscription d’une classe d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cceddaf01cff9677bb36ecc5315c15c1fa59e2c21046c3b7cd2bb4f3749f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047297"
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

 

 



