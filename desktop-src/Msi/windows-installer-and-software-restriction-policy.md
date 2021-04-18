---
description: Windows Installer est intégré à la stratégie de restriction logicielle dans Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer et stratégie de restriction logicielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533958"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Installer et stratégie de restriction logicielle

Windows Installer est intégré à la stratégie de restriction logicielle dans Microsoft Windows XP. La stratégie de restriction logicielle est configurable via la stratégie de groupe. La stratégie de restriction logicielle permet à un administrateur de limiter les administrateurs et les non-administrateurs à l’exécution de fichiers en fonction du chemin d’accès, de la zone d’URL, du hachage ou des critères du serveur de publication. La stratégie de restriction logicielle a deux niveaux : non restreint et interdit. Le Windows Installer installe uniquement les packages autorisés à s’exécuter au niveau non restreint.

Les correctifs ou les transformations doivent également être autorisés à s’exécuter au niveau non restreint. Si un package, un correctif ou une transformation est configuré pour s’exécuter à un niveau différent de non restreint, le Windows Installer affiche un message d’erreur et enregistre une entrée dans le journal des événements de l’application. La stratégie de restriction logicielle est évaluée lors de la première installation d’une application, lors de l’application d’un nouveau correctif, et lors de la remise en cache du package d’installation.

Si un package, un correctif ou une transformation est limité, le Windows Installer affiche un message d’erreur et écrit une entrée de [journalisation des événements](event-logging.md) dans le journal des événements de l’application. La stratégie de restriction logicielle est évaluée lors de la première installation d’une application, lors de l’application d’un nouveau correctif, et lors de la remise en cache du package d’installation.

Pour plus d’informations sur la stratégie de restriction logicielle, consultez la documentation du produit et [recherchez sur le site TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



