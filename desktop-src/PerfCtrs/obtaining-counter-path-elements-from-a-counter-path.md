---
description: Pour récupérer les éléments d’un chemin d’accès, appelez la fonction PdhParseCounterPath. La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans \_ une \_ structure d’éléments de chemin d’accès de compteur PDH \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007179"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Obtention d’éléments de chemin d’accès de compteur à partir d’un chemin de compteur

Pour récupérer les éléments d’un chemin d’accès, appelez la fonction [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) . La fonction analyse les éléments d’un chemin d’accès de compteur et les retourne dans une structure [**\_ \_ d' \_ éléments de chemin d’accès de compteur PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .

Si vous avez un nom d’instance complexe (un qui contient une instance parente et un index d’instance), vous pouvez appeler la fonction [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) pour extraire le nom de l’instance, l’index d’instance et le nom du parent.

 

 



