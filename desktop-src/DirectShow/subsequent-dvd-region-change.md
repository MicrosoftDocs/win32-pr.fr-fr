---
description: Modification de la région du DVD suivante
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Modification de la région du DVD suivante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534104"
---
# <a name="subsequent-dvd-region-change"></a>Modification de la région du DVD suivante

Dans Windows 2000 et versions ultérieures, le navigateur DVD appelle une page de propriétés sur le lecteur de DVD-ROM dans le Gestionnaire de périphériques. Cette page de propriétés est également mise en place par l’application DVDPlay.exe lorsqu’une région doit être modifiée. L’interface utilisateur de cette page de propriétés est très similaire à celle de DVDRgn.exe et elle est régionale dans le système d’exploitation.

Pour les lecteurs RPC1, les composants du système d’exploitation Windows gèrent les modifications de région. Les lecteurs RPC2 maintiennent le paramètre de région dans leur propre matériel. Lorsque le nombre de modifications autorisées est épuisé sur un lecteur RPC2, le lecteur échouera en cas d’échec de l’appel pour modifier la région et le composant Region-change dans le système d’exploitation indiquera qu’à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des modifications de région de DVD dans Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



