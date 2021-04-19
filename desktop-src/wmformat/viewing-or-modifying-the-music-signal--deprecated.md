---
title: Affichage ou modification du signal musical (déconseillé)
description: Affichage ou modification du signal musical (déconseillé)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure audio Path (SAP)
- gestion des droits numériques (DRM), Microsoft Secure audio Path (SAP)
- DRM (gestion des droits numériques), Microsoft Secure audio Path (SAP)
- Windows Media Format SDK, Secure audio Path (SAP)
- gestion des droits numériques (DRM), chemin audio sécurisé (SAP)
- DRM (gestion des droits numériques), chemin d’accès audio sécurisé (SAP)
- Windows Media Format SDK, musique signal (affichage ou modification)
- gestion des droits numériques (DRM), affichage ou modification des signaux musicaux
- DRM (gestion des droits numériques), affichage ou modification des signaux musicaux
- Microsoft Secure audio Path (SAP), affichage ou modification des signaux musicaux
- Chemin audio sécurisé (SAP), affichage ou modification d’un signal musical
- SAP (chemin d’accès audio sécurisé), affichage ou modification d’un signal musical
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513490"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Affichage ou modification du signal musical (déconseillé)

Cette page documente une fonctionnalité qui sera prise en charge avec une autre solution technique dans les futures versions de Windows.

Dans le modèle SAP (Secure audio Path) de Microsoft, les applications ne peuvent pas modifier la musique protégée de quelque manière que ce soit. Par exemple, lorsqu’une application tente d’intercepter un signal musical, le signal ressemble à un bruit aléatoire. Par conséquent, les applications qui modifient normalement les signaux (par exemple, un égaliseur) ne peuvent pas modifier le son de la musique.

Certaines applications affichent simplement un signal musical. Par exemple, certaines applications affichent des lumières clignotantes dans le temps avec le signal musical, mais ne les modifient pas. Pour prendre en charge les applications qui affichent des signaux, une petite partie de la musique est déchiffrée et transmise sous forme claire avec le contenu chiffré. Le signal résultant est très médiocre (pire que la qualité téléphonique), mais peut suffire pour les applications qui affichent des signaux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Chemin d’accès audio sécurisé Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




