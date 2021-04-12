---
title: Outils du journal des événements Windows
description: Le journal des événements Windows fournit les outils suivants que vous utilisez pour créer votre fournisseur.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104381734"
---
# <a name="windows-event-log-tools"></a>Outils du journal des événements Windows

Le journal des événements Windows fournit les outils suivants que vous utilisez pour créer votre fournisseur.



| Outil                                                           | Description                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md)  | Utilitaire en ligne de commande utilisé pour compiler des manifestes d’instrumentation et des fichiers texte de message. |
| WevtUtil.exe                                                   | Utilitaire de ligne de commande principalement utilisé pour inscrire votre fournisseur sur l’ordinateur. Vous pouvez également l’utiliser pour obtenir des informations de métadonnées sur le fournisseur, ses événements et les canaux dans lesquels il journalise des événements, ainsi que pour interroger des événements à partir d’un canal ou d’un fichier journal. L’outil WevtUtil.exe est inclus dans% windir% \\ system32. Pour obtenir des informations sur l’utilisation, entrez « wevtutil/ ? » à une invite de commandes.<br/> Cette commande est limitée aux membres du groupe administrateurs et doit être exécutée avec des privilèges élevés.|
