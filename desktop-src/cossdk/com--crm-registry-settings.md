---
description: Plusieurs paramètres du Registre sont disponibles pour modifier le comportement de CRM afin de faciliter le dépannage et le développement.
ms.assetid: c4e68451-fb8a-45b5-9968-7d5a6418dfe8
title: Paramètres du Registre CRM CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0ea4ec245ab55b73c79660973824fcf33c6c2b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860869"
---
# <a name="com-crm-registry-settings"></a>Paramètres du Registre CRM CRM

Plusieurs paramètres du Registre sont disponibles pour modifier le comportement de CRM afin de faciliter le dépannage et le développement. Tous ces paramètres de Registre, répertoriés et décrits dans le tableau suivant, sont facultatifs. aucun n’est requis pour le fonctionnement normal du CRM.

Tous les paramètres du Registre CRM se trouvent sous **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ COM3 \\ CRM**. Si ce n’est déjà fait, créez la clé **CRM** sous la clé **COM3** .



| Paramètres du Registre CRM                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VTRACE1**<br/>                 | Valeur de Registre \_ DWORD. La définition de cette valeur sur une valeur autre que zéro active les messages de trace de débogage sur les avertissements ou les erreurs. Ces messages peuvent être affichés dans la fenêtre sortie du débogueur. Cette valeur doit être définie pour le développement uniquement et pas pendant un déploiement normal. Cette valeur est lue au démarrage d’une application de serveur CRM.<br/>                                                                                                                                                                                                                                                   |
| **IgnoreCompensatorErrors**<br/> | Valeur de Registre \_ DWORD. La définition de cette valeur sur une valeur autre que zéro permet à l’infrastructure CRM d’ignorer toutes les erreurs retournées par les compensateurs CRM. Si la récupération échoue en raison d’une erreur d’un compensateur CRM, la définition de cette valeur permet d’effectuer la récupération. Cette valeur est lue au démarrage d’une application de serveur CRM.<br/>                                                                                                                                                                                                                                           |
| **CheckpointIntervalInSec**<br/> | Valeur de Registre \_ DWORD. Il s’agit de l’intervalle de point de contrôle en secondes. L’intervalle de point de contrôle par défaut est de 30 secondes. Les points de contrôle sont utilisés pour récupérer de l’espace à partir du fichier journal CRM. L’augmentation de l’intervalle de point de contrôle peut améliorer les performances, mais au détriment de l’augmentation du temps de récupération et d’un plus grand fichier journal CRM. Cette valeur est lue au démarrage d’une application de serveur CRM.<br/>                                                                                                                                                                                                  |
| **InitialLogFileSizeInKB**<br/>  | Valeur de Registre \_ DWORD. Il s’agit de la taille initiale du fichier journal de CRM, en kilo-octets. La taille du fichier journal CRM par défaut est de 1024 Ko (1 Mo). Le fichier journal CRM se développe automatiquement pour répondre à la charge de transaction imposée, mais si des charges lourdes sont attendues, il peut être nécessaire d’augmenter cette valeur. Cette valeur est lue lors du démarrage d’une application serveur COM+ activée pour CRM, mais si le fichier journal CRM existe déjà pour une application CRM Server, cette valeur est ignorée pour cette application serveur.<br/>                                                                               |
| **RecoveryTraceEnabled**<br/>    | Valeur de Registre \_ DWORD. La définition de cette valeur sur une valeur autre que zéro active une trace de récupération. Le suivi de récupération est un fichier texte qui porte le même nom que le fichier journal CRM et l’extension supplémentaire suivante : .recoverytrace.txt. <br/> Ce fichier se trouve dans le même répertoire que le fichier journal CRM. Le suivi de récupération fournit une trace de l’activité CRM pendant la récupération, qui peut être utilisée pour le diagnostic des problèmes. Cette valeur est lue au démarrage d’une application de serveur CRM. Toutefois, un fichier de trace de récupération unique est généré pour chaque application CRM Server.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 




