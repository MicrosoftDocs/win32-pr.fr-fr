---
description: Avec Moniteur réseau, la sélection d’une carte réseau par programmation est un processus en deux étapes. Tout d’abord, créez l’objet BLOB de filtre en appelant la méthode CreateBlob. Ensuite, sélectionnez la carte réseau en appelant la méthode GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128899"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Sélection d’une carte réseau à l’aide de GetNPPBlobFromUI

Avec Moniteur réseau, la sélection d’une carte réseau par programmation est un processus en deux étapes. Tout d’abord, créez l’objet BLOB de filtre en appelant la méthode [**CreateBlob**](createblob.md) . Ensuite, sélectionnez la carte réseau en appelant la méthode [**GetNPPBlobFromUI**](getnppblobfromui.md) .

Dans cet exemple, un objet BLOB de filtre est utilisé pour sélectionner la carte réseau requise :


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



