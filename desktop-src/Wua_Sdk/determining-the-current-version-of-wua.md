---
description: déterminez la version de Windows Update Agent (WUA) avant de l’utiliser.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Détermination de la version actuelle de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049497"
---
# <a name="determining-the-current-version-of-wua"></a>Détermination de la version actuelle de WUA

pour obtenir des informations générales sur la mise à jour de l’agent wua, y compris des instructions pas à pas pour déterminer par programmation à partir de votre application si la version de WUA exécutée sur l’ordinateur répond à vos besoins, consultez [mise à jour de l’Agent de Windows Update](updating-the-windows-update-agent.md).

dans les versions de Windows antérieures à Windows 7 et Windows Server 2008 R2, vous devez déterminer la version installée de Windows Update Agent (WUA) avant de l’utiliser. la version actuelle de WUA est déterminée par la version du Wuaueng.dll qui s’exécute dans le \\ sous-répertoire System32 de l’installation Windows actuelle. Si la version de Wuaueng.dll est la version 5.4.3790.1000 ou une version ultérieure, WUA est installé. Une version antérieure à 5.4.3790.1000 indique que Software Update Services (SUS) 1,0 est installé.

Lorsqu’un appel à SUS 1,0 est effectué à l’aide de l’API WUA, un **HRESULT** de Wu \_ E au \_ \_ LEGACYSERVER est retourné.

Vous pouvez également utiliser la méthode [**IWindowsUpdateAgentInfo :: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) pour récupérer la version de fichier actuelle de Wuapi.dll qui s’exécute sur un ordinateur. L’interface [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) n’est pas prise en charge dans WUA 1,0.
