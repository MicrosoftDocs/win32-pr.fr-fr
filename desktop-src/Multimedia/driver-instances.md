---
title: Instances de pilote
description: Instances de pilote
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- pilotes installables, instances
- pilotes installables, instances multiples
- plusieurs instances de pilote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672593"
---
# <a name="driver-instances"></a>Instances de pilote

Windows autorise l’installation de plusieurs instances d’un pilote. Le système crée une instance du pilote à chaque ouverture du pilote et détruit l’instance lorsque le pilote est fermé. Les instances de pilote sont particulièrement utiles pour les pilotes installables qui prennent en charge plusieurs appareils ou qui sont ouverts par plusieurs applications ou par la même application plusieurs fois.

Pour aider le pilote à effectuer le suivi des instances, le système envoie un descripteur d’instance de pilote à chaque message de pilote une fois l’instance créée. Étant donné que ce handle identifie l’instance de façon unique, les pilotes installables associent souvent le handle à la mémoire et à d’autres ressources qu’ils ont spécifiquement allouées pour l’instance.

Lorsque la première instance est ouverte, le système envoie les messages de [**\_ chargement du DRV**](drv-load.md), [**DRV \_ Enable**](drv-enable.md)et [**DRV \_ Open**](drv-open.md) au pilote dans cet ordre. Le DRV \_ Load et le DRV \_ activent les messages informent le pilote qu’il est désormais en mémoire et qu’il est activé pour l’opération. Le \_ message DRV Open identifie le descripteur d’instance et peut inclure des informations de configuration pour l’instance. À chaque ouverture suivante d’une instance du même pilote, le système envoie uniquement un message DRV \_ Open.

Lors du traitement d’un message de chargement du DRV \_ , un pilote lit généralement les paramètres de configuration à partir du Registre, configure le pilote et tout matériel associé et alloue de la mémoire pour une utilisation par toutes les instances du pilote. Si un pilote ne peut pas terminer la configuration ou allouer de la mémoire, il retourne zéro pour demander au système de supprimer immédiatement le pilote de la mémoire et d’empêcher l’envoi des messages suivants. Lors du traitement du \_ message d’activation du DRV, le pilote prépare le matériel à la réception et au traitement des demandes d’entrée et de sortie (e/s). La préparation peut inclure l’installation de gestionnaires d’interruptions.

Lors du traitement du \_ message d’ouverture du DRV, le pilote alloue la mémoire ou les ressources requises par l’instance donnée du pilote, puis retourne une valeur différente de zéro. Le système utilise cette valeur différente de zéro comme *identificateur de pilote* dans les messages de pilote suivants pour l’instance. Le pilote peut utiliser cet identificateur à n’importe quel motif. Par exemple, certains pilotes utilisent un handle de mémoire pour l’identificateur pour accéder rapidement à la mémoire contenant des informations sur l’instance donnée.

De nombreux pilotes installables traitent le deuxième paramètre du DRV \_ Open message, ce qui donne au système et aux applications le moyen d’envoyer des informations supplémentaires au pilote lors de l’ouverture d’une instance. Le paramètre peut être une valeur unique ou une adresse d’une structure contenant un ensemble de valeurs. Lorsque le traitement \_ de DRV est ouvert, le pilote vérifie le paramètre pour déterminer s’il s’agit d’une valeur et utilise les valeurs données, le cas échéant, pour terminer la création de l’instance.

Le système envoie un message de [**\_ fermeture du DRV**](drv-close.md) chaque fois qu’une instance est fermée. Le handle d’instance envoyé avec le message identifie l’instance à fermer. Lorsque la dernière instance restante est fermée, le système envoie les \_ messages DRV Close, [**DRV \_ Disable**](drv-disable.md)et [**DRV \_ Free**](drv-free.md) dans cet ordre. Le \_ message de fermeture du DRV indique au pilote de fermer l’instance, et les \_ messages DRV Disable et DRV \_ Free informent le pilote qu’il est désormais désactivé et qu’il sera immédiatement libéré de la mémoire.

Lors du traitement du \_ message de fermeture du DRV, le pilote libère généralement la mémoire ou les ressources allouées pour l’instance. Lors du traitement du \_ message de désactivation du DRV, le pilote place tout le matériel dans un état inactif, ce qui peut inclure la suppression des gestionnaires d’interruptions. Lors du traitement du \_ message du DRV Free, le pilote libère la mémoire ou les ressources qui sont toujours allouées.

Les pilotes installables ne sont pas requis pour prendre en charge plusieurs instances. Un pilote peut empêcher la création d’une instance en retournant zéro pour le [**DRV \_ Open**](drv-open.md) message.

 

 




