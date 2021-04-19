---
description: Les composants CRM peuvent être installés dans une application serveur COM+ ou une application de bibliothèque COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuration des composants CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514549"
---
# <a name="configuring-com-crm-components"></a>Configuration des composants CRM de COM+

Les composants CRM peuvent être installés dans une application serveur COM+ ou une application de bibliothèque COM+. Toutefois, ils doivent toujours s’exécuter dans une application serveur COM+. S’ils sont installés dans une application de bibliothèque COM+, ils ne peuvent pas être utilisés dans les processus client.

Si les composants CRM sont installés dans une application de bibliothèque, ils sont disponibles pour plusieurs applications serveur. S’il est installé dans une application serveur spécifique, il est uniquement disponible pour cette application serveur spécifique.

Pour activer l’utilisation d’un CRM dans une application serveur, procédez comme suit :

1.  Dans services de composants, sous la page Propriétés de l’application serveur, cliquez sur l’onglet **avancé** .

2.  Sélectionnez l’option **activer les gestionnaires de ressources de compensation** pour cette application serveur. Si cette option n’est pas sélectionnée, les tentatives d’utilisation d’un CRM au sein de cette application serveur échoueront.

    > [!Note]  
    > S’il est installé dans une application de bibliothèque, il n’est pas nécessaire de sélectionner l’option **activer les gestionnaires de ressources de compensation** pour cette application de bibliothèque, mais cette option doit être sélectionnée pour l’application serveur dans laquelle le CRM est destiné à être exécuté.

     

Il est recommandé d’installer les composants de travail CRM et du compensateur CRM pour un CRM spécifique dans la même application.

Les paramètres recommandés pour les composants CRM sont les suivants :



| Composant           | Paramètres                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM Worker**      | transaction = requiredsync = yesJIT = yesthreading Model = both (ou modèle de thread = Apartment)     |
| **Compensateur CRM** | transaction = disabledsync = disabledJIT = nothreading Model = both (ou modèle de thread = Apartment) |



 

> [!Note]  
> Les composants qui utilisent le CRM doivent spécifier explicitement un modèle de thread lorsqu’ils sont inscrits. La valeur par défaut « principal thread Apartment » n’est pas prise en charge. Les deux seuls modèles de thread pris en charge sont Apartment et Both.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



