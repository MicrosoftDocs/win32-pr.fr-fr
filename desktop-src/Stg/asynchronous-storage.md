---
title: Stockage asynchrone
description: Le stockage asynchrone améliore la spécification de stockage structuré COM pour prendre en charge le téléchargement asynchrone d’objets de stockage sur des réseaux à latence élevée et à liaison lente tels qu’Internet.
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- Stockage structuré Strctd STG, stockage asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463483"
---
# <a name="asynchronous-storage"></a>Stockage asynchrone

Le stockage asynchrone améliore la spécification de stockage structuré COM pour prendre en charge le téléchargement asynchrone d’objets de stockage sur des réseaux à latence élevée et à liaison lente tels qu’Internet. Le stockage asynchrone permet à la fois aux applications nouvelles et héritées qui utilisent des fichiers composés de restituer efficacement leur contenu lorsqu’ils sont accessibles au moyen de protocoles Internet existants. Une demande unique à un serveur de World Wide Web déclenche le téléchargement d’objets imbriqués contenus dans une page Web, ce qui évite d’avoir à demander séparément chaque objet. Un mécanisme asynchrone de téléchargement et d’accès permet à une application de restituer la première page de données avant que toutes les données n’aient été reçues. L’ordre exact dans lequel les éléments d’une page deviennent disponibles peut être spécifié par le serveur de publication Web et ne dépend pas des facteurs aléatoires de la topologie du réseau et de la disponibilité du serveur.

Le stockage asynchrone fonctionne avec les monikers asynchrones pour fournir un comportement de liaison asynchrone complet. Pour plus d’informations sur les monikers asynchrones, consultez le kit de développement logiciel (SDK) Microsoft ActiveX. Un moniker asynchrone propre au protocole déclenche l’opération de liaison et configure les composants requis. Dans le cas d’Internet, ce moniker est un moniker qui peut analyser une URL pour établir une liaison à un objet ou à un stockage. Si la cible de l’opération de liaison est un objet persistant, l’appel à [**IMoniker :: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) retourne un objet de stockage asynchrone.

> [!Note]  
> La version actuelle des monikers d’URL Microsoft ne prend pas en charge le stockage asynchrone.

 

Un client moniker asynchrone demande une liaison asynchrone en implémentant un objet de rappel d’état de liaison et en l’inscrivant auprès du contexte de liaison. L’objet de rappel d’état de liaison expose l’interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , qui permet au client de spécifier des préférences de liaison et de recevoir des notifications de disponibilité globale et de progression au cours d’une opération de liaison. L’implémentation asynchrone de fichiers composés fournit un point de connexion pour [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), que les clients peuvent utiliser pour recevoir des notifications de disponibilité spécifiques sur des flux individuels.

 

 