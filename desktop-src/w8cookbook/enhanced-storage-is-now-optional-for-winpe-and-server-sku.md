---
title: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
description: Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028847"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>Le stockage étendu est maintenant facultatif pour WINPE et la référence de serveur

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

le stockage étendu était toujours disponible sur les périphériques USB Windows 7. Avec la version de Windows 8, il est disponible pour tous les périphériques de stockage. Dans les périphériques basés sur le client, il est activé par défaut. dans périphériques serveur, cette option est facultative et doit être approvisionnée via environnement de préinstallation Windows (WinPE) (WinPE).

## <a name="manifestation"></a>Manifestation

Le périphérique serveur échoue si le stockage étendu n’est pas activé.

Les périphériques de démarrage doivent être approvisionnés via WinPE avec cette option activée.

## <a name="solution"></a>Solution

Étant donné que le stockage étendu est facultatif pour le serveur d’exécution, les développeurs doivent l’ajouter à WinPE pour l’approvisionnement et l’activation de ces lecteurs. Pour plus d’informations, consultez le Guide de déploiement.

Les administrateurs de serveur doivent ensuite configurer explicitement leur serveur pour qu’ils utilisent le stockage étendu.

 

 




