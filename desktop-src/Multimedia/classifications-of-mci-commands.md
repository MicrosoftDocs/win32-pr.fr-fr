---
title: Classifications des commandes MCI
description: Classifications des commandes MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- Commandes MCI, classifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009563"
---
# <a name="classifications-of-mci-commands"></a>Classifications des commandes MCI

MCI définit quatre classifications de commande : System, required, Basic et Extended. La liste suivante décrit ces classifications de commande :

-   Les *commandes système* sont gérées directement par MCI, plutôt que par le pilote.
-   Les *commandes requises* sont gérées par le pilote. Tous les pilotes MCI doivent prendre en charge les commandes et indicateurs requis.
-   Les *commandes de base* (ou les commandes facultatives) sont utilisées par certains appareils. Si un appareil prend en charge une commande de base, il doit prendre en charge un ensemble défini d’indicateurs pour cette commande.
-   Les *commandes étendues* sont spécifiques à un type d’appareil ou à un pilote. Les commandes étendues incluent des commandes, telles que les commandes [**put**](put.md) ([**MCI \_ put**](mci-put.md)) et [**Where**](where.md) ([**MCI \_**](mci-where.md)) des types d’appareils **Digitalvideo** et **Overlay** , ainsi que les extensions des commandes existantes (telles que l’indicateur « Stretch » de la commande [**Status**](status.md) ([**\_ État MCI**](mci-status.md)) pour le type d’appareil de superposition).

Alors que le système et les commandes requises sont le jeu de commandes minimal pour tout pilote MCI, les commandes de base et étendues ne sont pas prises en charge par tous les pilotes. Votre application peut toujours utiliser les commandes système et requises et leurs indicateurs, mais s’il doit utiliser une commande ou un indicateur de base ou étendu, elle doit d’abord interroger le pilote à l’aide de la commande [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)). Les sections suivantes résument les commandes spécifiques dans chaque catégorie.

## <a name="system-commands"></a>Commandes système

MCI traite les commandes système suivantes directement, plutôt que de les transmettre aux périphériques MCI.



| String                 | Message                             | Description                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**saut**](break.md) | [**\_Pause MCI**](mci-break.md)     | Définit une clé d’arrêt pour un appareil MCI.    |
| [sysinfo](sysinfo.md) | [**MCI \_ sysinfo**](mci-sysinfo.md) | Retourne des informations sur les périphériques MCI. |



 

## <a name="required-commands"></a>Commandes requises

Tous les périphériques MCI prennent en charge les commandes requises suivantes.



| String                           | Message                                   | Description                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Faculté**](capability.md) | [**\_GETDEVCAPS MCI**](mci-getdevcaps.md) | Obtient les fonctionnalités d’un appareil.                                                                                     |
| [**plus**](close.md)           | [**\_fermeture MCI**](mci-close.md)           | Ferme l’appareil.                                                                                                        |
| [**info**](info.md)             | [**\_infos MCI**](mci-info.md)             | Obtient des informations textuelles à partir d’un appareil.                                                                                |
| [**afficher**](open.md)             | [**MCI \_ ouvert**](mci-open.md)             | Initialise l’appareil.                                                                                                   |
| [**status**](status.md)         | [**\_État MCI**](mci-status.md)         | Obtient des informations d’État à partir de l’appareil. Certains indicateurs de cette commande ne sont pas requis. il s’agit également d’une commande de base. |



 

Les appareils doivent également prendre en charge un jeu standard d’indicateurs de commande pour les commandes requises.

## <a name="basic-commands"></a>Commandes de base

La liste suivante récapitule les commandes de base. L’utilisation de ces commandes par un périphérique MCI est facultative.



| String                   | Message                           | Description                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**chargera**](load.md)     | [**\_chargement MCI**](mci-load.md)     | Charge des données à partir d’un fichier.                                                                                                                                                                                                                 |
| [**suspen**](pause.md)   | [**\_Pause MCI**](mci-pause.md)   | Arrête la durée de la diffusion. La lecture ou l’enregistrement peut être repris à la position actuelle.                                                                                                                                                            |
| [**répétition**](play.md)     | [**\_lecture MCI**](mci-play.md)     | Commence la transmission des données de sortie.                                                                                                                                                                                                        |
| [**enregistrement**](record.md) | [**\_enregistrement MCI**](mci-record.md) | Démarre l’enregistrement des données d’entrée.                                                                                                                                                                                                            |
| [**sort**](resume.md) | [**\_reprise MCI**](mci-resume.md) | Reprend la diffusion ou l’enregistrement sur un appareil suspendu.                                                                                                                                                                                        |
| [**été**](save.md)     | [**\_enregistrement MCI**](mci-save.md)     | Enregistre les données dans un fichier sur disque.                                                                                                                                                                                                              |
| [**Demandez**](seek.md)     | [**\_recherche MCI**](mci-seek.md)     | Effectue une recherche vers l’avant ou vers l’arrière.                                                                                                                                                                                                              |
| [**set**](set.md)       | [**jeu de MCI \_**](mci-set.md)       | Définit l’état de fonctionnement de l’appareil.                                                                                                                                                                                                 |
| [**status**](status.md) | [**ÉTAT MCI**](mci-status.md)  | Obtient des informations d’État sur l’appareil. Il s’agit également d’une commande obligatoire. étant donné que certains de ses indicateurs ne sont pas nécessaires, ils sont également répertoriés ici. (Les éléments facultatifs prennent en charge les appareils qui utilisent un média linéaire avec des positions identifiables.) |
| [**erreur**](stop.md)     | [**\_arrêt MCI**](mci-stop.md)     | Arrête la durée de la diffusion.                                                                                                                                                                                                                          |



 

Si un pilote prend en charge une commande de base, il doit également prendre en charge un ensemble standard d’indicateurs pour la commande.

## <a name="extended-commands"></a>Commandes étendues

Certains périphériques MCI ont des commandes supplémentaires, ou ils ajoutent des indicateurs à des commandes existantes. Bien que certaines commandes étendues s’appliquent uniquement à un pilote de périphérique spécifique, la plupart d’entre elles s’appliquent à tous les pilotes d’un type d’appareil particulier. Par exemple, le jeu de commandes pour le type d’appareil **Sequencer** étend la commande [**Set**](set.md) ([**\_ jeu de MCI**](mci-set.md)) pour ajouter les formats d’heure requis par les séquenceurs midi.

Vous ne devez pas supposer que l’appareil prend en charge les commandes ou indicateurs étendus. Vous pouvez utiliser la commande [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) pour déterminer si une fonctionnalité spécifique est prise en charge, et votre application doit être prête à gérer les valeurs de retour « commande non prise en charge » ou « fonction non prise en charge ».

Les commandes étendues suivantes sont disponibles avec les types d’appareils répertoriés.



| String                         | Message                                 | Types d’appareils            | Description                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**configurer**](configure.md) | [**configuration de MCI \_**](mci-configure.md) | digitalvideo            | Affiche une boîte de dialogue de configuration.                                                              |
| [**signal**](cue.md)             | [**\_signal MCI**](mci-cue.md)             | Digitalvideo, WaveAudio | Prépare la diffusion ou l’enregistrement.                                                                |
| [**supprimer**](delete.md)       | [**suppression de MCI \_**](mci-delete.md)       | WaveAudio               | Supprime un segment de données du fichier multimédia.                                                       |
| [sortie](escape.md)           | [**\_échappement MCI**](mci-escape.md)       | videodisc               | Envoie des informations personnalisées à un appareil.                                                             |
| [**antigel**](freeze.md)       | [**\_blocage MCI**](mci-freeze.md)       | superposition                 | Désactive l’acquisition vidéo dans la mémoire tampon de trame.                                                   |
| [**posé**](put.md)             | [**PUT MCI**](mci-put.md)              | Digitalvideo, superposition   | Définit les fenêtres source, de destination et Frame.                                               |
| [**optimiser**](realize.md)     | [**MCI- \_ réalise**](mci-realize.md)     | digitalvideo            | Indique à l’appareil de sélectionner et de réaliser sa palette dans un contexte de périphérique de la fenêtre affichée. |
| [**setaudio**](setaudio.md)   | [**\_SETAUDIO MCI**](mci-setaudio.md)  | digitalvideo            | Définit les paramètres audio de la vidéo.                                                                  |
| [**setvideo**](setvideo.md)   | [**\_SETVIDEO MCI**](mci-setvideo.md)  | digitalvideo            | Définit les paramètres vidéo.                                                                            |
| [**témoin**](signal.md)       | [**\_signal MCI**](mci-signal.md)       | digitalvideo            | Identifie une position spécifiée avec un signal.                                                    |
| [**toupie**](spin.md)           | [**\_spin MCI**](mci-spin.md)           | videodisc               | Démarre le disque en rotation ou arrête la rotation du disque.                                         |
| [**première**](step.md)           | [**\_étape MCI**](mci-step.md)           | digitalvideo, videodisc | Exécute un ou plusieurs frames vers l’avant ou vers l’arrière.                                             |
| [**libérer**](unfreeze.md)   | [**MCI- \_ libérer**](mci-unfreeze.md)   | superposition                 | Permet à la mémoire tampon de trame d’acquérir des données vidéo.                                                   |
| [**mise à jour**](update.md)       | [**\_mise à jour MCI**](mci-update.md)       | digitalvideo            | Repeint le frame actuel dans le contexte de périphérique.                                               |
| [**Cela**](where.md)         | [**MCI OÙ**](mci-where.md)          | Digitalvideo, superposition   | Obtient le rectangle spécifiant la source, la destination ou la zone de frame.                          |
| [**fenetre**](window.md)       | [**\_fenêtre MCI**](mci-window.md)       | Digitalvideo, superposition   | Contrôle la fenêtre d’affichage.                                                                      |



 

 

 




