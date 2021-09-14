---
description: Décrit les concepts d’e/s de base.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Concepts d’e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009924"
---
# <a name="io-concepts"></a>Concepts d’e/s

Les concepts d’e/s suivants sont décrits dans cette section.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                               | Description                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mise en mémoire tampon des fichiers](file-buffering.md)<br/>                                     | Décrit les éléments à prendre en considération pour le contrôle d’application de la mise en mémoire tampon des fichiers, également appelée entrée/sortie (e/s) de fichiers non mis en mémoire tampon.<br/>                                    |
| [Mise en cache des fichiers](file-caching.md)<br/>                                         | Windows met en cache les données de fichiers qui sont lues à partir des disques et écrites sur les disques.<br/>                                                                                   |
| [E/s synchrones et asynchrones](synchronous-and-asynchronous-i-o.md)<br/> | Il existe deux types de synchronisation d’entrée/sortie (e/s) : e/s synchrone et e/s asynchrones. Les e/s asynchrones sont également appelées e/s avec chevauchement.<br/> |
| [Annulation d’opérations d’e/s en attente](canceling-pending-i-o-operations.md)<br/> | Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application.<br/>                             |
| [E/s alertables](alertable-i-o.md)<br/>                                       | Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.<br/>                     |
| [Ports de terminaison d’e/s](i-o-completion-ports.md)<br/>                         | Les ports de terminaison d’e/s fournissent un modèle de thread efficace pour traiter plusieurs demandes d’e/s asynchrones sur un système multiprocesseur.<br/>                  |



 

 

 




