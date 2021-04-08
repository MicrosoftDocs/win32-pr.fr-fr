---
description: Il existe plusieurs fonctions qu’une application doit appeler pour demander des fonctionnalités.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Demande d’une fonctionnalité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034748"
---
# <a name="requesting-a-feature"></a>Demande d’une fonctionnalité

Il existe plusieurs fonctions qu’une application doit appeler pour demander des fonctionnalités. Avant de demander une fonctionnalité, l’application doit s’assurer que la fonctionnalité est installée. Si l’application appelle [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) avant que l’application n’accède à une fonctionnalité, l’application peut utiliser les informations retournées pour conserver les métriques d’utilisation.

**Pour demander une fonctionnalité**

1.  Appelez la fonction [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ou [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) si vous souhaitez déterminer la disponibilité d’une fonctionnalité sans incrémenter le nombre d’utilisations.
2.  Indiquez l’intention de votre application d’utiliser une fonctionnalité en appelant la fonction [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .
3.  Déterminez les emplacements des fichiers en appelant la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .
4.  Configurez la fonctionnalité en appelant la fonction [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .
5.  Obtenez les métriques d’utilisation que votre application peut utiliser en appelant la fonction [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .

Le diagramme suivant illustre le modèle de demande de fonctionnalité.

![modèle de demande de fonctionnalité. ](images/over2.png)

 

 



