---
title: Configuration des compresseurs et des décompresseurs
description: Configuration des compresseurs et des décompresseurs
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Gestionnaire de compression vidéo (VCM), configuration des compresseurs
- VCM (gestionnaire de compression vidéo), configuration des compresseurs
- ICQueryConfigure macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379865"
---
# <a name="configuring-compressors-and-decompressors"></a>Configuration des compresseurs et des décompresseurs

L’exemple suivant utilise la macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) pour montrer comment tester si un compresseur prend en charge la boîte de dialogue de configuration et pour l’afficher si c’est le cas.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



L’exemple suivant montre comment obtenir les données d’État à l’aide de la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



L’exemple suivant montre comment restaurer des données d’État à l’aide de la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) . Les données d’État restaurées par les applications ne doivent pas contenir de modifications des données d’État obtenues à partir d’un pilote.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




