---
description: En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Utilisation de Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362928"
---
# <a name="using-microsoft-foundation-classes"></a>Utilisation de Microsoft Foundation Classes

En raison de l’encombrement des DLL liées statiquement, évitez d’utiliser Microsoft Foundation Classes (MFCs) pour écrire un expert. Toutefois, si vous utilisez les MFC, veillez à accéder à toutes les ressources DLL MFC en incluant le code suivant immédiatement à l’entrée :

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



