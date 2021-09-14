---
title: Planification des commandes
description: Une priorité est associée à chaque commande.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193635"
---
# <a name="command-scheduling"></a>Planification des commandes

## <a name="command-scheduling"></a>Planification des commandes

Les commandes peuvent être envoyées au TBS à partir de plusieurs contextes à tout moment. Toutefois, un module de plateforme sécurisée physique ne peut traiter qu’une seule commande à la fois, et certaines commandes peuvent s’exécuter pendant une période de temps considérable. Lorsque plusieurs commandes sont en attente, le TBS décide de la commande à envoyer au module de plateforme sécurisée. Lorsqu’une commande est envoyée, chaque commande est associée à une priorité. Le TBS utilise ces priorités pour déterminer la commande en attente à envoyer chaque fois que le module de plateforme sécurisée est gratuit. Les quatre niveaux de priorité sont faible, normal, élevé et système. Les applications doivent utiliser une priorité faible, normale ou élevée. Bien que les commandes de priorité élevée soient généralement exécutées avant les commandes de faible priorité, le planificateur de commandes TBS a une stratégie d’antériorité qui finit par donner une priorité très élevée aux commandes qui ont été bloquées pendant de longues périodes.

## <a name="context-management"></a>Gestion de contexte

Lorsqu’une \_ commande SAVECONTEXT TPM ou TPM2 ContextSave est soumise avec un descripteur virtuel à une ressource gérée par le TBS, le TBS exécute la commande appropriée sur la ressource physique et retourne le résultat à l’appelant si la ressource est physiquement présente dans le module de plateforme sécurisée. Si la ressource n’est pas physiquement présente dans le module de plateforme sécurisée, le prétraitement de la \_ commande TPM SaveContext ou TPM2 \_ ContextSave entraîne le rechargement de la ressource, auquel cas le contexte est enregistré et retourné à l’appelant. Si la ressource enregistrée est d’un type qui est normalement vidé automatiquement du module de plateforme sécurisée après l’enregistrement, le TBS invalide la ressource virtuelle à la fin de cette commande. Lorsqu’une \_ commande TPM LoadContext ou TPM2 \_ ContextLoad est soumise au tbs, le TBS exécute la commande immédiatement. Si la commande se termine correctement, le TBS virtualise le handle de ressource et passe le flux d’octets GPC résultant à l’appelant. Lorsqu’une \_ commande TPM FlushSpecific ou TPM2 \_ FlushContext est soumise avec un descripteur virtuel à une ressource gérée par le TBS, le TBS exécute une \_ commande TPM FlushSpecific ou TPM2 \_ FlushContext pour supprimer la ressource du module de plateforme sécurisée si elle est physiquement présente. Dans ce cas, le TBS invalide la ressource virtuelle et retourne le résultat de la commande flush à l’appelant. Si la ressource n’est pas physiquement présente dans le module de plateforme sécurisée (TPM), le prétraitement de la \_ commande TPM FlushSpecific ou TPM2 \_ FlushContext chargera la ressource qui correspond au handle virtuel, mais elle sera vidée lors du traitement réel de la commande. Le service TBS ne prend pas en charge le \_ bit TPM KeyControlOwner ou la fonctionnalité keepHandle de l' \_ opération LoadContext TPM, de sorte qu’il ne donne pas à une ressource le même handle que celui qu’il avait avant l’enregistrement du contexte.

## <a name="other-commands"></a>Autres commandes

Les commandes qui ne sont pas mentionnées dans cette documentation sont traitées en remplaçant les handles de clé virtuelle par des handles de clé physique (si nécessaire) et en les envoyant au module de plateforme sécurisée. Cette opération est effectuée après avoir effectué les opérations appropriées pour s’assurer que les ressources utilisées sont physiquement présentes sur le module de plateforme sécurisée. Aucun traitement spécial supplémentaire n’est effectué. Le TBS n’essaie pas d’améliorer la fidélité de la virtualisation en modifiant les données retournées du module de plateforme sécurisée dans le cadre d’une \_ requête TPM GetCapabilities ou TPM2 \_ GetCapability. Le TBS prend également en charge les commandes de présence physique TCG. Le TBS agit comme une transmission directe pour les commandes de présence physique ; aucun traitement spécial n’est effectué par le TBS lui-même.

## <a name="cleanup"></a>Nettoyage

Lorsqu’un contexte se termine, toutes les ressources physiques et virtuelles associées sont nettoyées afin qu’elles ne consomment plus de ressources système.

 

 




