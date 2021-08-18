---
title: Développement et déploiement sur le réseau
description: La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930619"
---
# <a name="development-vs-deployment-in-the-network"></a>Développement et déploiement sur le réseau

La plupart des développeurs écrivent et testent leurs logiciels sur un réseau local fiable et rapide. Le client et le serveur sont souvent sur le même segment de réseau. Dans ce cas, le réseau ne répond rarement pas et la connectivité est rarement perdue. En cas de déploiement dans un environnement client, toutefois, le client et le serveur sont souvent sur différents segments du réseau, éventuellement à distance géographique, et le serveur est très chargé avec d’autres clients. En d’autres termes : la réactivité du réseau ne peut pas être utilisée.

Cet article explique comment créer des architectures client/serveur robustes face à l’incertitude introduite par un réseau intrinsèquement fiable et des serveurs potentiellement indisponibles.

 

 




