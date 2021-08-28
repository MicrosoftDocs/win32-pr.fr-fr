---
description: Il existe de nombreuses façons de gérer la distribution des messages SOAP reçus au service approprié. Les deux mécanismes les plus simples sont la répartition au niveau du transport et la répartition des adresses et des actions.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Distribution des messages SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579c01d03a76fcadc1ee82a270c8e222cbf68aa739d10bed0749bb82bcda80ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030249"
---
# <a name="dispatching-soap-messages"></a>Distribution des messages SOAP

Il existe de nombreuses façons de gérer la distribution des messages SOAP reçus au service approprié. Les deux mécanismes les plus simples sont la répartition au niveau du transport et la répartition des adresses et des actions.

## <a name="transport-level-dispatch"></a>Distribution au niveau du transport

Avec la distribution au niveau du transport, le serveur HTTP sous-jacent (par exemple, l' [API http](/windows/desktop/Http/http-api-start-page)) est utilisé pour gérer le routage des demandes vers l’appareil et ses services. Le serveur fournit une URL différente pour chaque service et pour l’appareil, et des récepteurs différents sont enregistrés pour chaque URL. Cela permet à du code d’être conçu de telle sorte que chaque service soit isolé de l’autre, s’exécutant en tant que composants distincts au sein du même processus ou exécuté en tant que processus distincts.

La distribution au niveau du transport présente quelques avantages. Les messages peuvent être distribués au composant approprié sans analyser au préalable l’enveloppe SOAP ou le corps du message. En outre, le mécanisme existant pour le routage des messages fournis par la plupart des implémentations de serveur HTTP peut être réutilisé, ce qui signifie que le code de distribution personnalisé n’est pas nécessaire. Il isole également le code de traitement SOAP entre les services, ce qui fournit un niveau de sécurité, car les services sécurisés évitent que les messages transitent par le code commun.

## <a name="address-and-action-dispatch"></a>Distribution d’adresse et d’action

L’adresse et la répartition d’action s’appuient sur les en-têtes SOAP pour déterminer le service approprié vers lequel le message est distribué. Ce modèle peut également utiliser des informations supplémentaires, telles que les paramètres de référence, pour faciliter la distribution.

Ce modèle encourage la réutilisation de code dans une pile de messagerie en couches, car tout le code jusqu’au processeur SOAP est partagé par tous les services. En outre, les adresses de transport distinctes pour les services ne sont pas requises, ce qui signifie que des adresses UUID peuvent être utilisées pour les points de terminaison de service. L’adresse et la répartition des actions se traduisent également plus directement en un modèle de programmation. Les développeurs peuvent connecter des services et des appareils dans un composant unique qui gère le routage, plutôt que d’avoir à lier une couche HTTP ou à créer des composants distincts pour chaque service.

 

 
