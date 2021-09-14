---
description: Un appareil téléphonique est un appareil qui prend en charge la classe d’appareil téléphonique et qui comprend des hookswitches, des téléphones, des mains et des casques.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Téléphone Éléments d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011096"
---
# <a name="phone-device-elements"></a>Téléphone Éléments d’appareil

Un appareil téléphonique est un appareil qui prend en charge la classe Phone Device et qui comprend certains ou l’ensemble des éléments suivants :

-   **Hookswitch/transducteur**: il s’agit d’un moyen d’entrée et de sortie audio. Un appareil téléphonique peut avoir plusieurs transducteurs, qui peuvent être activés et désactivés (pris offhook ou placé OnHook) sous application ou contrôle utilisateur manuel.

    La téléphonie identifie trois types d’appareils hookswitch communs à de nombreux jeux de téléphones :

     **Téléphone**: la combinaison d’éléments de bouche et d’oreille traditionnelle qui doit être retirée manuellement d’une station d’accueil et maintenue contre l’oreille de l’utilisateur.  
    **Haut**-parleur : permet à l’utilisateur de procéder à des appels mains libres. Le haut-parleur peut être interne ou externe à l’appareil téléphonique. La partie haut-parleur d’un haut-parleur permet plusieurs écouteurs.  
    **Casque**: permet à l’utilisateur de procéder à des appels mains libres.  
    

    Un hookswitch doit être offhook pour permettre aux données audio d’être envoyées et/ou reçues par le capteur correspondant.

-   Contrôle de volume/gain de contrôle/muet : chaque appareil hookswitch est l’appariement d’un haut-parleur et d’un composant de microphone. L’API fournit un contrôle du volume et une désactivation des composants du haut-parleur et permet d’obtenir un contrôle ou une désactivation des composants du microphone.
-   [Sonnerie](ring.md): un moyen d’alerter les utilisateurs, généralement par le biais d’une cloche. Un appareil téléphonique peut être en mesure de sonner dans différents modes ou modèles.
-   [Display](display.md): mécanisme permettant de présenter visuellement des messages à l’utilisateur. Un affichage sur téléphone est caractérisé par le nombre de lignes et de colonnes.
-   [boutons de Téléphone](phone-buttons.md): tableau de boutons. Chaque fois que l’utilisateur appuie sur un bouton de l’ensemble de téléphones, l’API signale que le bouton correspondant a été enfoncé. Les identificateurs de lampe de bouton identifient une paire bouton/lampe. Bien entendu, il est possible d’avoir des paires bouton-lampe avec aucun bouton ou aucun feu. Les identificateurs de lampe de bouton sont des valeurs entières comprises entre 0 et le nombre maximal de lampes de bouton disponibles sur l’appareil téléphonique, moins un. Chaque bouton appartient à une classe Button. Les classes incluent les boutons d’apparence des appels, les boutons de fonctionnalité, les boutons du pavé numérique et les boutons locaux.
-   [Lampes](lamps.md): un tableau de lampes (tels que del) contrôlable individuellement à partir de l’API. Les lampes peuvent être allumées dans différents modes en modifiant la fréquence d’activation et de désactivation. L’identificateur de feu-bouton identifie la lampe.
-   [Zones de données](data-areas.md): zones mémoire du périphérique téléphonique où le code d’instruction ou les données peuvent être téléchargés vers et/ou téléchargés à partir de. Les informations téléchargées affectent le comportement (ou, en d’autres termes, le programme) du périphérique téléphonique.

L’interface TAPI permet à une application de surveiller et de contrôler les éléments de l’appareil téléphonique. Les éléments les plus utiles pour une application sont les appareils hookswitch. L’ensemble de téléphones peut agir comme un périphérique d’e/s Audio (sur l’ordinateur) avec le contrôle du volume, prendre le contrôle et le silence, un anneau (pour alerter l’utilisateur), des zones de données (pour la programmation du téléphone) et peut-être un affichage, même si l’affichage de l’ordinateur est plus efficace. Le writer d’application est déconseillé de contrôler directement ou d’utiliser des lampes ou des boutons de téléphone, car les fonctionnalités de lampe et de bouton peuvent varier considérablement d’un ensemble de téléphones à l’autre, et les applications peuvent rapidement devenir adaptées à des ensembles de téléphones spécifiques.

Il n’existe aucun ensemble de services de base garanti pris en charge par tous les appareils téléphoniques comme c’est le cas pour les appareils en ligne (les services de téléphonie de base). Par conséquent, avant qu’une application puisse utiliser un appareil téléphonique, l’application doit d’abord déterminer les fonctionnalités exactes du périphérique téléphonique. La fonctionnalité de téléphonie varie en fonction de la configuration (client et client/serveur), du matériel téléphonique et du logiciel du fournisseur de services. Les applications ne doivent pas faire d’hypothèses quant aux fonctionnalités de téléphonie disponibles. Une application détermine les fonctionnalités d’appareil d’un appareil téléphonique en appelant la fonction [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) . Les fonctionnalités de l’appareil d’un téléphone indiquent lequel de ces éléments existent pour chaque appareil téléphonique présent dans le système et leurs fonctionnalités. Bien qu’ils soient fortement orientés vers les jeux de téléphone réels, cette abstraction peut également fournir une implémentation significative (ou sous-ensemble de ces derniers) pour d’autres périphériques. Prenons comme exemple un casque distinct directement connecté et contrôlable à partir de l’ordinateur et fonctionnant comme un appareil téléphonique. Les modifications hookswitch peuvent être déclenchées par la détection de l’énergie vocale (offhook) ou par une période de silence (OnHook); la sonnerie peut être émulée par la génération d’un signal sonore dans le casque ; un affichage peut être émulé par le biais de la conversion de texte par synthèse vocale.

Un appareil téléphonique n’a pas besoin d’être réalisé sur le matériel, mais il peut être émulé dans un logiciel à l’aide d’une interface de commande graphique pilotée par la souris ou du clavier, ainsi que du haut-parleur ou du système audio de l’ordinateur. Un tel « téléphone logiciel » peut être une application qui utilise l’interface TAPI. Il peut également s’agir d’un fournisseur de services, qui peut être listé comme un appareil téléphonique disponible pour d’autres applications par le biais de l’API. par conséquent, un identificateur de périphérique téléphonique leur est attribué.

En fonction de l’environnement et de la configuration, les ensembles de téléphones peuvent être des appareils partagés entre l’application et le commutateur. Une configuration mineure est effectuée dans l’API dans laquelle le commutateur peut suspendre temporairement le contrôle de l’API d’un appareil téléphonique.

 

 



