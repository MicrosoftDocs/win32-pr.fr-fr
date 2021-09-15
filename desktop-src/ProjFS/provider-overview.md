---
title: Vue d’ensemble du fournisseur
description: Vue d’ensemble conceptuelle d’une application de fournisseur.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531037"
---
# <a name="provider-overview"></a>Vue d’ensemble du fournisseur

Le fournisseur est une application en mode utilisateur qui gère et comprend un magasin de données de sauvegarde.  Le fournisseur implémente les rappels ProjFS et utilise l’API ProjFS pour projeter ce magasin de données dans le système de fichiers où il apparaît à l’utilisateur sous la forme de fichiers et de répertoires.  Le magasin de stockage du fournisseur peut être local sur le système de l’utilisateur ou il peut être placé à distance.

## <a name="data-projection"></a>Projection de données

La partie du système de fichiers que le fournisseur possède, où ses données sont projetées, est enracinée dans un répertoire appelé « racine de virtualisation ».  Lorsque le fournisseur souhaite commencer à projeter ses données, il démarre une « instance de virtualisation », qui est un objet qui gère la communication entre le fournisseur et ProjFS pour l’ensemble de fichiers et de répertoires situés sous une racine de virtualisation particulière.  Tous les fichiers et répertoires qui sont des descendants de la racine de virtualisation qui n’ont pas été créés localement par l’utilisateur sont matérialisés par le fournisseur via l’API ProjFS.  Ces éléments démarrent sous la forme de fichiers et de répertoires virtuels, ce qui signifie qu’ils n’existent pas sur le périphérique de stockage local de l’utilisateur, mais sont injectés dans les résultats de l’énumération par ProjFS.  À mesure que les éléments sont ouverts et lus, ProjFS appelle les rappels implémentés par le fournisseur pour demander des données, et le fournisseur utilise les API ProjFS pour envoyer ces données au stockage local où elles sont mises en cache pour un accès ultérieur.  Si la vue de l’utilisateur du magasin de données de stockage doit être modifiée, par exemple si le contenu du magasin de données a changé, le fournisseur peut utiliser des API ProjFS pour mettre à jour ou supprimer des éléments locaux afin de refléter la nouvelle vue du magasin de données.

## <a name="callback-return-codes"></a>Codes de retour de rappel

Chaque rappel répertorie plusieurs valeurs de retour possibles spécifiques à ce rappel.  En plus des valeurs de retour listées pour un rappel donné, un rappel peut également retourner certains autres codes d’erreur.  Il s’agit de la liste complète des codes d’erreur pouvant être renvoyés par un rappel :

| Code d'erreur                                    | Signification
|-----------------------------------------------|--------
| S_OK                                          | Opération réussie
| E_OUTOFMEMORY                                 | Impossible d’allouer la mémoire nécessaire.
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)          | Le fournisseur souhaite terminer l’opération ultérieurement.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Une mémoire tampon passée à un rappel est trop petite.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | Le fichier n’existe pas dans le magasin de stockage du fournisseur.
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)   | Un argument de rappel n’est pas valide.  Par exemple, un ID d’énumération ne correspond pas à une session d’énumération active.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | Le fournisseur souhaite empêcher une opération, telle qu’un changement de nom ou une suppression, de se produire.

Les rappels peuvent également retourner toutes les erreurs qu’ils peuvent recevoir des appels aux API ProjFS.
Si un rappel retourne un code d’erreur qui ne figure pas dans la liste précédente ou qui ne provient pas d’une API ProjFS, ProjFS le renverra au système de fichiers en tant que STATUS_INTERNAL_ERROR.
