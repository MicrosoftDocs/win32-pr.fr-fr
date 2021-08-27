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
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071519"
---
# <a name="creating-a-managed-wmi-client"></a>Création d’un client WMI géré

La version actuelle de WMI contient l’espace de noms System. Management, qui expose un certain nombre d’API qui interagissent avec WMI. Toutefois, il n’est pas recommandé d’utiliser cet espace de noms.

si vous souhaitez créer un client WMI géré, il est recommandé d’utiliser l’Infrastructure de gestion des Windows (MI). MI est la version de la nouvelle génération de WMI et contient la prise en charge complète du code managé. Pour plus d’informations, consultez [comment implémenter un client mi géré](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 
