---
title: Restauration du système
description: À mesure que l’ordinateur est utilisé au fil du temps, les points de restauration sont collectés dans l’archive de données sans aucune gestion ou intervention requise de la part de l’utilisateur.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106527136"
---
# <a name="restoring-the-system"></a>Restauration du système

À mesure que l’ordinateur est utilisé au fil du temps, les points de restauration sont collectés dans l’archive de données sans aucune gestion ou intervention requise de la part de l’utilisateur. Si l’utilisateur doit restaurer le système à un état antérieur, les points de restauration disponibles sont rendus visibles à l’utilisateur par le biais de l’interface utilisateur de la restauration du système. L’utilisateur peut choisir n’importe lequel de ces points de restauration. La seule façon d’accéder à cette archive des points de restauration consiste à utiliser l’interface utilisateur de la restauration du système et l’API de restauration du système. Cela permet de protéger l’intégrité des données et d’empêcher les modifications accidentelles apportées par l’utilisateur, les applications ou d’autres agents.

Pour restaurer un système, la restauration du système annule les modifications apportées aux fichiers surveillés, en recapturant l’état du fichier au moment du point de restauration sélectionné. Il remplace ensuite le registre actuel par celui enregistré pour le point de restauration sélectionné.

Pour vous assurer que votre application a le comportement souhaité après une restauration, procédez comme suit :

-   Ne stockez pas d’informations dans le Registre qui empêche l’accès des utilisateurs aux fichiers de données personnels ou aux applications lors de la restauration du système. Dans le cas contraire, vous devez fournir un mécanisme permettant à l’utilisateur de télécharger et de réinstaller les applications sans avoir à les payer à nouveau.
-   Utilisez l' [API de restauration du système](system-restore-api.md) pour créer des points de restauration significatifs lors de l’installation et de la désinstallation.
-   Dans Windows XP, les binaires d’application clés à protéger doivent utiliser des extensions conformes à celles utilisées dans Filelist.xml. Pour plus d’informations, consultez [extensions de nom de fichier surveillées](monitored-file-extensions.md). Ce fichier n’est pas utilisé par Windows 7 et Windows Vista. N’utilisez pas de types d’extension analysés pour les fichiers modifiables par l’utilisateur. Par exemple, si vous nommez le fichier de données personnel d’un utilisateur à l’aide de l’extension. ini, l’utilisateur peut perdre son travail suite à une restauration du système.

 

 




