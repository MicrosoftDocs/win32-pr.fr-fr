---
title: Liaison à la DLL d’accès à distance
description: Si une application est liée de manière statique à la DLL RASAPI32, le chargement de l’application échoue si le service d’accès à distance n’est pas installé.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b98757320cf9a166e741eb10ace8607d0287740a5494ca20fcc431b16b4367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790649"
---
# <a name="linking-to-the-remote-access-dll"></a>Liaison à la DLL d’accès à distance

Si une application est liée de manière statique à la DLL RASAPI32, le chargement de l’application échoue si le service d’accès à distance n’est pas installé. Une application RAS peut se charger lorsque RAS n’est pas installé à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger la dll et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir des pointeurs vers les fonctions RAS.

Les fonctions RAS se trouvent dans RASAPI32.DLL. La bibliothèque d’importation pour ces fonctions est RASAPI32. LIB. Pour utiliser les fonctions RAS, vos programmes doivent inclure les fichiers suivants :



| Fichier       | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| Exécutant. Manutention      | Contient les prototypes de fonction RAS, les constantes et les définitions de structure. |
| RASERROR. Manutention | Contient les codes d’erreur RAS.                                               |



 

 

 