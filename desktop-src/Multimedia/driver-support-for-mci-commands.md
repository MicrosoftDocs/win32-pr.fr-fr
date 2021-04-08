---
title: Prise en charge des pilotes pour les commandes MCI
description: Prise en charge des pilotes pour les commandes MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672590"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="0f8ab-103">Prise en charge des pilotes pour les commandes MCI</span><span class="sxs-lookup"><span data-stu-id="0f8ab-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="0f8ab-104">Les pilotes MCI fournissent les fonctionnalités pour les commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="0f8ab-105">Le logiciel système effectue des tâches de gestion de données de base, mais l’ensemble de la lecture, de la présentation et de l’enregistrement multimédia est géré par les pilotes MCI individuels.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="0f8ab-106">Les pilotes varient en fonction de la prise en charge des commandes MCI et des indicateurs de commande.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="0f8ab-107">Étant donné que les périphériques multimédias peuvent avoir des fonctionnalités très différentes, MCI est conçu pour permettre aux pilotes individuels d’étendre ou de réduire les jeux de commandes pour qu’ils correspondent aux fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="0f8ab-108">Par exemple, la commande d' [**enregistrement**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) fait partie du jeu de commandes pour les séquenceurs midi, mais le pilote MCISEQ inclus avec Windows ne prend pas en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="0f8ab-109">La rubrique de référence pour la commande record explique que les appareils du type d’appareil **Sequencer** reconnaissent la commande ; Cela ne signifie pas que tous les appareils de ce type prennent en charge la commande.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="0f8ab-110">Les applications doivent utiliser la commande [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) pour déterminer les capacités d’un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="0f8ab-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




