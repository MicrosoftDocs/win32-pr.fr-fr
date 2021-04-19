---
description: La \_ classe fournisseurs msft et les classes de résolution des problèmes WMI sont un groupe de classes d’événements msft associées aux événements du fournisseur WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Classes de résolution des problèmes et de configuration du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521228"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Classes de résolution des problèmes et de configuration du fournisseur

La [**classe \_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) et les classes de résolution des problèmes WMI sont un groupe de [classes d’événements msft](msft-classes.md) associées aux événements du fournisseur WMI.

La [**classe \_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contient des informations de configuration pour les fournisseurs et inclut les méthodes suivantes qui vous permettent de charger et de décharger des fournisseurs, ou d’interrompre et de reprendre les opérations du fournisseur :

-   [**Méthode Load de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Méthode Unload de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Méthode Resume de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Méthode suspend de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

Les [classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md) sont nommées pour indiquer si l’événement est déclenché avant ou après un événement de fournisseur. Par exemple, le [**pré-objet \_ wmiprovider \_ AccessCheck \_ msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) est généré immédiatement avant l’appel de l’implémentation du fournisseur de **IWbemEventSecurity :: AccessCheck**, tandis que l’objet [**msft \_ wmiprovider \_ AccessCheck \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) est appelé immédiatement après.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
