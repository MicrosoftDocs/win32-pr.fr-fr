---
description: Déterminez la version de Windows Update Agent (WUA) avant de l’utiliser.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Détermination de la version actuelle de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524968"
---
# <a name="determining-the-current-version-of-wua"></a>Détermination de la version actuelle de WUA

Pour obtenir des informations générales sur la mise à jour de l’agent WUA, y compris des instructions pas à pas pour déterminer par programmation à partir de votre application si la version de WUA exécutée sur l’ordinateur répond à vos besoins, consultez [mise à jour de l’agent de Windows Update](updating-the-windows-update-agent.md).

Dans les versions de Windows antérieures à Windows 7 et Windows Server 2008 R2, vous devez déterminer la version installée de Windows Update Agent (WUA) avant de l’utiliser. La version actuelle de WUA est déterminée par la version du Wuaueng.dll qui s’exécute dans le \\ sous-répertoire system32 de l’installation Windows actuelle. Si la version de Wuaueng.dll est la version 5.4.3790.1000 ou une version ultérieure, WUA est installé. Une version antérieure à 5.4.3790.1000 indique que Software Update Services (SUS) 1,0 est installé.

Lorsqu’un appel à SUS 1,0 est effectué à l’aide de l’API WUA, un **HRESULT** de Wu \_ E au \_ \_ LEGACYSERVER est retourné.

Vous pouvez également utiliser la méthode [**IWindowsUpdateAgentInfo :: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) pour récupérer la version de fichier actuelle de Wuapi.dll qui s’exécute sur un ordinateur. L’interface [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) n’est pas prise en charge dans WUA 1,0.
