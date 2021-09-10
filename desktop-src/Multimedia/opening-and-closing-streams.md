---
title: Ouverture et fermeture de Flux
description: Ouverture et fermeture de Flux
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- AVIFileGetStream fonction)
- AVIStreamRelease fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369247"
---
# <a name="opening-and-closing-streams"></a>Ouverture et fermeture de Flux

L’ouverture de flux de données est semblable à l’ouverture de fichiers. Vous pouvez ouvrir un flux à l’aide de la fonction [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Cette fonction crée une interface de flux, place un handle du flux dans l’interface et retourne un pointeur vers l’interface. **AVIFileGetStream** gère également un décompte de références des applications qui ont ouvert un flux, mais pas celles qui l’ont fermé.

Si vous souhaitez accéder à un flux unique dans un fichier, vous pouvez ouvrir le fichier et le flux à l’aide de la fonction [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) . Cette fonction combine les arguments Operations et Function des fonctions [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) et **AVIFileGetStream** .

Pour accéder à plusieurs flux dans un fichier, utilisez **AVIFileOpen** une fois suivi de plusieurs appels à **AVIFileGetStream**.

Vous pouvez incrémenter le décompte de références d’un flux à l’aide de la fonction [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) pour garder un flux ouvert lors de l’utilisation d’une fonction qui fermerait normalement le flux.

Vous pouvez fermer un flux à l’aide de la fonction [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Cette fonction décrémente le décompte de références du flux et la ferme lorsque le nombre de références atteint zéro. Vos applications doivent équilibrer le nombre de références en incluant un appel à **AVIStreamRelease** pour chaque utilisation de la fonction [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** ou **AVIStreamOpenFromFile** . Lorsque vous publiez un flux qui a été ouvert à l’aide de **AVIStreamOpenFromFile**, avifile ferme le fichier contenant le flux. Si votre application libère un fichier qui a des flux de données ouverts, AVIFile ne ferme pas les flux tant que tous les flux n’ont pas été libérés.

 

 




