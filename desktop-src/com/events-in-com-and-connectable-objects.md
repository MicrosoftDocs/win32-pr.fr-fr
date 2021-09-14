---
title: Événements dans les objets COM et connectables
description: Lorsqu’un programme détecte un événement qui s’est produit, il peut notifier ses clients.
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921792"
---
# <a name="events-in-com-and-connectable-objects"></a>Événements dans les objets COM et connectables

Lorsqu’un programme détecte un événement qui s’est produit, il peut notifier ses clients. Par exemple, si un programme de cotations boursières détecte une modification du prix d’un stock, il peut informer tous les clients de la modification. Ce processus de notification est appelé *déclenchement d’un événement*.

Avec COM, les objets serveur peuvent utiliser des événements COM pour déclencher des événements sans informations sur les objets qui seront avertis. Les objets peuvent également utiliser des *objets connectables* pour gérer des informations détaillées sur les clients qui ont demandé des notifications.

Les objets connectables COM fournissent des interfaces sortantes à leurs clients en plus de leurs interfaces entrantes. Par conséquent, les objets et leurs clients peuvent être engagés dans une communication bidirectionnelle. Les interfaces entrantes sont implémentées sur un objet et reçoivent les appels des clients externes d’un objet, tandis que les interfaces sortantes sont implémentées sur le récepteur du client et reçoivent les appels de l’objet. L’objet définit une interface qu’il souhaite utiliser, et le client l’implémente.

Un objet définit ses interfaces entrantes et fournit des implémentations de ces interfaces. Les interfaces entrantes sont disponibles pour les clients via la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) de l’objet. Les clients appellent les méthodes d’une interface entrante sur l’objet, et l’objet effectue les actions souhaitées pour le compte du client.

Les interfaces sortantes sont également définies par un objet, mais le client fournit les implémentations des interfaces sortantes sur un objet récepteur créé par le client. L’objet appelle ensuite les méthodes de l’interface sortante sur l’objet récepteur pour informer le client des modifications apportées à l’objet, pour déclencher des événements dans le client, pour demander des éléments au client, ou, en fait, pour toutes les finalités du créateur de l’objet.

Un exemple d’interface sortante est une interface IButtonSink définie par un contrôle de bouton de commande pour notifier ses clients de ses événements. Par exemple, l’objet bouton appelle IButtonSink :: OnClick sur l’objet récepteur du client lorsque l’utilisateur clique sur le bouton à l’écran. Le contrôle Button définit l’interface sortante. Pour qu’un client du bouton gère l’événement, le client doit implémenter cette interface sortante sur un objet récepteur, puis connecter ce récepteur au contrôle bouton. Ensuite, lorsque des événements se produisent dans le bouton, le bouton appelle le récepteur, auquel cas le client peut exécuter toutes les actions qu’il souhaite assigner à ce clic de bouton.

Les objets connectables fournissent un mécanisme général pour la communication entre les clients. Tout objet qui souhaite exposer des événements ou des notifications de n’importe quel type peut utiliser cette technologie. En plus de la technologie générale de l’objet connectable, COM fournit de nombreuses interfaces de site et de récepteur spécialement utilisées par les objets pour informer les clients d’événements spécifiques qui présentent un intérêt pour le client. Par exemple, [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) peut être utilisé par des objets pour notifier des clients de données et afficher des modifications dans l’objet.

Pour plus d'informations, voir les rubriques suivantes :

-   [Architecture des objets connectables](architecture-of-connectable-objects.md)
-   [Interfaces d’objets connectables](connectable-object-interfaces.md)

 

 




