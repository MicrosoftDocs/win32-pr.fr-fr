---
description: Les capteurs logiques fournissent des données sans dépendre des périphériques matériels.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: À propos des capteurs logiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013567"
---
# <a name="about-logical-sensors"></a>À propos des capteurs logiques

Les *capteurs logiques* fournissent des données sans dépendre des périphériques matériels. Par exemple, un capteur logique peut fournir des données sur l’emplacement actuel de l’utilisateur à l’aide d’un service qui recherche une adresse IP dans une table. Les capteurs logiques sont implémentés en tant que pilotes de capteur. pour plus d’informations sur la façon d’implémenter un pilote de capteur, consultez le Kit de pilotes Windows.

Une fois qu’un capteur logique est installé sur l’ordinateur de l’utilisateur, vous pouvez l’utiliser de la même façon qu’un capteur basé sur le matériel. L’API de capteur fournit une interface [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) pour représenter le capteur logique, et votre programme peut demander des données à l’aide des mêmes mécanismes que ceux que vous utiliseriez pour n’importe quel autre type de capteur. Les capteurs logiques peuvent également utiliser les catégories, les types de données, les types de données, les propriétés et les événements de capteur définis par la plateforme. Ou vous pouvez définir des valeurs personnalisées.

L’interface [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) permet aux développeurs qui créent des capteurs logiques de gérer les connexions au capteur et à la plateforme d’emplacement.

> [!Note]  
> Comme avec d’autres pilotes, l’installation ou la désinstallation d’un pilote de capteur logique requiert des privilèges d’administrateur.

 

Pour essayer d’utiliser un exemple de capteur logique, consultez [à propos des exemples et des outils](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Gestion des capteurs logiques

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) présente les méthodes suivantes :

-   [**Connexion**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Déconnecter**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Désinstaller l’interface**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

lorsque vous appelez [**Connecter**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), l’API de capteur crée une instance du pilote de capteur, si elle n’existe pas déjà, puis connecte le capteur logique à la plateforme. Cela signifie que le capteur logique apparaît avec d’autres capteurs dans le panneau de configuration **emplacement et autres capteurs** . Lorsque vous appelez [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), l’API Sensor déconnecte le capteur logique et le supprime du panneau de configuration. L’appel de **Disconnect** ne supprime pas le capteur logique de **Gestionnaire de périphériques**. par conséquent, les appels futurs à **Connecter** entraînent une connexion beaucoup plus rapide au capteur logique.

Pour supprimer un capteur logique, vous devez appeler [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). La désinstallation d’un capteur logique supprime le capteur de **Gestionnaire de périphériques**. Étant donné que les périphériques de capteur logique existent uniquement en mémoire, un capteur logique est désinstallé lorsque l’utilisateur redémarre Windows.

L’API de capteur identifie un capteur logique particulier par son *ID logique*, qui est un **GUID**. Chaque fois que vous vous connectez à un capteur logique particulier, vous devez fournir un ID logique. Chaque fois que vous déconnectez ou désinstallez un capteur particulier, vous devez fournir le même ID logique que celui que vous avez utilisé pour vous connecter. Si vous vous connectez plusieurs fois au même pilote de capteur logique en utilisant différents ID logiques, vous allez créer une instance distincte du capteur logique pour chaque nouvel ID logique. Même si vous appelez [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) pour chaque ID logique, ces instances sont conservées dans **Gestionnaire de périphériques** jusqu’à ce que vous appeliez [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) pour chaque capteur logique, ou que l’utilisateur redémarre Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de capteurs logiques](using-logical-sensors.md)
</dt> </dl>

 

 
