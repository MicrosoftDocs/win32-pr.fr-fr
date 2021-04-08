---
description: En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Utilisation de Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757612"
---
# <a name="using-microsoft-foundation-classes"></a>Utilisation de Microsoft Foundation Classes

En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert. Toutefois, si vous utilisez les MFC, veillez à accéder à toutes les ressources DLL MFC en incluant le code suivant immédiatement à l’entrée :

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



