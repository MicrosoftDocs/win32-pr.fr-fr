---
description: L’ordinateur des utilisateurs peut avoir accès à plusieurs appareils sélectionnables par l’utilisateur et utilisé pour effectuer des conversations vocales interactives.
ms.assetid: cc7ad70a-157e-4db4-b5e4-00d25686a9dd
title: Définition d’un terminal pour les conversations sur téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b12e772d8f941cb7c68e25136a843ec5f9a1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522000"
---
# <a name="setting-a-terminal-for-phone-conversations"></a>Définition d’un terminal pour les conversations sur téléphone

L’ordinateur de l’utilisateur peut avoir accès à plusieurs appareils sélectionnables par l’utilisateur et utilisé pour effectuer des conversations vocales interactives. Tout d’abord, il y a l’appareil téléphonique proprement dit, avec les lampes, les boutons, l’affichage, le sonnerie et l’appareil d’e/s vocal (combiné, haut-parleur, casque). L’ordinateur de l’utilisateur peut également disposer d’un périphérique d’e/s vocal distinct (par exemple, un casque ou une combinaison microphone/intervenant attaché à une carte son) pour une utilisation avec des conversations sur téléphone.

TSPI permet à l’utilisateur de sélectionner où router les informations que le commutateur envoie sur la ligne, l’adresse ou l’appel. Normalement, le commutateur s’attend à ce qu’il s’agit de l’un de ses jeux de téléphones et envoie des demandes de sonnerie, des événements de lampe (pour les téléphones à stimulus), des données d’affichage et des données vocales, le cas échéant. Le téléphone envoie à son tour des événements hookswitch, des événements d’enfoncement de bouton (pour les téléphones à stimulus) et des données vocales vers le commutateur.

La partie *ligne* de TSPI rend les événements de lampe, les événements d’affichage et les événements de sonnerie disponibles, soit en tant que codes de retour fonctionnels aux diverses opérations de ligne dans TSPI, soit en tant que messages d’état d’appel fonctionnel non sollicités envoyés au rappel d’application. L’implémentation du fournisseur de services est chargée du mappage entre le niveau TSPI fonctionnel et la stimulation ou les messages fonctionnels sous-jacents utilisés par le réseau de téléphonie. Dans les environnements de téléphonie fonctionnelle, les fonctions TSPI sont mappées au Protocole fonctionnel.

À l’aide de la fonction [**TSPI \_ LINESETTERMINAL**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) , TAPI peut contrôler le routage d’événements de bas niveau différents échangés entre le commutateur et la station ; il peut également décider de ne pas Router certains de ces événements de bas niveau vers un appareil. Le routage des différentes classes d’événements peut être contrôlé individuellement. Par exemple, le flux multimédia d’un appel (par exemple, la voix) peut être envoyé à n’importe quel périphérique de transducteur si le matériel et le fournisseur de services sont capables de le faire. Les événements de sonnerie du commutateur sur le téléphone peuvent être mappés dans une alerte visuelle sur l’écran de l’ordinateur ou ils peuvent être acheminés vers un appareil téléphonique. Les événements de lampe et les événements d’affichage peuvent être ignorés ou acheminés vers un appareil téléphonique (qui semble se comporter comme un ensemble de téléphones normal). Enfin, l’appui sur un bouton sur un appareil téléphonique peut ou non être passé sur la ligne. Dans tous les cas, ce routage de signaux de bas niveau à partir de la ligne n’affecte pas le fonctionnement de la partie de ligne de TSPI, qui mappe toujours les événements de bas niveau à leur équivalent fonctionnel. Les applications peuvent consulter les fonctionnalités d’appareil d’une ligne pour déterminer les terminaux disponibles.

En d’autres termes, la fonction [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) spécifie le périphérique terminal auquel la ligne, les événements d’adresse ou les événements de flux de média d’appel spécifiés sont routés. Des terminaux distincts peuvent être spécifiés pour chaque classe d’événements. Les classes d’événements incluent les lampes, les boutons, les affichages, les sonneries, les hookswitch et les flux de médias.

 

 
