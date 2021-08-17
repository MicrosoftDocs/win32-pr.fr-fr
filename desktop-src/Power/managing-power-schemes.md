---
description: Gestion du mode de gestion de l’alimentation
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gestion du mode de gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4717fd8efc91a520e178baac6ad9138028f306386ed2ee1141b76a423b16e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143402"
---
# <a name="power-scheme-management"></a>Gestion du mode de gestion de l’alimentation

Chaque mode de gestion de l’alimentation est identifié de manière unique par un **GUID**. Pour énumérer tous les modes de gestion de l’alimentation disponibles, utilisez la fonction [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) . **PowerEnumerate** peut également être utilisé pour récupérer tous les paramètres d’alimentation pour un schéma spécifié.

Le mode de gestion de l’alimentation en cours d’utilisation sur le système est appelé mode de gestion de l’alimentation ou plan actif. Pour récupérer le **GUID** du plan actif, appelez la fonction [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) . Pour modifier le mode de gestion de l’alimentation actif, appelez la fonction [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .

Pour créer un mode de gestion de l’alimentation, vous devez d’abord dupliquer un schéma existant à l’aide de la fonction [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , en spécifiant le **GUID** du schéma sur lequel vous souhaitez baser votre nouveau schéma. Vous devez copier l’un des schémas intégrés et modifier les paramètres d’alimentation selon vos besoins. Notez que la création d’un mode de gestion de l’alimentation ne met pas automatiquement à jour le mode de gestion de l’alimentation actif. Vous devez toujours appeler [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) pour mettre à jour le mode de gestion de l’alimentation actif. Les modes de gestion de l’alimentation existants peuvent être modifiés, puis appliqués de la même manière.

Pour supprimer un mode de gestion de l’alimentation, appelez la fonction [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .

> [!Note]  
> Pour récupérer des informations supplémentaires sur l’état d’alimentation du système, appelez la fonction [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes de gestion de l’alimentation](power-schemes.md)
</dt> </dl>

 

 



