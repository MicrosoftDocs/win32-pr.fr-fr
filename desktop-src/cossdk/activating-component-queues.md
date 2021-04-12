---
description: Activation des files d’attente de composants
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Activation des files d’attente de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393052"
---
# <a name="activating-component-queues"></a>Activation des files d’attente de composants

Le fait d’appeler des méthodes sur un composant en file d’attente n’exécute pas directement la méthode. Au lieu de cela, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshale et stocke les appels de méthode et les paramètres dans une file d’attente où ils sont récupérés et exécutés ultérieurement par le composant mis en file d’attente. Contrairement à l’activation d’un objet DCOM distant, le composant mis en file d’attente n’est pas instancié quand une méthode est appelée. Il s’agit de l’idée de base de l’utilisation des composants en file d’attente : les composants en file d’attente n’ont pas besoin d’être instanciés en même temps que l’application appelante.

> [!Note]  
> Les descriptions d’activation d’une application en file d’attente supposent que l’application est marquée comme étant en file d’attente et que la case à cocher écouteur est activée.

 

Vous pouvez utiliser des scripts pour démarrer et arrêter une application en file d’attente. Vous pouvez placer le script sous le contrôle du planificateur de tâches pour l’exécuter en fonction des besoins. Par exemple, le script peut être exécuté lors du redémarrage du système si les applications doivent être disponibles de manière permanente. Si l’application doit traiter les transactions en mode batch, le script peut être exécuté à une heure donnée chaque jour conjointement à un script d’arrêt pour s’assurer que le traitement par lots s’arrête à un moment précis.

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour démarrer une application en file d’attente, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Cliquez avec le bouton droit sur l’application dont vous souhaitez activer la file d’attente.

3.  Cliquez sur **Start**.

## <a name="visual-basic"></a>Visual Basic

Consultez l’exemple COMAdminCatalog. StartApplication.

## <a name="cc"></a>C/C++

Consultez l’exemple [**ICOMAdminCatalog :: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du moniker de la file d’attente](using-the-queue-moniker.md)
</dt> </dl>

 

 



