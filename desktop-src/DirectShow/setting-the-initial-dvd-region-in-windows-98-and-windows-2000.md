---
description: Définition de la région du DVD initial
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Définition de la région du DVD initial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102319"
---
# <a name="setting-the-initial-dvd-region"></a>Définition de la région du DVD initial

Il incombe au fabricant du système de sélectionner une région de DVD initiale pour le lecteur de DVD dans leurs PC.

> [!Note]  
> Seuls les disques chiffrés peuvent être utilisés pour définir la région.

 

### <a name="windows-2000-and-later"></a>Windows 2000 et versions ultérieures

à partir de Windows 2000, la région DVD par défaut est sélectionnée en fonction des paramètres régionaux pour lesquels la machine est configurée. Windows 2000 définira toujours la région initiale pour un lecteur de DVD à l’aide de cette région par défaut, ainsi que de la région du disque, si un disque se trouve dans le lecteur. le fabricant du système n’a rien à faire pour définir la région initiale pour les lecteurs de DVD Windows 2000 ou version ultérieure.

Pour les lecteurs RPC1, s’il n’y a pas de disque dans le lecteur lors du démarrage, la région par défaut est définie uniquement en fonction des paramètres régionaux de l’ordinateur. S’il y a un disque DVD dans le lecteur lors du démarrage, la région par défaut est sélectionnée pour être la région du lecteur, à condition qu’elle corresponde à une région du disque. dans le cas contraire, la région la plus basse sur le disque est choisie comme région initiale du lecteur. L’utilisateur (ou le fabricant du système) a une modification restante autorisée, si la valeur par défaut n’était pas correcte.

pour les lecteurs RPC2, si au cours du processus d’installation Windows 2000 constate que le lecteur n’a pas de région définie, il tente de sélectionner une région comme indiqué ci-dessus, mais uniquement s’il y a un disque dans le lecteur. (Les lecteurs RPC1 choisissent la région sans disque dans le lecteur). Une fois qu’une région est définie pour les lecteurs RPC2, elle n’est pas modifiée automatiquement par une réinstallation ou une nouvelle installation du système d’exploitation.

L’OEM peut définir une clé de registre contenant la région du DVD par défaut pour le système. Au premier démarrage, la région du lecteur sera définie sur cette valeur. la clé de registre sur Windows 2000 et versions ultérieures est HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (binary).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du changement de région des DVD dans Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



