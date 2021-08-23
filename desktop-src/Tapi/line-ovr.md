---
description: Le concept de ligne a évolué au fil du temps et a été partiellement remplacé par les concepts d’adresse et de terminal. TAPI 3 n’utilise pas directement le concept de ligne, mais TAPI 2 continue à incorporer ce paradigme.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c299924a69d3e6e4889d14a72a571ca11ed2dc9e97514702f8ba4836f4c5b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660202"
---
# <a name="line"></a>Ligne

Le concept de ligne a évolué au fil du temps et a été partiellement remplacé par les concepts d’adresse et de terminal. TAPI 3 n’utilise pas directement le concept de ligne, mais TAPI 2 continue à incorporer ce paradigme.

Un *périphérique de ligne* est un appareil physique, tel qu’un tableau de télécopie, un modem ou une carte RNIS connectée à un réseau. L’appareil peut ne pas être connecté physiquement à l’ordinateur sur lequel l’application TAPI est exécutée, par exemple un pool de modems sur un serveur. Les appareils en ligne prennent en charge les fonctionnalités de communication en permettant aux applications d’envoyer des informations ou de recevoir des informations d’un réseau. Un périphérique de ligne contient un ensemble d’un ou de plusieurs canaux homogènes qui peuvent être utilisés pour établir des appels.

Dans les applications TAPI 2. x, un appareil de ligne est la représentation logique d’un appareil téléphonique physique. Bien que « Line » contourne souvent un élément avec deux points de terminaison, il est possible d’abstraire un appareil de ligne à un point unique, car l’interface TAPI l’affiche uniquement comme point d’entrée de la ligne menant au commutateur.

![périphériques de ligne](images/ch0501.png)

Bien que les trois lignes de l’illustration précédente soient composées de matériel différent et utilisées pour différentes fonctions, elles sont extraites du même type de périphérique et régies par les mêmes règles. Le téléphone ne représente pas un appareil téléphonique, mais un appareil de ligne utilisé pour les appels vocaux. Lors de l’utilisation de ce périphérique de ligne pour les appels entrants ou sortants, l’application doit également ouvrir et contrôler une instance de la classe de périphérique téléphonique, qui est décrite en détail dans les sections suivantes.

La classe de périphérique en ligne est une représentation indépendante du périphérique d’un périphérique de ligne physique, tel qu’un modem. Il peut contenir un ou plusieurs canaux de communication identiques (utilisés pour la signalisation et/ou les informations) entre l’application et le commutateur ou le réseau. Étant donné que les canaux appartenant à une seule ligne ont des fonctionnalités identiques, ils sont interchangeables. Dans de nombreux cas (comme avec les POTS), un fournisseur de services modélise une ligne comme n’ayant qu’un seul canal. D’autres technologies, comme RNIS, offrent davantage de canaux et le fournisseur de services doit les traiter en conséquence.

**TAPI 2. x :** Les applications découvrent les fonctionnalités de ligne à l’aide de la fonction [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) . La négociation de version à l’aide des fonctions [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) doit avoir été appelée précédemment.

**TAPI 3. x :** Les applications reposent principalement sur le concept d’adresse.

 

 
