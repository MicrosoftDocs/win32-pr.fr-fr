---
description: La structure COMMCONFIG définit la configuration d’une ressource de communication, en série ou dans le cas contraire.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuration des ressources de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01cd85a60eabc3cf6adcbdb0e05d2fbdc662442029044a5ac67d9a37bc073d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918319"
---
# <a name="communications-resource-configuration"></a>Configuration des ressources de communication

La structure [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) définit la configuration d’une ressource de communication, en série ou dans le cas contraire. Le format de la structure varie selon le type de ressource de communication (le sous-type de fournisseur). Les premiers membres de la structure sont communs à toutes les ressources de communication ; des membres supplémentaires sont définis pour des sous-types de fournisseur spécifiques. Les fournisseurs de services spécifiques peuvent également étendre la structure **COMMCONFIG** .

Une application peut obtenir et définir la configuration d’une ressource de communication à l’aide des fonctions [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) et [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) . Une fois ouverte, une ressource de communication est initialisée à l’aide de la configuration par défaut pour son sous-type de fournisseur. Pour obtenir et définir la configuration par défaut d’un sous-type de fournisseur, utilisez les fonctions [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) et [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .

Pour inviter l’utilisateur à fournir des informations de configuration, utilisez la fonction [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) . Cette fonction affiche une boîte de dialogue définie par le fournisseur de services et remplit une structure [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) en fonction de l’entrée de l’utilisateur.

 

 



