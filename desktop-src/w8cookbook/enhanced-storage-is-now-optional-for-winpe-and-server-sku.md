---
title: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
description: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316596"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Le stockage étendu était toujours disponible sur les périphériques USB Windows 7. Avec la sortie de Windows 8, il est disponible pour tous les périphériques de stockage. Dans les périphériques basés sur le client, il est activé par défaut. dans périphériques serveur, cette option est facultative et doit être approvisionnée via environnement de préinstallation Windows (WinPE) (WinPE).

## <a name="manifestation"></a>Manifestation

Le périphérique serveur échoue si le stockage étendu n’est pas activé.

Les périphériques de démarrage doivent être approvisionnés via WinPE avec cette option activée.

## <a name="solution"></a>Solution

Étant donné que le stockage étendu est facultatif pour le serveur d’exécution, les développeurs doivent l’ajouter à WinPE pour l’approvisionnement et l’activation de ces lecteurs. Pour plus d’informations, consultez le Guide de déploiement.

Les administrateurs de serveur doivent ensuite configurer explicitement leur serveur pour qu’ils utilisent le stockage étendu.

 

 




