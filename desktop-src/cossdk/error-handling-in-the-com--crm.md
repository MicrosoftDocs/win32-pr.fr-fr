---
description: Gestion des erreurs dans le CRM COM+
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Gestion des erreurs dans le CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403671"
---
# <a name="error-handling-in-the-com-crm"></a>Gestion des erreurs dans le CRM COM+

Les applications serveur COM+ implémentent une stratégie FailFast. si une erreur interne grave est détectée, le processus de l’application serveur se termine et écrit un message d’erreur dans le journal des événements Windows. Cela permet de détecter rapidement les problèmes et est possible en raison de la protection des données d’application par le traitement des transactions. recherchez toujours dans le journal des événements Windows des erreurs de CRM, soit pendant le développement, soit pendant le déploiement final.

Les erreurs de base dans l’utilisation des interfaces CRM, telles que les arguments non valides ou les erreurs de séquence (par exemple, la tentative d’écriture d’un enregistrement de journal avant l’inscription du compensateur CRM), renvoient des codes d’erreur et ne doivent pas déclencher FailFast. pour le développement CRM, vous pouvez choisir de définir la clé de registre VTRACE1 (consultez [COM+ CRM registry Paramètres](com--crm-registry-settings.md)), ce qui entraîne l’affichage d’un message dans la fenêtre sortie du débogueur pour chaque erreur.

Des erreurs temporaires peuvent également se produire. Ces erreurs sont généralement dues à des conditions de synchronisation et entraînent le renvoi d’un code d’erreur. Le développeur CRM doit s’assurer que ces conditions d’erreur sont gérées. Par exemple, lors de l’écriture d’un enregistrement de journal, la transaction peut être abandonnée en raison d’un délai d’attente. La méthode retourne ensuite une erreur, que l’appelant doit vérifier et gérer de manière appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



