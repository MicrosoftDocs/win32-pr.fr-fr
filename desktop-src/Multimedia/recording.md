---
title: Enregistrement
description: Enregistrement
ms.assetid: 0026eb1d-5be1-4090-801b-f1c65c179f42
keywords:
- Commande MCI_RECORD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4248b2d4bbdd984ad23a772f0adca04581afca1d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368183"
---
# <a name="recording"></a>Enregistrement

La spécification MCI générale prend en charge l’enregistrement avec la vidéo numérique, le séquenceur MIDI, l’enregistreur vidéo-cassette (VCR) et les périphériques audio Waveform. Toutefois, seuls les appareils Wave-audio et VCR implémentent actuellement des fonctionnalités d’enregistrement. Vous pouvez insérer ou remplacer des informations enregistrées dans un fichier ou un enregistrement existant dans un nouveau fichier. Pour enregistrer un fichier existant, ouvrez un fichier et un périphérique audio Waveform comme vous le feriez normalement. Pour enregistrer dans un nouveau fichier, lorsque vous ouvrez l’appareil, spécifiez « nouveau » comme nom de périphérique si vous utilisez l’interface de chaîne de commande. Si vous utilisez l’interface de message de commande, spécifiez un nom de fichier de longueur nulle.

Quand MCI crée un fichier pour l’enregistrement, le format de données est défini sur un format par défaut spécifié par le pilote de périphérique. Pour utiliser un format autre que le format par défaut, vous pouvez utiliser la commande [**Set**](set.md) ([**\_ jeu de MCI**](mci-set.md)).

Pour commencer l’enregistrement, utilisez la commande d' [**enregistrement**](record.md) (ou l' [**\_ enregistrement MCI**](mci-record.md) et la structure des [**\_ \_ PARMS d’enregistrement MCI**](mci-record-parms.md) ).

Si vous enregistrez en mode insertion dans un fichier existant, vous pouvez utiliser les indicateurs « de » (MCI \_ de) et « à » (MCI \_ à) de la commande **Enregistrer** pour spécifier les positions de début et de fin de l’enregistrement. Par exemple, si vous enregistrez dans un fichier dont la longueur est de 20 secondes et que vous commencez l’enregistrement à 5 secondes et que vous terminez l’enregistrement à 10 secondes, le fichier résultant sera de 25 secondes. Le fichier aura un segment de 5 secondes inséré 5 secondes dans l’enregistrement d’origine.

Si vous enregistrez le mode de remplacement dans un fichier existant, vous pouvez utiliser les indicateurs « from » et « to » pour spécifier les emplacements de début et de fin de la section qui est remplacée. Par exemple, si vous enregistrez dans un fichier dont la longueur est de 20 secondes et que vous commencez l’enregistrement à 5 secondes et que vous terminez l’enregistrement à 10 secondes, vous obtenez toujours un enregistrement de 20 secondes, mais la section qui commence à 5 secondes et se termine à 10 secondes a été remplacée.

Si vous ne spécifiez pas d’emplacement de fin, l’enregistrement continue jusqu’à ce que vous ayez envoyé une commande [**Stop**](stop.md) ([**\_ Stop MCI**](mci-stop.md)) ou jusqu’à ce que le pilote manque d’espace disque libre. Si vous enregistrez dans un nouveau fichier, vous pouvez omettre l’indicateur « from » ou lui affecter la valeur zéro pour démarrer l’enregistrement au début d’un nouveau fichier. Vous pouvez spécifier un emplacement de fin pour terminer l’enregistrement lors de l’enregistrement dans un nouveau fichier.

La commande d' [**enregistrement**](record.md) est parfois précise dans uniquement 1 seconde de l’emplacement de départ, comme avec les périphériques VCR. Pour enregistrer plus précisément, vous devez utiliser la commande de [**signalement**](cue.md) ([**MCI \_**](mci-cue.md)). Cette commande est reconnue par les périphériques vidéo numérique, magnétoscope et Waveform-Audio. Pour plus d’informations sur l’enregistrement avec les périphériques VCR, consultez [magnétoscope services](vcr-services.md).

## <a name="saving-a-recorded-file"></a>Enregistrement d’un fichier enregistré

Une fois l’enregistrement terminé, utilisez la commande [**Save**](save.md) (ou l' [**\_ enregistrement MCI**](mci-save.md) et la structure [**MCI \_ Save \_ PARMS**](mci-save-parms.md) ) pour enregistrer l’enregistrement avant de fermer l’appareil.

> [!Note]  
> Si vous fermez l’appareil sans enregistrer, les données enregistrées sont perdues.

 

## <a name="checking-input-levels-pcm-only"></a>Vérification des niveaux d’entrée (PCM uniquement)

Pour obtenir le niveau du signal d’entrée avant l’enregistrement sur un appareil d’entrée Waveform PCM (Pulse Code Modulation) Wave-audio, utilisez la commande [**Status**](status.md) ([**\_ État MCI**](mci-status.md)). Spécifiez l’indicateur « Level » (ou l' \_ \_ indicateur d’élément d’État MCI et définissez le membre **dwItem** de la structure de l' [**\_ état \_ MCI**](mci-status-parms.md) sur le \_ niveau d’État Wave MCI \_ \_ ). Le niveau de signal d’entrée moyen est retourné. La valeur du canal de gauche se trouve dans le mot de poids fort et la valeur de droite ou de mono-canal est dans le mot de poids faible.

Le niveau d’entrée est représenté sous la forme d’une valeur non signée. Pour les exemples de 8 bits, cette valeur est comprise entre 0 et 127 (0x7F). Pour les exemples de 16 bits, elle est comprise entre 0 et 32 767 (0x7FFF).

 

 




