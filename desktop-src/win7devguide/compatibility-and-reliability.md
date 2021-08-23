---
title: Compatibilité et fiabilité
description: Windows 7 est conçu pour s’exécuter sur le même matériel que Windows vista et pour être compatible avec les applications et les pilotes de périphériques qui fonctionnent avec Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e42dbf564fc524fbfb620746cea84e387fbe9f76484ce9e0d87803f55dae4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706299"
---
# <a name="compatibility-and-reliability"></a>Compatibilité et fiabilité

Windows 7 est conçu pour s’exécuter sur le même matériel que Windows vista et pour être compatible avec les applications et les pilotes de périphériques qui fonctionnent avec Windows Vista.

Windows 7 est la version la plus fiable de Windows encore. conçu sur une fondation technologique améliorée, Windows 7 permet aux utilisateurs de démarrer, d’arrêter ou de mettre en veille de manière fiable leurs ordinateurs sans avoir à se soucier de la perte d’un travail précieux. en outre, Windows 7 facilite plus que jamais la sauvegarde et la restauration des données sur des lecteurs réseau ou des disques vidéo numériques (dvd). Windows 7 améliore également la fiabilité et les performances d’impression. (voir [Windows 7](../win7appqual/windows-7-application-quality-cookbook.md)livre de recettes sur la qualité des applications.)

## <a name="applications"></a>Applications

pour garantir la compatibilité, Windows 7 a été conçu en partenariat étroit avec les éditeurs de logiciels et les fabricants de PC. L’engagement précoce a permis à Microsoft de créer une liste complète des applications les plus couramment utilisées. Les cycles de tests automatisés garantissent que les problèmes de compatibilité sont détectés et résolus au début du cycle de développement. (voir [Windows compatibilité des applications](/windows/apps/desktop/).)

## <a name="drivers"></a>Pilotes

Windows Driver Kit (WDK) version 7.0.0 fournit l’environnement de génération, les outils, la documentation et les exemples dont les développeurs ont besoin pour créer des pilotes de qualité pour Windows. WDK 7.0.0 prend en charge l’analyse statique du code source, à l’aide de PREfast pour détecter certaines classes d’erreurs de codage C et C++. PREfast comprend un composant de pilote spécialisé, appelé PREfast for drivers (PFD), qui détecte les erreurs dans le code du pilote en mode noyau. En outre, le kit WDK a été amélioré en annotant tous les fichiers d’en-tête du noyau pour la prise en charge de PFD. De nouveaux exemples de pilotes ont été ajoutés pour illustrer les nouvelles technologies et la documentation a été développée.

Windows 7 prend en charge un large éventail de produits logiciels et matériels conçus pour s’intégrer en toute transparence à la plateforme. les pilotes qui ont été créés pour Windows Vista ne doivent pas nécessiter une mise à jour pour s’exécuter correctement dans Windows 7. (voir [Kit de pilotes Windows](/windows-hardware/drivers/).)

## <a name="devices"></a>Appareils

Windows 7 offre une prise en charge flexible et robuste pour un large éventail d’applications et de périphériques, y compris les lecteurs musicaux, les périphériques de stockage, les téléphones mobiles et d’autres types d’appareils connectés. Le test automatique de ces appareils est utilisé pour s’assurer que les problèmes de compatibilité sont résolus au début du cycle de développement. (consultez [Windows notions de base](https://www.microsoft.com/whdc/device/default.mspx)de la classe d’appareil.)

## <a name="reliability-analysis-component"></a>Composant d’analyse de fiabilité

Le Composant d'analyse de fiabilité est un agent intégré qui fournit des informations détaillées de l'expérience du client sur l'utilisation du système et la fiabilité. Ces informations sont affichées via une interface WMI (Windows Management Instrumentation), qui permet leur lecture sur un système PRS (Portable Reader System). En exposant le Composant d'analyse de fiabilité via une interface WMI, les développeurs peuvent surveiller et analyser leurs applications, en augmentant la fiabilité et les performances.

Windows 7 utilise le composant d’analyse de fiabilité intégré pour calculer un index de fiabilité qui fournit des informations sur l’utilisation globale du système et la stabilité dans le temps. RAC effectue également le suivi des modifications importantes apportées au système et qui peuvent avoir un impact sur la stabilité, par exemple les mises à jour Windows, les installations d'applications. Vous pouvez utiliser le composant logiciel enfichable Moniteur de fiabilité pour voir les tendances de l’index de fiabilité de votre système corrélées avec ces événements potentiellement déstabilisants, ce qui facilite le suivi d’une modification de fiabilité directement dans un événement particulier. (Voir [fonction MountVHD](/previous-versions/windows/desktop/msvs/mountvhd).)

 

 