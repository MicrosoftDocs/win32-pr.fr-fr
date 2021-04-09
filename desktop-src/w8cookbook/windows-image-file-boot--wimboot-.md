---
title: Démarrage du fichier image Windows (WimBoot)
description: Démarrage du fichier image Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734644"
---
# <a name="windows-image-file-boot-wimboot"></a>Démarrage du fichier image Windows (WimBoot)

## <a name="platform"></a>Plateforme

**Clients :** Windows 8.1  

## <a name="description"></a>Description

WimBoot est une autre façon pour les fabricants OEM de déployer Windows. Un déploiement WimBoot démarre et exécute Windows directement à partir d’un fichier image Windows (WIM) compressé. Ce fichier WIM est immuable et son accès est géré par un nouveau pilote de filtre de système de fichiers (WoF.sys).

Le résultat est une réduction significative de l’espace disque nécessaire à l’installation de Windows.

## <a name="manifestations"></a>Manifestations

La plupart des applications doivent être complètement désaffectées par WimBoot. Seules les applications qui accèdent à des fichiers système ou déverrouillent des fichiers système ou des fichiers préchargés pour l’accès en écriture peuvent être affectées. Étant donné que le fichier WIM est immuable, les mises à jour de celui-ci (c’est-à-dire les fichiers système ou préchargés) sont simplement stockées sur la partition C : \\ .

Si une application a déverrouillé l’accès en écriture pour tous les fichiers système et les fichiers préchargés par le fichier WIM, les économies que WimBoot fournit seraient complètement perdues, car tous ces fichiers seraient décompressés et placés sur le volume C : \\ .

En outre, les applications de sauvegarde et de restauration doivent être conscientes des déploiements de WimBoot, car le fichier WIM est présent dans une partition distincte. autrement dit, lors de la sauvegarde, les partitions C : \\ et Wim doivent être enregistrées et les deux doivent être restaurées ensemble.

## <a name="solution"></a>Solution

De nouvelles API ont été introduites pour permettre aux applications de demander directement si un volume ou un fichier donné est associé à un fichier WIM. Ces informations permettent aux applications de prendre des décisions appropriées, telles que l’ouverture de ces fichiers uniquement pour l’accès en lecture ou pour identifier les volumes/partitions qui doivent être sauvegardées et restaurées ensemble.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Compatibilité, performances, fiabilité ou tests d’utilisation

Les développeurs d’applications doivent tester leurs logiciels et leurs scénarios correspondants sur un système WimBoot, en particulier si ces applications accèdent à des fichiers système ou préchargés. Une attention particulière doit être accordée à une réduction significative de l’espace disque disponible après la fin d’un scénario.

 

 




