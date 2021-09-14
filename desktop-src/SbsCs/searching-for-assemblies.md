---
description: Il existe deux méthodes permettant à une application d’hébergement de rechercher des assemblys côte à côte.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Recherche d’assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121222"
---
# <a name="searching-for-assemblies"></a>Recherche d’assemblys

Il existe deux méthodes permettant à une application d’hébergement de rechercher des assemblys côte à côte.

Les modules hébergés peuvent s’inscrire auprès de l’application d’hébergement en étendant certaines informations de configuration partagée. L’application peut ensuite utiliser ces informations de configuration pour charger les assemblys requis pour la nouvelle fonctionnalité. Cela peut être fait en appelant [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) sur les manifestes spécifiés dans les données d’inscription, puis en appelant [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour accéder au nouveau module. Notez qu’avec cette méthode, les nouveaux composants doivent mettre à jour un état d’application partagé pour indiquer leur présence.

L’application d’hébergement peut rechercher activement les assemblys au démarrage à l’aide de [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) pour rechercher des dll ou des manifestes à un emplacement spécifié, puis utiliser [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) pour accéder aux informations. Cette méthode ne requiert aucune inscription du composant.

 

 
