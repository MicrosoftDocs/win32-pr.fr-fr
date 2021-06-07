---
title: Pour utiliser un flux de script
description: Pour utiliser un flux de script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- flux de script, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444730"
---
# <a name="to-use-a-script-stream"></a>Pour utiliser un flux de script

Cette section décrit comment envoyer des données de script à l’enregistreur pour les inclure dans un fichier. Pour plus d’informations sur l’inclusion de flux de script dans des profils, consultez [configuration de types de flux arbitraires](configuring-arbitrary-stream-types.md).

Chaque script se compose de deux chaînes, d’une chaîne de *type* et d’une chaîne d' *argument* .

Les données du script doivent être mises en forme avant d’être envoyées au writer. Les chaînes doivent être concaténées, séparées par un caractère **null** et se terminant par un caractère **null** . L’exemple suivant montre un script légitime :



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

Chaque paire de commandes de script doit être écrite en tant qu’exemple dans le writer. Pour plus d’informations sur l’écriture d’exemples, consultez [pour écrire des exemples](to-write-samples.md).

Lorsque le fichier ASF est lu, les commandes de script sont remises par le lecteur (ou lecteur synchrone) dans l’ordre de la durée de la présentation. Il est de la responsabilité de l’application d’analyser les deux chaînes et de répondre à la commande de script.

> [!Note]  
> Lorsque vous utilisez DRM pour chiffrer un fichier, aucune commande de script ne peut avoir une heure de présentation de 0.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des commandes de script**](using-script-commands.md)
</dt> </dl>

 

 




