---
title: Développement et déploiement sur le réseau
description: La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029086"
---
# <a name="development-vs-deployment-in-the-network"></a>Développement et déploiement sur le réseau

La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide. Le client et le serveur sont souvent sur le même segment de réseau. Dans ce cas, le réseau ne répond rarement pas et la connectivité est rarement perdue. En cas de déploiement dans un environnement client, toutefois, le client et le serveur sont souvent sur différents segments du réseau, éventuellement à distance géographique, et le serveur est très chargé avec d’autres clients. En d’autres termes : la réactivité du réseau ne peut pas être utilisée.

Cet article explique comment créer des architectures client/serveur robustes face à l’incertitude introduite par un réseau intrinsèquement fiable et des serveurs potentiellement indisponibles.

 

 




