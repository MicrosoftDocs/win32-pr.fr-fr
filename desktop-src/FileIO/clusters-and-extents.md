---
description: 'Les clusters peuvent être référencés à partir de deux perspectives différentes : dans le fichier et sur le volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clusters et étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545824"
---
# <a name="clusters-and-extents"></a>Clusters et étendues

Les clusters peuvent être référencés à partir de deux perspectives différentes : dans le fichier et sur le volume. Tout cluster d’un fichier a un *numéro de cluster virtuel* (VCN), qui est son décalage relatif par rapport au début du fichier. Par exemple, une recherche sur deux fois la taille d’un cluster, suivie d’une lecture, renverra des données en commençant au troisième VCN. Un *numéro de cluster logique* (LCN) décrit le décalage d’un cluster à partir d’un point arbitraire au sein du volume. LCNs doit être traité uniquement comme des nombres ordinaux ou relatifs. Il n’existe aucun mappage garanti de clusters logiques vers des secteurs de lecteur de disque dur physique.

Une *extension* est une exécution de clusters contigus. Supposons, par exemple, qu’un fichier composé de 30 clusters soit enregistré dans deux extensions. La première extension peut être constituée de cinq clusters contigus, l’autre des 25 clusters restants.

Il n’existe aucune garantie de relation sur le disque, quelle que soit l’étendue de l’étendue. Par exemple, la première extension peut être à un LCN plus élevé qu’une autre étendue.

 

 



