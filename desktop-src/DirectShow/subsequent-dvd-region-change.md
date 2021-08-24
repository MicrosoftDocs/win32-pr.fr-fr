---
description: Modification de la région du DVD suivante
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Modification de la région du DVD suivante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6da91ff9fefb17480bbc502deb2fea80683e5861d32cfa4d4fa1a5cb22c2847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633289"
---
# <a name="subsequent-dvd-region-change"></a>Modification de la région du DVD suivante

dans Windows 2000 et versions ultérieures, le navigateur dvd appelle une page de propriétés sur le lecteur de dvd-ROM dans le Gestionnaire de périphériques. Cette page de propriétés est également mise en place par l’application DVDPlay.exe lorsqu’une région doit être modifiée. L’interface utilisateur de cette page de propriétés est très similaire à celle de DVDRgn.exe et elle est régionale dans le système d’exploitation.

pour les lecteurs RPC1, les composants du système d’exploitation Windows gèrent les modifications de région. Les lecteurs RPC2 maintiennent le paramètre de région dans leur propre matériel. Lorsque le nombre de modifications autorisées est épuisé sur un lecteur RPC2, le lecteur échouera en cas d’échec de l’appel pour modifier la région et le composant Region-change dans le système d’exploitation indiquera qu’à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du changement de région des DVD dans Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



