---
description: Pour récupérer les éléments d’un chemin d’accès, appelez la fonction PdhParseCounterPath. La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans \_ une \_ structure d’éléments de chemin d’accès de compteur PDH \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c8df5c7176684fc439f632a22f829afe5afae202f7595579350450ee30c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143972"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur

Pour récupérer les éléments d’un chemin d’accès, appelez la fonction [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) . La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans une structure [**\_ \_ d' \_ éléments de chemin d’accès de compteur PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .

Si vous avez un nom d’instance complexe (un qui contient une instance parente et un index d’instance), vous pouvez appeler la fonction [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) pour extraire le nom de l’instance, l’index d’instance et le nom du parent.

 

 



