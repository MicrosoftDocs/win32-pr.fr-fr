---
description: Le fournisseur de Registre système tente d’envoyer une notification pour chaque événement qui se produit.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Réception d’événements de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034257"
---
# <a name="receiving-registry-events"></a>Réception d’événements de Registre

Le fournisseur de Registre système tente d’envoyer une notification pour chaque événement qui se produit. Toutefois, le fournisseur de Registre système ne garantit pas que le consommateur recevra un ou tous les événements. L’exception est que le fournisseur de Registre système s’assure qu’un consommateur recevra une notification pour chaque inscription d’événement.

Par exemple, supposons qu’un consommateur s’inscrit pour deux événements de changement d’arborescence, en demandant une notification pour les instances [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) . Chaque inscription a la même valeur Hive (sous-arborescence) mais une valeur RootPath différente. Si les clés des deux chemins changent plusieurs fois, le fournisseur de Registre système garantit que le consommateur recevra une notification pour chaque chemin d’accès. En fonction du temps de réponse du Registre et du fournisseur de Registre système, le consommateur peut recevoir autant de notifications qu’il y avait d’occurrences d’événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription pour les événements du Registre système](registering-for-system-registry-events.md)
</dt> </dl>

 

 
