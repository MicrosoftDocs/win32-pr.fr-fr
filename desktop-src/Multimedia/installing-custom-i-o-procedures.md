---
title: Installation des procédures d’e/s personnalisées
description: Installation des procédures d’e/s personnalisées
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de fichier multimédia, procédures personnalisées
- e/s de fichier, procédures personnalisées
- entrées et sorties (e/s), procédures personnalisées
- E/s (entrée et sortie), procédures personnalisées
- installation des procédures d’e/s personnalisées
- e/s personnalisées
- mmioInstallIOProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368420"
---
# <a name="installing-custom-io-procedures"></a>Installation des procédures d’e/s personnalisées

Pour installer une procédure d’e/s associée au. L’extension de nom de fichier ARC, utilisez la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) comme suit :


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Lorsque vous installez une procédure d’e/s à l’aide de [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), la procédure reste installée jusqu’à ce que vous la supprimiez. La procédure d’e/s est utilisée pour tout fichier que vous ouvrez tant que le fichier a l’extension de nom de fichier appropriée.

Vous pouvez également installer temporairement une procédure d’e/s à l’aide de la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Dans ce cas, la procédure d’e/s est utilisée uniquement avec un fichier ouvert à l’aide de **mmioOpen** et elle est supprimée lorsque le fichier est fermé à l’aide de la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) . Pour spécifier une procédure d’e/s lorsque vous ouvrez un fichier à l’aide de **mmioOpen**, utilisez le paramètre *lpmmioinfo* pour référencer une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) comme suit :

1.  Affectez la valeur **null** au membre **fccIOProc** .
2.  Définissez le membre **pIOProc** sur l’adresse de l’instance de procédure de la procédure d’e/s.
3.  Affectez à tous les autres membres la valeur zéro (sauf si vous ouvrez un fichier de mémoire ou si vous lisez ou écrivez directement dans le tampon d’e/s de fichier).

Veillez à supprimer toutes les procédures d’e/s que vous avez installées avant de quitter votre application.

 

 