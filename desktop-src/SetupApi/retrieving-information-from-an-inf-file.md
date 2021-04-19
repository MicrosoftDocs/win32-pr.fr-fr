---
description: Une fois que vous avez un handle vers un fichier INF, vous pouvez en extraire des informations de différentes façons. Les fonctions telles que SetupGetInfInformation, SetupQueryInfFileInformation et SetupQueryInfVersionInformation récupèrent des informations sur le fichier INF lui-même.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Récupération d’informations à partir d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525077"
---
# <a name="retrieving-information-from-an-inf-file"></a>Récupération d’informations à partir d’un fichier INF

Une fois que vous avez un handle vers un fichier INF, vous pouvez en extraire des informations de différentes façons. Les fonctions telles que [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)et [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) récupèrent des informations sur le fichier INF lui-même.

D’autres fonctions, telles que [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) et [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , acquièrent des informations sur les fichiers sources et les répertoires cibles.

Les fonctions de bas niveau, telles que [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) et [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) , vous permettent d’accéder directement aux informations stockées dans une ligne ou un champ d’un fichier INF. Ces fonctions sont utilisées en interne par les fonctions de niveau supérieur, mais elles sont également disponibles si vous devez accéder aux informations INF au niveau de la ligne ou du champ.

 

 



