---
title: Modification de la synchronisation de Sequencer
description: Modification de la synchronisation de Sequencer
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f7f31544b7b9ceb00109551718b9984dd2aa506557848e0d63e77724c4be32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526419"
---
# <a name="changing-sequencer-synchronization"></a>Modification de la synchronisation de Sequencer

> [!NOTE]
> Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.  Dans ce document, il existe des références au mot « esclave ». Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.  Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans le logiciel. Pour des fins de cohérence, ce document contient ce mot. Lorsque ce mot est supprimé du logiciel, nous allons corriger ce document pour qu’il soit aligné.

Pour modifier le mode de synchronisation d’un périphérique Sequencer, utilisez le message de commande [**\_ Set MCI**](mci-set.md) avec les \_ indicateurs MCI Seq \_ Set \_ Master et MCI \_ Seq \_ Set \_ esclave. Deux membres de la structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) , **dwMaster** et **dwSlave**, sont utilisés pour spécifier les modes de synchronisation maître et subordonné.

Le mode de synchronisation maître contrôle les informations de synchronisation envoyées par Sequencer à un port de sortie. Voici les constantes pour le membre **dwMaster** et les modes de synchronisation principaux correspondants.



| Constante        | Mode de synchronisation                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ Seq \_ midi  | Synchronisation MIDI. Envoyer les informations de minutage au port de sortie à l’aide des messages d’horloge de minutage MIDI.   |
| MCI \_ Seq \_ SMPTE | Synchronisation SMPTE. Envoyer les informations de minutage au port de sortie à l’aide de messages MIDI quart-Frame. |
| MCI \_ Seq \_ aucun  | Aucune synchronisation. Ne pas envoyer d’informations de minutage.                                                  |



 

Le mode de synchronisation subordonné détermine où Sequencer obtient ses informations de minutage pour lire un fichier MIDI. Voici les constantes pour le membre **dwSlave** et les modes de synchronisation subordonnés correspondants.



| Constante        | Mode de synchronisation                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fichier séquence \_ MCI  | Synchronisation de fichiers. Obtient les informations de minutage à partir du fichier MIDI.                                                                                       |
| MCI \_ Seq \_ midi  | Synchronisation MIDI. Obtient les informations de minutage à partir du port d’entrée à l’aide des messages d’horloge de minutage MIDI.                                                     |
| MCI \_ Seq \_ SMPTE | Synchronisation SMPTE. Obtient les informations de minutage à partir du port d’entrée à l’aide de messages MIDI quart-Frame.                                                   |
| MCI \_ Seq \_ aucun  | Aucune synchronisation. Récupérez les informations de minutage des commandes MCI uniquement et ignorez les informations de minutage (telles que les changements de tempo) qui se trouvent dans le fichier MIDI. |



 

> [!Note]  
> Actuellement, pour la synchronisation principale, MCI MIDI Sequencer ne prend en charge que le mode sans synchronisation (MCI \_ Seq \_ None). Pour la synchronisation subordonnée, elle prend en charge uniquement le mode de synchronisation de fichiers ( \_ fichier MCI Seq \_ ) et le mode sans synchronisation (MCI \_ Seq \_ None).

 

 

 




