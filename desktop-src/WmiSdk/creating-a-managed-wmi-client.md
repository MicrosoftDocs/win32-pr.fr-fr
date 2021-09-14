---
description: WMI ne prend pas actuellement en charge le code managé sur WMI, mais il est pris en charge sur MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Création d’un client WMI géré
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292211"
---
# <a name="creating-a-managed-wmi-client"></a>Création d’un client WMI géré

La version actuelle de WMI contient l’espace de noms System. Management, qui expose un certain nombre d’API qui interagissent avec WMI. Toutefois, il n’est pas recommandé d’utiliser cet espace de noms.

si vous souhaitez créer un client WMI géré, il est recommandé d’utiliser l’Infrastructure de gestion des Windows (MI). MI est la version de la nouvelle génération de WMI et contient la prise en charge complète du code managé. Pour plus d’informations, consultez [comment implémenter un client mi géré](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
